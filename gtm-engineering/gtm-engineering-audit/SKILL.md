---
name: gtm-engineering-audit
description: "Audit a GTM engineering stack end to end: ICP, providers, Clay tables and workflows, enrichment, scoring, signals, AI copy, data quality, CRM and sequencer sync, sending infrastructure, QA, costs, documentation and reporting, with a funnel from source to revenue, unit costs, a 0 to 3 scorecard, a 90-day plan and governance rules. Use whenever someone inherits or reviews a Clay or GTM automation setup, wants to scale outbound, sees reply rates or match rates drop, has rising credit or provider costs, or asks where their GTM system is leaking."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/gtm-engineering-audit/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-13"
  updated: "2026-10-13"
---

# GTM Engineering Audit

GTM engineering stacks grow by accident. A Clay workspace fills with tables nobody owns, three providers enrich the same field, AI columns run on every row whether needed or not, CRM fields multiply, sequences send from mailboxes with no warm-up plan, and nobody can say what a qualified meeting actually costs. Problems stay hidden until reply rates fall, domains get flagged or the credit bill arrives.

This skill audits a go-to-market engineering setup end to end: goals and ICP, data sources and providers, Clay (or similar) tables and workflows, enrichment logic, scoring, signals, AI copy, data quality, CRM and sequencer sync, sending infrastructure, QA, costs, documentation and reporting. It scores each area, finds the leaks that cost the most pipeline or money, and builds a prioritised plan that hands each fix to a specialist skill. It is the entry point for the GTM Engineering set.

## Operating principles
1. **Start from pipeline, not tools.** Measure what the system produces: qualified accounts, meetings, opportunities and revenue.
2. **Map the whole flow.** Leaks hide in the handoffs between tools.
3. **Unit economics matter.** Cost per enriched contact, per qualified account and per meeting decides what scales.
4. **Quality before volume.** More rows with bad data or weak copy burn domains and reputation.
5. **Own and document everything.** Every table, provider and field has an owner and a purpose.

## Audit areas
| Area | What to check | Typical finding |
|---|---|---|
| 1. Goals and ICP | Written ICP, segments, targets per segment | ICP lives in someone's head |
| 2. Data sources | Providers, coverage, cost, contracts | Three providers for the same email field |
| 3. Tables and workflows | Structure, naming, owners, run logic | 60 tables, 12 in use, no naming convention |
| 4. Enrichment | Waterfall order, match rates, accuracy | Most expensive provider runs first |
| 5. Scoring | Fit and intent scoring rules | Every account scored "high" |
| 6. Signals | Which triggers are tracked and used | Hiring signals collected but never used |
| 7. AI copy | Prompts, inputs, review, results | Generic openers; invented facts |
| 8. Data quality | Duplicates, formats, normalisation | Same company three times with different names |
| 9. CRM and sequencer sync | Mapping, ownership, routing, overwrites | Enrichment overwrites rep-entered data |
| 10. Sending infrastructure | Domains, mailboxes, authentication, volumes | Sending from the main domain at high volume |
| 11. QA | Specs, checks before launch | Spot checks only |
| 12. Costs | Credits, provider fees, cost per result | No idea of cost per meeting |
| 13. Documentation | Specs, runbooks, handovers | One person knows how it works |
| 14. Reporting | Funnel from list to revenue | Only send volume and opens tracked |

## When to use, and when not to
Use it when taking over a GTM stack, before scaling outbound, when results drop, when costs spike, after a new hire inherits workflows, or once a quarter.

Don't use it for paid media or SEO audits (other Marketing skills) or for a single table's pre-launch check (`gtm-workflow-qa`).

## Inputs to ask for, in one message
1. Revenue goals, ICP and target segments.
2. Tools: Clay or similar, data providers, CRM, sequencer, email infrastructure.
3. List of active tables and workflows with owners.
4. Last 90 days of results: rows processed, sends, replies, meetings, opportunities.
5. Monthly costs by tool and provider, including credits used.
6. Known problems and recent changes.

## Workflow

### Step 1. Map the flow
Draw the path from source to revenue: list building, enrichment, scoring, signals, copy, QA, CRM, sequencer, sending, replies, meetings, pipeline.

### Step 2. Inventory assets
Tables, workflows, providers, AI columns, CRM fields, sequences, domains and mailboxes, each with owner, purpose and last run.

### Step 3. Measure the funnel
Rows sourced, enriched (match rate), qualified (by score), sent, delivered, replied (positive replies), meetings, opportunities, revenue, by segment.

### Step 4. Calculate unit costs
Cost per enriched contact, per qualified account, per positive reply and per meeting.

### Step 5. Score each area 0 to 3
With one line of evidence each.

### Step 6. Find the biggest leaks
Rank by pipeline or cost impact: for example low match rates in a key region, poor deliverability, weak copy, unqualified accounts reaching sequences.

### Step 7. Build the 90-day plan
Top fixes with owner, skill, metric and date; quick wins first.

### Step 8. Set governance
Naming conventions, ownership, change process, QA before launch and a monthly review.

## Funnel template
```
| Stage | Volume | Rate | Cost | Benchmark or target | Problem |
| Accounts sourced | 12,000 | - | £180 | - | - |
| Contacts enriched with valid email | 7,400 | 62% | £1,950 | 75% | Low match in DACH |
| Qualified by score | 3,100 | 42% | - | - | Scoring too loose |
| Sent | 3,100 | - | - | - | - |
| Positive replies | 46 | 1.5% | - | 2%+ | Generic copy |
| Meetings | 22 | 48% of positive | - | - | - |
| Cost per meeting | | | £110 | <£80 | - |
```

## Scorecard template
```
| Area | Score (0-3) | Evidence | Fix | Skill | Owner |
| Enrichment | 1 | Most expensive provider first; 62% match | Reorder waterfall, add regional provider | enrichment-waterfalls | |
| Infrastructure | 0 | Sending 400/day from main domain | Secondary domains, warm-up, limits | outbound-infrastructure | |
```

## Governance basics
- Naming: `<team>-<purpose>-<segment>-<yyyy-mm>` for tables and workflows.
- Every table has an owner, a spec and a status (active, paused, archived).
- Changes to live workflows go through a short checklist and QA.
- Archive unused tables monthly; document what each provider is for.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| No historical data | Start tracking now; audit structure and costs first |
| One builder, no documentation | Prioritise documentation and handover before scaling |
| Several teams in one workspace | Folders, naming and ownership by team |
| Very small volume | Focus on ICP, copy and infrastructure; skip complex automation |
| Regulated markets | Add legal review of data sources and outreach rules |
| Sudden drop in replies | Check infrastructure and deliverability first |

## Handoffs to specialist skills
- Table structure: `clay-table-design`
- Provider logic: `enrichment-waterfalls`
- Scoring: `icp-account-scoring`
- Triggers: `signal-based-outbound`
- AI personalisation: `ai-copy-columns`
- Data cleaning: `data-deduplication-normalisation`
- CRM and sequencer: `crm-sync-routing`
- Sending setup: `outbound-infrastructure`
- Pre-launch checks: `gtm-workflow-qa`
- Costs: `gtm-cost-control`
- Specs and runbooks: `gtm-workflow-documentation`
- Results: `gtm-reporting`

## Worked example
A B2B SaaS team ran outbound through 58 Clay tables built by one person who had left. The audit found 14 tables in use, three providers enriching emails with the most expensive first, a 62% match rate in Germany, every account scored "high", generic AI openers, enrichment overwriting rep notes in the CRM and 400 emails a day from the main domain. Cost per meeting was about £110. The 90-day plan reordered the waterfall and added a regional provider, rebuilt scoring with three tiers, moved sending to warmed secondary domains, rewrote AI prompts with real signals, protected rep-owned CRM fields and introduced specs, QA and naming. After a quarter, match rate rose to 78%, positive reply rate doubled and cost per meeting fell below £70.

## Common mistakes
- Measuring sends and opens instead of meetings and pipeline.
- Adding providers without measuring match rates and cost.
- No owner or documentation for tables.
- Scaling volume before fixing infrastructure and copy.
- No QA before launches.

## Output format
```
# GTM engineering audit: <company>, <date>
## Summary: biggest leaks and first moves
## Flow map
## Asset inventory
## Funnel and unit costs
## Scorecard
## 90-day plan
## Governance rules
```

## Self-check before you answer
- Is the funnel measured from source to revenue?
- Are unit costs calculated?
- Is every area scored with evidence?
- Does each fix have a skill, owner, metric and date?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/gtm-engineering-audit/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
