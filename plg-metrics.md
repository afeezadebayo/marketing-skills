---
name: plg-metrics
description: "Measure product-led growth from sign-up to net revenue retention: a metric tree, shared definitions for activation, time to value, habit, team formation, free-to-paid conversion, revenue per sign-up, expansion and PQL conversion, cohort and segment views, self-serve versus sales-assisted reporting, careful benchmarks, dashboards and decision-led reviews. Use whenever someone asks about PLG metrics, product-led growth KPIs, activation rate, free-to-paid conversion, revenue per sign-up, PLG dashboards, cohort analysis for self-serve or diagnosing why sign-ups grow but revenue does not."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/plg-metrics/
  category: marketing
  subcategory: product-led-growth
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# PLG Metrics and Reporting

Product-led businesses live or die by what happens inside the product, yet many still report sign-ups and revenue and little in between. Without activation, habit, team formation, conversion, expansion and retention metrics, teams can't tell whether growth problems come from acquisition, onboarding, the free model or sales assist. Good PLG reporting connects product behaviour to revenue, by cohort and segment, with a small set of metrics everyone agrees on.

This skill builds PLG metrics and reporting: the metric tree from sign-up to net revenue retention, definitions, cohort analysis, product-qualified account tracking, self-serve versus sales-assisted views, benchmarks used carefully, dashboards, review rhythms and decisions.

## Operating principles
1. **Measure the journey, not just the ends.** Activation, habit, team and conversion matter as much as sign-ups and revenue.
2. **Cohorts beat totals.** Compare groups who signed up in the same period.
3. **Accounts and users both matter.** B2B PLG needs account-level views alongside users.
4. **One definition per metric.** Shared definitions end debates between teams.
5. **Every review ends in a decision.** Metrics exist to change what teams do.

## Core PLG metrics
| Stage | Metric | Definition (example) |
|---|---|---|
| Acquisition | Sign-ups | New accounts created |
| Activation | Activation rate | Sign-ups reaching the value moment within 7 days |
| Time to value | Median time to activation | Hours or days from sign-up |
| Habit | Week-4 retention | Activated users active in week 4 |
| Team | Team formation rate | Accounts with 2+ active users within 30 days |
| Conversion | Free-to-paid or trial-to-paid rate | Accounts paying within 30, 60 or 90 days |
| Monetisation | Revenue per sign-up | Revenue from a cohort divided by its sign-ups |
| Expansion | Expansion rate | Paying accounts that add seats or upgrade |
| Retention | Logo and revenue retention | Accounts and revenue kept over time |
| Overall | Net revenue retention | Revenue from a cohort a year later, including expansion and churn |
| Sales assist | PQL conversion | PQL accounts converting to paid |
| Efficiency | CAC payback | Months to recover acquisition cost |

## When to use, and when not to
Use it when setting up PLG dashboards, preparing board updates, diagnosing growth slowdowns, comparing self-serve and sales-assisted revenue and aligning product and go-to-market teams.

Don't use it for detailed tracking plans (the Growth Marketing `tracking-plan` skill) or company-wide growth reporting beyond PLG (the Growth Marketing `growth-reporting` skill).

## Inputs to ask for, in one message
1. Product analytics, billing and CRM data access.
2. Current definitions of activation, active users and conversion.
3. Plans, free model and sales assist thresholds.
4. Cohort data for at least 6 to 12 months.
5. Stakeholders and decisions they make.
6. Existing dashboards.

## Workflow

### Step 1. Build the metric tree
From sign-ups to net revenue retention, showing how each stage feeds the next.

### Step 2. Agree definitions
Write them down: events, time windows, user versus account level.

### Step 3. Check data quality
Event tracking, identity across devices, account mapping between product, billing and CRM.

### Step 4. Build cohort views
Monthly sign-up cohorts by activation, conversion and retention; segments by source, plan, company size and region.

### Step 5. Separate motions
Self-serve versus sales-assisted conversion, deal size and retention.

### Step 6. Build dashboards
A one-page PLG overview, plus stage-specific views for teams.

### Step 7. Use benchmarks carefully
Compare to your own history first; external benchmarks vary widely by product and definition.

### Step 8. Set review rhythm
Weekly team metrics, monthly PLG review, quarterly board view.

### Step 9. Decide
Each review names the stage to focus on next and the experiments or fixes planned.

## PLG overview dashboard
```
| Metric | This month | Last month | Same month last year | Target | Note |
| Sign-ups | | | | | |
| Activation rate | | | | | |
| Median time to value | | | | | |
| Week-4 retention | | | | | |
| Team formation rate | | | | | |
| Free-to-paid (90 days) | | | | | |
| Revenue per sign-up | | | | | |
| Net revenue retention | | | | | |
| PQL conversion | | | | | |
```

## Diagnosing a slowdown
| Pattern | Likely stage | Next step |
|---|---|---|
| Sign-ups up, revenue flat | Activation or conversion | Check activation and limits by cohort |
| Activation stable, conversion falling | Free model or upgrade prompts | Review limits and prompts |
| Conversion stable, revenue retention falling | Retention or expansion | Cohort retention and feature adoption |
| Self-serve strong, large accounts stuck | Sales assist | PQL coverage and plays |

## Cohort table example
| Sign-up month | Sign-ups | Activated (7 days) | Week-4 retained | Paid by day 90 | Revenue per sign-up |
|---|---|---|---|---|---|
| January | 4,200 | 38% | 21% | 4.1% | \u00a311.40 |
| February | 4,900 | 37% | 20% | 3.6% | \u00a39.80 |
| March | 6,100 | 39% | 21% | 3.2% | \u00a38.70 |
Illustrative; here activation holds steady while conversion falls, pointing at the free model or upgrade prompts rather than onboarding.

## Account versus user metrics
| Question | User-level metric | Account-level metric |
|---|---|---|
| Are people getting value? | Activation, weekly active users | Accounts with activated users |
| Is usage spreading? | Invites sent | Active users per account, team formation rate |
| Is revenue growing? | Upgrades by users | Paid accounts, seats, expansion, net revenue retention |

## Decision log
Record each review's decision, the metric it targets, the owner and the date to check results. Over time the log shows which changes moved PLG metrics and stops teams repeating failed ideas.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Activation definition changes | Restate past cohorts or mark the break clearly |
| Free users with no account mapping | Improve identity and domain mapping |
| Long conversion cycles | Use 90 or 180-day windows and leading indicators |
| Seasonality | Compare cohorts year on year |
| Several products | Separate funnels with a shared account view |

## Handoffs to related skills
- Audit: `plg-audit`
- Strategy and value moment: `plg-strategy`
- PQLs: `product-qualified-leads`
- Tracking plans: the Growth Marketing `tracking-plan` skill
- Cohort analysis: the Growth Marketing `cohort-retention-analysis` skill
- Company reporting: the Growth Marketing `growth-reporting` skill

## Worked example
A SaaS company reported monthly sign-ups and revenue only. Sign-ups had doubled in a year while revenue grew slowly. A PLG dashboard with cohort views showed activation steady but free-to-paid conversion falling for recent cohorts, because a new free plan covered most small-team needs, while sales-assisted accounts expanded well. The monthly review led to tighter free limits, new upgrade prompts and more PQL coverage for larger accounts. Revenue per sign-up recovered over two quarters, and the board received a clearer story.

## Output format
```
# PLG metrics plan: <product>, <date>
## Metric tree
## Definitions
## Data quality checks
## Cohort and segment views
## Self-serve vs sales-assisted view
## Dashboard design
## Review rhythm and decision log
```

## Common mistakes
- Reporting only sign-ups and revenue.
- Inconsistent activation definitions across teams.
- Totals instead of cohorts.
- Ignoring account-level metrics in B2B.
- Comparing to external benchmarks with different definitions.

## Questions to ask before you build
- What is your value moment, and is activation measured against it?
- Can product usage be tied to accounts and revenue?
- Who uses the metrics, and what decisions do they make?

## Self-check before you answer
- Does the metric tree cover every stage?
- Are definitions written and shared?
- Are cohorts and segments used?
- Do reviews lead to decisions?

## Further reading
- Lenny Rachitsky on PLG benchmarks: https://www.lennysnewsletter.com/
- Amplitude product analytics playbooks: https://amplitude.com/blog

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/plg-metrics/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
