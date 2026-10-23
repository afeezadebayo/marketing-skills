---
name: clay-table-design
description: "Design Clay and similar GTM tables that are cheap, fast and debuggable: a table spec, one job per table, staged columns from input and cheap qualification to paid enrichment, scoring, signals, AI copy, QA and output, run conditions on every paid column, naming conventions, dependency order, sample tests and reusable templates. Use whenever someone builds or rebuilds a Clay table, wants to cut credits per row, fix a messy workflow, add run conditions, structure an outbound or enrichment table or turn a table into a reusable template."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/clay-table-design/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-13"
---

# Clay Table Design

Clay tables become hard to run when they grow without design: dozens of columns in no particular order, enrichment that runs on every row even when the row will be filtered out later, AI columns that fire before their inputs exist, hidden dependencies, and no way to tell which columns cost credits. The same patterns appear in any table-based GTM tool. A well-designed table is cheaper, faster, easier to debug and reusable by the next person.

This skill designs GTM tables for Clay or similar tools: a clear purpose and spec, a staged column layout (input, qualify, enrich, score, write, QA, output), filters and run conditions that stop paid steps on rows that will not qualify, naming conventions, dependency order, error handling, templates for reuse and a test plan on a small sample before full runs.

## Operating principles
1. **One table, one job.** A table builds a list, enriches it or writes copy, not everything at once.
2. **Qualify before you pay.** Cheap checks and filters run before expensive enrichment and AI.
3. **Left to right is the order of work.** Columns follow the flow of data.
4. **Every paid column has a run condition.** It only runs when its inputs exist and the row still qualifies.
5. **Test small, then scale.** Run 20 to 50 rows, check, then run the rest.

## Table stages
| Stage | Columns | Notes |
|---|---|---|
| 1. Input | Source data: company, domain, LinkedIn URL, list source | Normalise domains on entry |
| 2. Qualify (cheap) | Firmographic checks, exclusion lookups, country and size filters | Free or low-cost; drop non-ICP rows early |
| 3. Enrich (paid) | Contacts, emails, phone, technographics | Waterfalls with run conditions |
| 4. Score | Fit and intent score, tier | Formula columns |
| 5. Signals | Hiring, funding, tech changes, news | Only for qualified tiers |
| 6. Write | AI copy columns | Only for rows ready to send |
| 7. QA | Validation formulas, flags | Before any export |
| 8. Output | CRM push, sequencer push, export | Only rows that pass QA |

## Naming conventions
- Tables: `<team>-<purpose>-<segment>-<yyyy-mm>`, for example `sales-outbound-fintech-uk-2026-10`.
- Columns: prefix by stage, such as `in_domain`, `q_country_ok`, `en_email`, `sc_tier`, `sig_hiring`, `ai_opener`, `qa_status`, `out_crm_id`.
- Booleans start with `is_` or `has_`; scores end with `_score`.

## When to use, and when not to
Use it when building a new table, rebuilding a messy one, turning a one-off table into a template, or before scaling a workflow to many rows.

Don't use it to choose providers (`enrichment-waterfalls`) or write prompts (`ai-copy-columns`), though the table must leave room for both.

## Inputs
- Purpose of the table and the output it must produce.
- The spec or ICP rules (see `gtm-workflow-qa` for spec format).
- Data sources and providers available.
- Expected volume and credit budget.
- Where the output goes (CRM, sequencer, export).

## Workflow

### Step 1. Write the table spec
Purpose, input source, output, volume, owner, ICP and exclusion rules, fields required at the end, budget.

### Step 2. Design the column plan
List columns in stage order with type (input, formula, enrichment, AI, integration), cost and run condition.

### Step 3. Add cheap qualification first
Country, employee range, industry, exclusion lookups against customers and competitors, domain validity.

### Step 4. Gate every paid step
Run conditions such as "only if `q_icp_ok` is true and `en_email` is empty". Never let enrichment or AI run on rows that will be filtered out.

### Step 5. Order dependencies
A column that needs another column's output sits to its right and only runs when that value exists.

### Step 6. Handle errors
Fallback values, error flags and a `qa_status` column that records why a row failed.

### Step 7. Test on a sample
Run 20 to 50 representative rows across segments; check outputs, costs and errors; fix; repeat.

### Step 8. Scale and monitor
Run the full table in batches; watch credits, error rates and match rates.

### Step 9. Save as a template
Document purpose, columns and run conditions so the table can be duplicated for new segments.

## Column plan template
```
| # | Column | Stage | Type | Inputs | Run condition | Est. cost per row |
| 1 | in_domain | Input | Import | - | - | 0 |
| 2 | q_employees_ok | Qualify | Formula | employees | always | 0 |
| 3 | q_not_customer | Qualify | Lookup | in_domain | always | 0 |
| 4 | en_contacts | Enrich | Provider | in_domain | q_employees_ok AND q_not_customer | 1 credit |
| 5 | en_email | Enrich | Waterfall | name, domain | en_contacts found | 1 to 3 credits |
| 6 | sc_tier | Score | Formula | firmographics, signals | always | 0 |
| 7 | ai_opener | Write | AI | signals, role | sc_tier in [A,B] AND en_email valid | AI cost |
| 8 | qa_status | QA | Formula | all required | always | 0 |
| 9 | out_crm | Output | Integration | all | qa_status = pass | 0 |
```

## Run condition patterns
| Pattern | Purpose |
|---|---|
| Only if input exists | Avoid errors and wasted credits |
| Only if previous step found nothing | Waterfall logic |
| Only if qualified tier | Spend on the best rows |
| Only if not already in CRM | Avoid duplicates |
| Only if QA passed | Protect the CRM and sequencer |

## Debugging a table
When outputs look wrong, filter rows by `qa_status`, check the first column where values go missing, compare a failing row with a passing one and look at run conditions and input formats. Most problems come from a dependency running too early, an unexpected input format or a provider returning a different field name.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Very large lists | Split by segment into several tables; run in batches |
| Shared workspace | Folders and naming by team; one owner per table |
| Inherited messy table | Duplicate, rebuild with stages, compare outputs, then archive the old one |
| Columns hidden by others | Document hidden columns in the spec |
| Real-time triggers | Separate trigger tables from bulk list tables |
| Tool limits on rows or runs | Batch and archive processed rows |

## Handoffs to related skills
- Audit first: `gtm-engineering-audit`
- Provider order: `enrichment-waterfalls`
- Scoring formulas: `icp-account-scoring`
- AI columns: `ai-copy-columns`
- Cleaning: `data-deduplication-normalisation`
- Pre-launch checks: `gtm-workflow-qa`
- Costs: `gtm-cost-control`
- Documentation: `gtm-workflow-documentation`

## Worked example
A team's outbound table had 74 columns, enriched every imported company and ran an AI opener on every row, using about 9 credits per row even though only a third qualified. The redesign split it into a list-building table and an outreach table, added free qualification filters first, put run conditions on every paid column, moved AI copy to the end for tier A and B rows only and added a QA status column. After a 40-row test and two fixes, the full run used about 3.5 credits per row and produced the same number of qualified contacts.

## Common mistakes
- Enriching rows before qualifying them.
- AI columns that run before their inputs exist.
- No naming convention, so nobody can follow the table.
- Running thousands of rows without a sample test.
- One giant table doing every job.

## Output format
```
1. Table spec
2. Column plan with stages, types, run conditions and costs
3. Naming conventions
4. Test plan and results
5. Template notes for reuse
```

## Self-check before you answer
- Do cheap qualification steps run before paid ones?
- Does every paid column have a run condition?
- Are dependencies ordered left to right?
- Was a small sample tested before the full run?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/clay-table-design/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
