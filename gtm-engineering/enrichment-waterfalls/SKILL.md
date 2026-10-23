---
name: enrichment-waterfalls
description: "Design enrichment waterfalls for emails, phones, contacts and company data: success definitions, provider benchmarks by region, ordering by cost per valid result, stop-on-success run conditions, email verification with catch-all policies, confidence fields, regional variants and monthly monitoring of match, bounce and cost. Use whenever someone sets up or tunes Clay enrichment, has low email match rates or high bounces, wants to cut provider costs, adds a data provider or enters a new region."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/enrichment-waterfalls/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-13"
---

# Enrichment Waterfalls

No single data provider finds every email, phone number or company detail. A waterfall tries providers one after another and stops when one returns a valid result, raising coverage while paying only for what is needed. Badly designed waterfalls do the opposite: they run the most expensive provider first, call every provider for every row, accept unverified emails, or ignore that providers perform differently by country and industry.

This skill designs and tunes enrichment waterfalls for emails, phone numbers, contacts and company data in Clay or similar tools: choosing providers per field and region, ordering by accuracy and cost, stopping rules, verification, confidence scoring, regional variants, testing on samples, monitoring match and bounce rates and documenting the logic.

## Operating principles
1. **Measure before ordering.** Test providers on your own sample, by region and segment.
2. **Cheapest accurate first.** Order by cost per valid result, not by price per lookup alone.
3. **Stop on success.** Each step runs only if earlier steps found nothing valid.
4. **Verify before use.** Emails go through verification; risky or catch-all results are flagged.
5. **Regions differ.** A provider strong in North America may be weak in Germany or Nigeria.

## Waterfall types
| Field | Typical steps | Verification |
|---|---|---|
| Work email | Provider A, B, C, pattern guess as last resort | Email verifier; flag catch-all |
| Mobile phone | Provider A, B | Format and country code checks |
| Contact discovery | People search by title and seniority, then fallback provider | Title and company match |
| Company firmographics | Primary provider, then website scrape | Domain match |
| Technographics | Tech detection provider, then site scan | Date of last detection |

## When to use, and when not to
Use it when setting up enrichment, when match or bounce rates are poor, when costs are high, when entering new regions or when adding a provider.

Don't use it for deciding who to target (`icp-account-scoring`) or for deliverability setup (`outbound-infrastructure`).

## Inputs
- Fields needed and how they will be used (email outreach, calls, scoring).
- Providers available, their costs and contract terms.
- A test sample of 200 to 500 rows representative of segments and regions.
- Current match, bounce and cost figures.
- Compliance requirements for data sources and regions.

## Workflow

### Step 1. Define success per field
For emails: verified valid, not catch-all unless accepted, matched to the right person and company.

### Step 2. Benchmark providers
Run each provider on the same sample. Record match rate, verified valid rate, cost per lookup and cost per valid result, by region.

### Step 3. Order the waterfall
Sort by cost per valid result within each region; put providers with unique coverage where they add most.

### Step 4. Add stop and run conditions
Each step runs only if previous steps returned nothing valid and the row still qualifies.

### Step 5. Verify
Run verification on every found email; mark valid, risky, catch-all or invalid; decide which statuses can be sent.

### Step 6. Add confidence
Combine provider, verification and match signals into a confidence field used by QA and sending rules.

### Step 7. Build regional variants
Where results differ, use separate orders for regions such as UK, DACH, North America and Africa.

### Step 8. Monitor
Track match rate, verified rate, bounce rate after sending and cost per valid result monthly; re-test providers quarterly.

## Benchmark table
```
| Provider | Region | Lookups | Found | Verified valid | Cost per lookup | Cost per valid email |
| A | UK | 200 | 128 | 112 | 1.0 | 1.79 |
| B | UK | 200 | 140 | 98 | 0.6 | 1.22 |
| C | UK | 200 | 90 | 85 | 1.5 | 3.53 |
```
In this example B goes first for the UK, then A, then C only for remaining rows.

## Verification statuses
| Status | Meaning | Default action |
|---|---|---|
| Valid | Mailbox confirmed | Send |
| Catch-all | Domain accepts all mail; mailbox unknown | Send only in small volumes or skip, by policy |
| Risky or unknown | Could not confirm | Hold or skip |
| Invalid | Will bounce | Never send |

## Cost logic
Cost per valid result = total spend on a step / number of valid results that step produced. A cheap provider with low accuracy can cost more per valid email than an expensive accurate one, once verification and bounces are counted.

## Phone waterfalls
Phone data is costlier and less reliable than email. Enrich phones only for top-tier accounts that sales will actually call, check formats and country codes, prefer direct dials over switchboards and track connect rates after calls to judge providers.

## Company data waterfalls
For firmographics, start with the cheapest reliable source, fall back to a second provider and use website scraping or AI research only for missing fields on qualified accounts. Record the source and date for each field so stale data can be refreshed.

## Bounce feedback loop
After sending, feed bounces back to the table: mark the provider and verification status that produced each bounced email. If one provider or status causes most bounces, demote or remove it. Keeping bounce rates low protects domain reputation as much as it saves money.

## Documenting the waterfall
Record each field's order, run conditions, verification rules, regional variants and the date of the last benchmark in the table spec, so anyone can explain and maintain the logic.

## Re-testing
Re-run the benchmark every quarter, after any provider pricing change and before entering a new region, because coverage and accuracy shift over time.

Keep a short change log of every reorder and why, so results can be compared over time.

Share benchmark results with sales operations so data quality expectations are clear.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Catch-all heavy segment | Use alternative signals (phone, LinkedIn) or small test sends |
| New region | Benchmark before scaling; consider regional providers |
| Provider changes pricing | Re-run the benchmark and reorder |
| Data protection limits | Check lawful basis and provider compliance; exclude restricted data |
| Personal emails returned | Exclude for B2B outreach unless policy allows |
| Very small volumes | One or two providers plus verification may be enough |

## Handoffs to related skills
- Table structure and run conditions: `clay-table-design`
- Cleaning outputs: `data-deduplication-normalisation`
- Sending safely: `outbound-infrastructure`
- QA before launch: `gtm-workflow-qa`
- Costs: `gtm-cost-control`
- Data hygiene in CRM: the CRM and Lifecycle `crm-data-hygiene` skill

## Worked example
A team's email waterfall ran its most expensive provider first for all regions and accepted unverified results; match rate in Germany was 58% and bounces reached 6%. A 400-row benchmark by region showed a cheaper provider led in the UK, a regional provider led in DACH and the expensive provider added unique coverage only as a third step. The new waterfall used regional orders, verified every email and held catch-all addresses. Match rate in DACH rose to 76%, bounce rate fell under 2% and cost per valid email dropped by about a third.

## Common mistakes
- Ordering by price per lookup instead of cost per valid result.
- Running every provider on every row.
- Sending unverified or catch-all emails at volume.
- One order for all regions.
- Never re-testing providers.

## Output format
```
1. Fields and success definitions
2. Provider benchmark by region
3. Waterfall order per field and region, with run conditions
4. Verification and confidence rules
5. Monitoring metrics and re-test schedule
```

## Self-check before you answer
- Were providers benchmarked on a representative sample?
- Is the order based on cost per valid result by region?
- Does each step stop on success?
- Are emails verified, with catch-all handled by policy?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/enrichment-waterfalls/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
