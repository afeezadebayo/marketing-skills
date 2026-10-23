---
name: gtm-workflow-qa
description: "QA every row of a Clay or other GTM table against a written spec before sending or syncing: required fields, formats, ICP and exclusion rules, duplicates, CRM mapping, copy checks for placeholders, length, banned phrases, invented facts and tone, code checks plus batched AI judgement, errors grouped by cause and a go or no-go report. Use whenever someone builds outbound or enrichment workflows in Clay or similar tools, wants to QA a table or AI-written copy before launch, check data against a spec, catch quiet workflow failures or validate records before a CRM sync, especially with Claude Code."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/gtm-workflow-qa/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-13"
  updated: "2026-10-13"
---

# GTM Workflow QA

Go-to-market (GTM) workflows built in tools such as Clay chain many steps together: find companies, enrich contacts, run waterfalls across data providers, score fit, write personalised lines with AI, then push records to a CRM or sequencer. Each step can fail quietly. A provider returns an empty value, a formula breaks on one country's data, an AI column writes "[First Name]" or invents a fact, a filter lets the wrong companies through, and hundreds of emails go out before anyone notices. Spot-checking ten rows does not catch problems that affect 3% of a 5,000-row table.

This skill runs row-by-row QA on a GTM table against a written spec. It checks every row for data completeness and format, business rules (ICP fit, exclusions, routing), copy quality (personalisation, tone, banned words, claims) and technical requirements (field mapping, duplicates, CRM readiness), using deterministic checks in code and AI judgement only where rules cannot decide. It produces a pass or fail per row, an error summary by cause, examples and fixes, and a go or no-go recommendation before anything is sent or synced.

## Operating principles
1. **The spec is the source of truth.** QA checks rows against written requirements, not against vibes.
2. **Check every row, not a sample.** Quiet failures hide in small percentages.
3. **Code for rules, AI for judgement.** Formats, lengths and lists are checked deterministically; tone and factual fit get AI review.
4. **Group errors by cause.** Fix the step that broke, not each row by hand.
5. **Nothing ships on a fail.** Sending, syncing or launching waits for a go decision.

## Technical requirements
| Requirement | Detail |
|---|---|
| Agent | Claude Code (or another agent that can run Python and read files) |
| Runtime | Python 3.10 or later with pandas (`pip install pandas`) |
| Input | Table export as CSV (from Clay: export the table or a view), UTF-8 |
| Spec | `qa-spec.md` or `qa-spec.yaml` in the same folder (template below) |
| Optional | Clay API or webhook access to pull data directly; CRM field list |
| Output | `qa-report.md`, `qa-results.csv` (row ID, status, failed checks, notes) |
| Scale | Code checks handle tens of thousands of rows; AI review runs in batches (for example 50 rows) to control cost |
| Privacy | Contact data stays local or in approved tools; never paste personal data into unapproved services |

## The QA spec
Write the spec before building or before QA, with the person who owns the campaign.
```yaml
table: outbound-q4-fintech
row_id: record_id
required_fields: [company_name, domain, first_name, last_name, email, title, country, opener_line]
formats:
  email: email
  domain: domain
  linkedin_url: url_contains:linkedin.com/in/
allowed_values:
  country: [United Kingdom, Ireland, Netherlands, Germany]
rules:
  - name: icp_employee_range
    check: employees between 50 and 1000
  - name: exclude_customers
    check: domain not in customers.csv
  - name: title_seniority
    check: title contains any [Head, Director, VP, Chief, Lead]
duplicates:
  unique: [email]
  unique_per_company_max: 3
copy:
  field: opener_line
  max_words: 25
  must_not_contain: ["[", "{", "undefined", "N/A", "I hope this finds you well"]
  must_reference: company_name or recent_signal
  tone: plain, specific, no flattery, British English
  no_invented_facts: true
crm:
  push_fields: {email: Email, first_name: FirstName, company_name: Company}
  required_for_push: [email, company_name, owner]
thresholds:
  max_fail_rate: 2%
  max_copy_fail_rate: 5%
```

## When to use, and when not to
Use it before sending any outbound sequence, before syncing enriched data to a CRM, after changing a workflow step or provider, when launching a new table template, and on a schedule for always-on workflows.

Don't use it as a replacement for data provider compliance checks or legal review of outreach rules (for example data protection and email marketing laws in each country), which the team must handle separately.

## Workflow

### Step 1. Confirm the spec
Read `qa-spec`. If key rules are missing (exclusions, copy limits, thresholds), ask the owner before running.

### Step 2. Load and profile the data
Row count, columns present versus spec, empty rates per column, obvious encoding problems.

### Step 3. Run deterministic checks on every row
Required fields, formats, allowed values, numeric rules, exclusion lists, duplicates, CRM required fields, copy length and forbidden strings.

### Step 4. Run AI judgement checks
Only for checks code cannot decide: does the opener reference something real from the row's data, is the tone right, does it invent a fact, is the title a real decision maker for this offer? Review in batches; record a reason for every fail.

### Step 5. Group failures by cause
Map failed checks to the workflow step that produced them (provider, formula, AI prompt, filter, mapping).

### Step 6. Compare with thresholds
Fail rate overall and per check versus the spec.

### Step 7. Report and recommend
Go, go with fixes (exclude failed rows) or no-go (fix the workflow and re-run).

### Step 8. Re-run after fixes
Run QA again on the corrected table; keep both reports.

## Deterministic checker (starter script)
```python
import pandas as pd, re
df = pd.read_csv("table.csv", dtype=str).fillna("")
results = []
EMAIL = re.compile(r"^[^@\s]+@[^@\s]+\.[a-z]{2,}$", re.I)
BANNED = ["[", "{", "undefined", "N/A", "I hope this finds you well"]
for _, r in df.iterrows():
    fails = []
    for f in ["company_name", "domain", "first_name", "email", "title", "opener_line"]:
        if not r.get(f, "").strip(): fails.append(f"missing:{f}")
    if r.get("email") and not EMAIL.match(r["email"]): fails.append("format:email")
    line = r.get("opener_line", "")
    if len(line.split()) > 25: fails.append("copy:too_long")
    if any(b.lower() in line.lower() for b in BANNED): fails.append("copy:banned_or_placeholder")
    if r.get("company_name") and r["company_name"].lower() not in line.lower(): fails.append("copy:no_company_reference")
    results.append({"record_id": r.get("record_id", ""), "status": "fail" if fails else "pass", "fails": ";".join(fails)})
dup = df[df.duplicated("email", keep=False) & (df["email"] != "")]
out = pd.DataFrame(results)
out.loc[out["record_id"].isin(dup.get("record_id", [])), "fails"] += ";duplicate:email"
out.to_csv("qa-results.csv", index=False)
print(out["status"].value_counts())
```
Extend it from the spec: allowed values, exclusion lists, numeric ranges and CRM mappings.

## Copy checks
| Check | Method | Fail example |
|---|---|---|
| Placeholder left in | Code | "Hi [First Name], loved {company}'s..." |
| Too long | Code | 48-word opener |
| Banned phrases | Code | "I hope this finds you well" |
| References real data | AI with row data | Mentions a funding round not in the row |
| Tone and spelling | AI | Gushing flattery; US spelling in a UK campaign |
| Relevance to offer | AI | Line about hiring for an analytics product pitch |

## Report format
```
# QA report: <table>, <date>
Rows: 4,812 | Pass: 4,590 (95.4%) | Fail: 222 (4.6%) | Threshold: 2% -> NO-GO
Top causes
1. Missing email (118 rows): provider waterfall skipped step 3 for .de domains
2. Placeholder in opener (61 rows): AI column ran before first_name was filled
3. Existing customers (24 rows): exclusion list outdated
4. Copy invents facts (19 rows): prompt asks for "recent news" with no news column
Fixes: <step, change, owner>
Examples: <3 failed rows per cause>
Recommendation: fix causes 1 and 2, refresh exclusions, re-run QA
```

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| No written spec | Draft one from the brief and workflow; get owner approval first |
| Very large tables | Code checks on all rows; AI checks on all rows with copy, in batches |
| Mixed languages | Spec per language; AI checks in the right language |
| Always-on workflow | Schedule QA daily on new rows; alert on threshold breaches |
| Borderline AI judgements | Mark "review" rather than pass or fail; a human decides |
| Sensitive or regulated targeting | Escalate to legal or compliance before sending |

## Handoffs to related skills
- ICP definition used in rules: the Product Marketing `ideal-customer-profile` skill
- CRM data hygiene: the CRM and Lifecycle `crm-data-hygiene` skill
- Lead scoring and routing: the CRM and Lifecycle `lead-scoring-routing` skill
- Cold email copy itself: the Content, Copy and PR `marketing-copywriting` skill
- Email security and deliverability: the CRM and Lifecycle `email-deliverability` skill

## Worked example
A growth team built a Clay table of 4,812 fintech contacts with a provider waterfall, an AI opener column and a push to their sequencer. Spot checks looked fine. Full QA found a 4.6% fail rate against a 2% threshold: German domains skipped a provider step, an AI column ran before first names were filled, 24 contacts were existing customers and 19 openers mentioned news that was not in the data. The team fixed the waterfall order and the column dependency, refreshed the exclusion list and changed the prompt to use only provided signals. The re-run passed at 0.8%, and the campaign launched without the errors reaching prospects.

## Common mistakes
- QA by scrolling a few rows.
- No written spec, so nobody agrees what "correct" means.
- Using AI for checks code can do exactly.
- Fixing rows by hand instead of fixing the step.
- Sending before the report says go.

## Self-check before you answer
- Was every row checked against a written spec?
- Are code checks and AI checks separated, with reasons for AI fails?
- Are failures grouped by cause with fixes?
- Is there a clear go or no-go against thresholds?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/gtm-workflow-qa/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
