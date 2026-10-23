---
name: growth-model
description: "Build cohort-based growth models and forecasts: new users by channel, activation, retention curves, monetisation, expansion, referral and reactivation, calibrated on history, a baseline projection, sensitivity analysis to rank levers, conservative, expected and stretch scenarios tied to initiatives, input targets with owners and monthly actuals versus forecast. Use whenever someone asks for a growth model, growth forecast, what it takes to hit a target, which growth lever matters most, cohort-based revenue forecasts or planning growth for a quarter or year."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/growth-model/
  category: marketing
  subcategory: growth-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Growth Model and Forecasting

A growth model is a simple, explicit description of how a business grows: which inputs (new users by channel, activation, retention, monetisation, referral) combine to produce the outcome, and by how much. It turns "we need to grow 50%" into "we need activation from 22% to 30% and two new channels at this scale", and shows which lever moves the outcome most. Most companies set targets top-down and hope; a model makes targets traceable and trade-offs visible.

This skill builds growth models in a spreadsheet or notebook, calibrates them with historical data, runs sensitivity analysis to find the levers that matter, and produces forecasts with scenarios that teams can own.

## Operating principles
1. **Simple enough to explain.** A model the team understands beats a perfect one nobody trusts.
2. **Cohort-based.** New users join in cohorts and decay over time; growth stacks cohorts on top of each other.
3. **Calibrated on history.** Every assumption comes from your data or is labelled as an assumption.
4. **Sensitivity before targets.** Find which input changes the outcome most before assigning goals.
5. **Living document.** Update monthly with actuals and adjust assumptions.

## Model building blocks
| Block | Typical formula | Data source |
|---|---|---|
| New users | Sum of channel volumes (paid, organic, referral, partnerships) | Analytics, attribution, ad platforms |
| Activation | New users × activation rate | Product analytics |
| Retention | Activated users × retention curve by month since start | Cohort analysis |
| Monetisation | Active users × paid conversion × ARPU (or orders × AOV) | Billing, commerce |
| Expansion and contraction | Existing revenue × net expansion rate | Billing |
| Referral or loop | Active users × invite rate × invite conversion | Product analytics |
| Reactivation | Lapsed users × reactivation rate | Lifecycle data |

## When to use, and when not to
Use it for annual and quarterly planning, setting input targets, deciding between growth investments, fundraising forecasts, and when leadership asks what it would take to hit a goal.

Don't use it for detailed media budget allocation (use the Performance Marketing `media-planning-budgeting` skill) or financial statements beyond growth drivers.

## Inputs to ask for, in one message
1. Monthly new users or customers by channel for 12 to 24 months.
2. Activation rate by cohort and channel.
3. Cohort retention curves (users and revenue).
4. Monetisation: conversion to paid, ARPU or AOV, expansion.
5. Referral or invite data if any.
6. Planned initiatives and their expected effects (to label as assumptions).
7. The target and time frame.

## Workflow

### Step 1. Choose the shape
SaaS: users or accounts, activation, retention, conversion, ARPU, expansion. E-commerce: new customers, repeat purchase curves, AOV. Marketplace: supply and demand sides with liquidity. Consumer app: installs, activation, retention, monetisation, virality.

### Step 2. Calibrate on history
Build the model for the past 12 months and compare predicted with actual outcomes month by month. Adjust until it fits reasonably.

### Step 3. Project the baseline
If nothing changes, where does the outcome land? This is the honest starting point for targets.

### Step 4. Run sensitivity analysis
Change each input by a realistic amount (for example +10% relative) and record the effect on the outcome after 12 months. Rank inputs by impact.

### Step 5. Build scenarios
Conservative, expected and stretch, each a set of input assumptions tied to named initiatives, with evidence labels.

### Step 6. Set input targets
Give each team a target for the input they own, consistent with the expected scenario.

### Step 7. Track actuals
Monthly: actual inputs versus assumptions; update the forecast.

## Sensitivity example (12-month impact on revenue)
| Input | Change | Revenue impact |
|---|---|---|
| Month-3 retention | +10% relative | Largest (compounds across cohorts) |
| Activation rate | +10% relative | Large |
| Paid conversion | +10% relative | Medium |
| New users (paid) | +10% | Medium, with rising cost |
| Invite rate | +10% | Small now, grows if loop strengthens |
Illustrative ranking; retention often matters most because it compounds.

## Spreadsheet structure
```
Tab 1: Assumptions (each with source and evidence label)
Tab 2: Cohorts (rows = sign-up month, columns = months since sign-up)
Tab 3: Channels (volumes and costs by month)
Tab 4: Outputs (active users, paying customers, revenue, CAC, payback)
Tab 5: Scenarios and sensitivity
Tab 6: Actuals vs forecast
```

## How cohorts stack into growth
| Sign-up month | Month 0 | Month 1 | Month 2 | Month 3 |
|---|---|---|---|---|
| Jan cohort (1,000 activated) | 1,000 | 620 | 510 | 470 |
| Feb cohort (1,100 activated) | | 1,100 | 680 | 560 |
| Mar cohort (1,200 activated) | | | 1,200 | 740 |
| Total active | 1,000 | 1,720 | 2,390 | 1,770 + Apr cohort |
Each month's active base is the sum of every cohort still active. Improving retention lifts every column at once, which is why it usually beats acquisition in sensitivity tests.

## Assumption register
| Assumption | Value | Source | Evidence label | Owner | Review date |
|---|---|---|---|---|---|
| Activation rate | 24% → 30% | Last 6 months 22-25%; onboarding test planned | Assumption (test pending) | Growth PM | Monthly |
| Month-3 retention | 47% | Cohort data Jan-Jun | Data | Analyst | Monthly |
| New channel volume | 400 users/month | Pilot results | Test (small) | Acquisition lead | After 8 weeks |

## Forecast accuracy check
Each month, compare forecast and actual for the outcome and each input. Track the error. If one input is consistently wrong, fix that assumption rather than adjusting everything. A model that is within about 10% on the outcome after three months is usually good enough to plan with.

## Communicating the model
- Lead with the baseline ("if nothing changes") before showing targets.
- Show which assumptions drive the gap between baseline and goal.
- Name the initiatives behind each assumption and who owns them.
- Present ranges, not single numbers, for the stretch scenario.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Little history (new product) | Use benchmarks from similar products, labelled; update monthly |
| Big seasonality | Model seasonal indices per month |
| Pricing change planned | Model before and after separately; watch conversion and churn |
| Marketplace | Model supply, demand and match rates; liquidity is usually the constraint |
| Investors want aggressive numbers | Show the stretch scenario with the assumptions it requires |

## Handoffs to related skills
- Metric tree and inputs: `north-star-metric-tree`
- Retention curves: `cohort-retention-analysis`
- Funnel rates: `funnel-analysis`
- Channel volumes: `acquisition-channel-testing`
- Loop contributions: `growth-loops`
- Reporting actuals: `growth-reporting`

## Worked example
A subscription fitness app wanted to double revenue in 12 months. The calibrated model showed the baseline reaching about 1.4 times current revenue. Sensitivity analysis found month-3 retention was the strongest lever, followed by trial-to-paid conversion; doubling paid acquisition alone would add less and raise CAC. The expected scenario combined a retention initiative (personalised plans after week two), a trial conversion experiment programme and one new channel, each with input targets and owners. Monthly tracking showed retention improving faster than conversion, and the forecast was updated to reflect it.

## Output format
```
# Growth model: <company>, <date>
## Model shape and assumptions (with sources and labels)
## Calibration against history
## Baseline projection
## Sensitivity ranking
## Scenarios (conservative, expected, stretch) with initiatives
## Input targets and owners
## Tracking plan for actuals
```

## Common mistakes
- Top-down targets with no link to inputs.
- Ignoring cohort decay, so forecasts overshoot.
- Unlabelled assumptions presented as facts.
- Treating acquisition as the only lever.
- Never updating the model with actuals.

## Questions to ask before you model
- What outcome and time frame does the model need to answer?
- Which inputs have reliable history?
- Which initiatives are planned, and what evidence supports their expected effect?

## Self-check before you answer
- Is the model cohort-based and calibrated on history?
- Is every assumption sourced or labelled?
- Did I run sensitivity before setting targets?
- Are input targets owned and tracked monthly?

## Further reading
- Reforge, growth models: https://www.reforge.com/blog
- a16z, consumer metrics and growth: https://a16z.com/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/growth-model/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
