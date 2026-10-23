---
name: data-deduplication-normalisation
description: "Clean GTM data: normalisation rules for domains, company names, people, emails, countries, phones, titles, seniority, departments and industries, company matching on root domain, contact matching on email and LinkedIn, match confidence, survivor rules, CRM lookups before creating records and duplicate prevention. Use whenever someone has duplicate companies or contacts, messy job titles, inconsistent countries or phone formats, merges lists from several sources, prepares data for scoring or a CRM sync, or wants to stop duplicate outreach."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/data-deduplication-normalisation/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-13"
---

# Data Deduplication and Normalisation

Dirty data breaks GTM systems quietly. The same company appears as "Acme Ltd", "ACME" and "acme.co.uk"; one person has three records with different emails; job titles come in hundreds of spellings; countries are written as "UK", "United Kingdom" and "GB". The results are duplicate outreach, wrong routing, broken scoring, inflated reports and prospects contacted by two reps on the same day.

This skill cleans GTM data before and after enrichment: normalising domains, company names, people names, titles, seniority, departments, countries, phone numbers and industries; matching and merging duplicate companies and contacts with clear rules; checking against the CRM before creating records; and setting up prevention so duplicates do not return.

## Operating principles
1. **Normalise before matching.** Clean formats first, then compare.
2. **Domains are the best company key.** Names vary; root domains rarely do.
3. **Email plus name for people.** Use LinkedIn URLs or CRM IDs as stronger keys where available.
4. **Merge with rules, not guesses.** Decide which record and fields survive before merging.
5. **Prevent at the door.** Check the CRM before creating or pushing records.

## Normalisation rules
| Field | Rule | Example |
|---|---|---|
| Domain | Lowercase, remove protocol, www and paths, keep root domain | https://www.Acme.co.uk/about -> acme.co.uk |
| Company name | Trim, remove legal suffixes for matching (Ltd, Inc, GmbH), keep display version | ACME Ltd -> acme (match key) |
| Person name | Trim, proper case, separate first and last | jOHN smith -> John Smith |
| Email | Lowercase, trim | John.Smith@Acme.co.uk -> john.smith@acme.co.uk |
| Country | ISO standard name or code | UK, GB, Great Britain -> United Kingdom (GB) |
| Phone | E.164 format with country code | 07700 900123 -> +447700900123 |
| Job title | Keep original; add normalised role, seniority and department | "Sr. Mgr, Growth Mktg" -> Growth marketing, Manager, Marketing |
| Industry | Map to your own short list | "Financial technology" -> Fintech |
| LinkedIn URL | Lowercase, remove tracking parameters and trailing slashes | Standard profile URL |

## Title normalisation
| Seniority | Includes |
|---|---|
| C-level | CEO, CFO, CMO, COO, CTO, Chief |
| VP | VP, Vice President, SVP, EVP |
| Head or Director | Head of, Director, Senior Director |
| Manager | Manager, Lead, Team Lead |
| Individual contributor | Specialist, Analyst, Executive, Associate |

## When to use, and when not to
Use it before scoring, before CRM syncs, when merging lists from several sources, after enrichment, during CRM clean-ups and when reports look inflated.

Don't use it to decide CRM ownership rules (`crm-sync-routing`) or to clean marketing email lists for consent (the CRM and Lifecycle skills).

## Inputs
- The tables or CSV exports to clean.
- CRM exports of existing companies and contacts with IDs.
- Your industry list, title mapping and country standard.
- Merge rules agreed with sales operations.

## Workflow

### Step 1. Profile the data
Count rows, empty fields, distinct values per field and obvious duplicates.

### Step 2. Normalise fields
Apply the rules above into new normalised columns; keep originals.

### Step 3. Match companies
Exact match on root domain; then fuzzy match on normalised name plus country for rows without domains; review low-confidence matches.

### Step 4. Match contacts
Exact match on email; then LinkedIn URL; then normalised name plus company domain.

### Step 5. Decide survivors
Rules such as: keep the CRM record if it exists; keep the most recently verified email; keep rep-entered fields over enriched ones.

### Step 6. Merge or flag
Merge automatically only for high-confidence matches; flag the rest for review.

### Step 7. Check against the CRM
Before pushing, look up each record; update existing records instead of creating new ones.

### Step 8. Prevent recurrence
Normalise on entry, enforce unique keys, run a weekly duplicate report.

## Match confidence
| Match | Confidence | Action |
|---|---|---|
| Same root domain | High | Merge companies |
| Same email | High | Merge contacts |
| Same LinkedIn URL | High | Merge contacts |
| Same normalised name and country, no domain | Medium | Review |
| Similar name only | Low | Do not merge; flag |

## Fuzzy matching tips
- Compare normalised names with legal suffixes and punctuation removed.
- Require a second matching field (country, city or phone) for fuzzy company matches.
- Use similarity thresholds (for example 0.9 or higher) and review anything between 0.8 and 0.9.
- Never fuzzy-match people on name alone; common names collide.

## Merge field priority
| Field | Survivor rule |
|---|---|
| Owner | Existing CRM owner |
| Email | Most recently verified valid email |
| Title | Most recent source date |
| Phone | Rep-entered over enriched |
| Notes and activity | Combine; never delete history |
| Lifecycle stage | Furthest stage reached |

## Weekly duplicate report
List new duplicate pairs by type and source, the share of records created without a CRM lookup and the top sources of messy data. Fix the source workflow when one input keeps causing duplicates.

## Using an AI agent
The agent can profile data, write normalisation formulas or Python scripts, propose title mappings, run matching with confidence scores and prepare merge lists for review. Bulk merges in the CRM happen only after a backup and a human check of samples.

## Keeping originals
Always keep the original value beside each normalised field and record the source and date. When a mapping is wrong, originals make it easy to fix without re-buying data, and they show auditors exactly what changed and why. Store mapping tables, such as titles to seniority, in one shared place so every table uses the same rules.

Run the duplicate report before every large CRM push and after importing any new list, and fix the source of repeated problems rather than cleaning the same issues each month.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Group companies with many domains | Link subsidiaries to a parent account; do not merge |
| Shared generic domains (gmail.com) | Never match companies on them |
| Person moved company | New contact at new company; keep history linked |
| Country-specific domains of one brand | Decide account model: global parent or local accounts |
| Very large CRM clean-up | Back up first; work in batches; review samples |
| Records owned by different reps | Follow ownership rules before merging |

## Handoffs to related skills
- Table design: `clay-table-design`
- Waterfall outputs: `enrichment-waterfalls`
- CRM rules: `crm-sync-routing`
- QA: `gtm-workflow-qa`
- CRM hygiene programmes: the CRM and Lifecycle `crm-data-hygiene` skill

## Worked example
A team merged three lead sources into one table of 18,000 contacts. Profiling found 2,300 duplicate contacts, companies spelled up to five ways and 410 country variants. Normalisation, domain matching and email matching merged 1,950 duplicates automatically and flagged 350 for review. A CRM lookup found 1,100 contacts already in the CRM, which were updated instead of created. Title normalisation produced clean seniority and department fields for scoring. Duplicate outreach complaints stopped, and pipeline reports no longer double-counted accounts.

## Common mistakes
- Matching on company names instead of domains.
- Overwriting originals instead of adding normalised columns.
- Auto-merging low-confidence matches.
- Creating CRM records without checking for existing ones.
- Cleaning once and never preventing recurrence.

## Output format
```
1. Data profile
2. Normalisation rules applied
3. Match results by confidence
4. Survivor and merge rules
5. CRM lookup results (update versus create)
6. Prevention plan and weekly report
```

## Self-check before you answer
- Are fields normalised before matching, with originals kept?
- Are companies matched on root domain first?
- Are only high-confidence matches merged automatically?
- Is the CRM checked before creating records?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/data-deduplication-normalisation/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
