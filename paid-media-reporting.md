---
name: paid-media-reporting
description: "Build paid media reporting leadership trusts: business truth from finance and commerce first, blended MER and new-customer CAC, contribution margin and payback, labelled platform attribution never summed across platforms, analytics, incrementality factors from lift and geo tests, MMM inputs, cohorts, naming and UTM conventions, and weekly and monthly reports that end in decisions. Use whenever someone asks about marketing attribution, ROAS reporting, MER, blended CAC, why platform numbers exceed sales, paid media dashboards, leadership marketing reports or incrementality-adjusted reporting."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/paid-media-reporting/
  category: marketing
  subcategory: performance-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Paid Media Reporting and Attribution

Paid media reports often add up platform claims: Google says it drove this much revenue, Meta says it drove that much, TikTok claims more, and the total exceeds what the business sold. Leadership either over-invests in whoever claims most or stops trusting marketing numbers. Since the end of most Privacy Sandbox APIs in October 2025 and with consent rules limiting tracking, no single attribution model sees the full picture.

This skill builds paid media reporting that holds up: platform numbers labelled for what they are, blended business metrics, new-customer and margin views, incrementality factors from tests, MMM inputs, and a weekly and monthly cadence that leads to decisions.

## Operating principles
1. **Start with business truth.** Revenue, orders, new customers and margin from your own systems.
2. **Label every platform number** with its attribution window and model.
3. **Never sum platform-attributed conversions** across platforms as a total.
4. **Triangulate:** platform attribution, analytics, incrementality tests and MMM each answer part of the question.
5. **Report decisions, not just data.** Every report ends with what changes next.

## The measurement stack
| Layer | Source | Answers | Limits |
|---|---|---|---|
| Business truth | Finance, commerce, CRM | What actually happened | No channel split |
| Blended metrics | Truth ÷ total spend | Overall efficiency (MER, blended CAC) | No channel split |
| Platform attribution | Google Ads, Meta, TikTok | Directional channel and campaign performance | Self-reported; overlapping credit |
| Analytics attribution | GA4 or similar | Cross-channel view on site | Consent and cookie gaps; last-click bias |
| Incrementality tests | Lift and geo tests | Causal value per channel | Point-in-time; needs volume |
| MMM | Weekly aggregated data | Channel contribution and response curves | Needs history; refreshed periodically |

## When to use, and when not to
Use it to build or fix paid media dashboards, prepare leadership reports, reconcile platforms with finance, set weekly operating metrics and decide how to read conflicting numbers.

Don't use it to design tests (`incrementality-testing`) or models (`marketing-mix-modelling`) in depth.

## Inputs to ask for, in one message
1. Revenue, orders, new customers and margins by day or week from your systems.
2. Spend and platform-reported results by channel and campaign.
3. GA4 or analytics setup and UTM conventions.
4. Incrementality test results and MMM outputs, if any.
5. Who reads which report and what decisions they make.

## Workflow

### Step 1. Define the metric dictionary
MER, blended CAC, new-customer CAC, contribution margin after ads, payback, platform ROAS (with window), incremental ROAS, each with formula, source and owner.

### Step 2. Fix tagging
Consistent UTMs on every ad; offline conversion IDs; consistent naming for campaigns so reports can group by channel, objective and audience.

### Step 3. Reconcile
Compare platform totals with analytics and finance; document why they differ.

### Step 4. Apply incrementality factors
From tests: incremental conversions ÷ platform conversions per channel; use them to adjust platform numbers in planning views, and show both.

### Step 5. Build reports by audience
Weekly operating dashboard for the paid team (spend pacing, CPA and ROAS by campaign with windows, creative performance, anomalies). Monthly leadership report (blended metrics, new customers, margin, incrementality-adjusted channel view, decisions).

### Step 6. Add cohorts and payback
New-customer cohorts by acquisition month and channel: 30, 60, 90 and 180-day revenue and margin, payback month.

### Step 7. Review
Weekly anomalies and pacing; monthly allocation decisions; quarterly calibration with new tests and MMM.

## Leadership report template
```
# Paid media report: <month>
## Summary (3 sentences)
## Business outcomes: revenue, new customers, contribution margin after ads, MER, blended CAC
## Channel view: spend, platform-reported (labelled), incrementality-adjusted, trend
## New-customer cohorts and payback
## Tests completed and what they changed
## Decisions and next month's plan
```

## Naming convention example
`channel_objective_audience_geo_detail` such as `meta_prospecting_broad_uk_ugc-q4` or `google_search_nonbrand_core_us`. Consistent names let reports group spend and results by channel, objective and audience without manual mapping.

## Weekly operating checks
| Check | Look for |
|---|---|
| Spend pacing vs plan | Over- or under-delivery by channel |
| Blended MER and new-customer CAC | Changes beyond normal range |
| Platform CPA and ROAS by campaign (labelled) | Sudden shifts after changes |
| Conversion volume vs orders in your system | Tracking breaks |
| Creative fatigue signals | Rising frequency, falling CTR |
| Budget-limited campaigns | Missed scale opportunities |

## Incrementality-adjusted channel view
| Channel | Platform-reported conversions | Incrementality factor (latest test) | Adjusted conversions | Spend | Adjusted CAC |
|---|---|---|---|---|---|
| Meta prospecting | 1,000 | 0.8 | 800 | £40,000 | £50 |
| Meta retargeting | 600 | 0.2 | 120 | £12,000 | £100 |
| Brand search | 900 | 0.3 | 270 | £8,000 | £30 |
Illustrative numbers; show the test date and confidence beside each factor, and refresh after new tests.

## Reading conflicting numbers
| Conflict | Likely reason | How to report it |
|---|---|---|
| Meta reports more purchases than GA4 | View-through credit, cross-device, consent gaps in GA4 | Show both, labelled; use tests to decide |
| Google Ads exceeds GA4 for search | Different windows, modelled conversions | Align windows where possible; note modelling |
| All platforms together exceed orders | Overlapping credit | Report business truth; never sum platforms |
| GA4 last click undervalues video | Last-click bias | Use lift tests and MMM for upper funnel |

## Cohort payback view
| Acquisition month | Channel | New customers | CAC | 30d margin | 90d margin | 180d margin | Payback month |
|---|---|---|---|---|---|---|---|
| 2026-06 | Meta prospecting | 820 | £52 | £21 | £44 | £61 | Month 4 |
| 2026-06 | Google non-brand | 410 | £71 | £30 | £52 | £74 | Month 5 |
Illustrative; build from your commerce or CRM data, not platform data.

## Metric definitions to agree
- **MER:** total revenue ÷ total marketing spend (state which revenue and which spend).
- **Blended CAC:** total marketing spend ÷ new customers.
- **New-customer CAC by channel:** channel spend ÷ new customers attributed by your chosen method (label it).
- **Contribution margin after ads:** revenue minus cost of goods, fees, shipping, returns and ad spend.
- **Payback period:** months until cumulative margin from a cohort exceeds its CAC.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Platform totals exceed actual sales | Show business truth first; present platform numbers as directional only |
| No tests yet | Use blended metrics for decisions and plan the first test |
| B2B long cycles | Report pipeline by source and cohort; avoid month-end revenue attribution |
| Offline or phone sales | Include them through offline imports and finance data |
| Agency reporting | Require reconciliation with your own data in every report |

## Handoffs to related skills
- Tracking and UTMs: `conversion-tracking-capi`
- Incrementality factors: `incrementality-testing`
- MMM outputs: `marketing-mix-modelling`
- Budget decisions: `media-planning-budgeting`
- Account issues found in reports: `paid-media-audit`

## Worked example
A DTC apparel brand's monthly report summed Google, Meta and TikTok attributed revenue to a figure well above actual online sales. The new reporting led with business truth and blended MER, added new-customer CAC from the commerce platform, labelled each platform's attribution window, applied incrementality factors from two geo tests (retargeting low, prospecting video higher than claimed) and added 90-day cohort payback by channel. Leadership approved moving budget from retargeting to prospecting video, and blended MER improved the following quarter.

## Output format
```
# Paid media reporting plan: <business>, <date>
## Metric dictionary
## Tagging and naming conventions
## Reconciliation findings
## Incrementality factors by channel
## Weekly and monthly report designs
## Cohort and payback views
## Review cadence and owners
```

## Common mistakes
- Summing platform-attributed revenue.
- Unlabelled attribution windows.
- Reporting ROAS without margin or new-customer context.
- No link between test results and reporting.
- Reports with no decisions.

## Questions to ask before you build
- Which revenue figure does finance treat as the record?
- Which decisions will this report inform, and how often?
- What incrementality evidence exists by channel?

## Self-check before you answer
- Does the report start with business truth and blended metrics?
- Are platform numbers labelled and never summed?
- Are incrementality factors and cohorts included?
- Does every report end with decisions?

## Official documentation
- GA4 attribution settings: https://support.google.com/analytics/answer/10596866
- GA4 campaign URL builder and UTMs: https://support.google.com/analytics/answer/10917952
- Google Meridian: https://developers.google.com/meridian

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/paid-media-reporting/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
