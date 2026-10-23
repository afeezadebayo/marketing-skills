---
name: cohort-retention-analysis
description: "Build and read cohort retention analyses for users, accounts and revenue: value-based activity definitions, N-day, unbounded and bracket retention, logo retention, net revenue retention and repeat purchase rate, cohort tables and curves, flattening, cohort comparisons over time, segments by channel and plan, retention-linked behaviours and actions. Use whenever someone asks about retention analysis, cohort analysis, retention curves, churn by cohort, net revenue retention, repeat purchase rate, product-market fit signals or why users don't come back."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/cohort-retention-analysis/
  category: marketing
  subcategory: growth-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Cohort Retention Analysis

Retention is the foundation of growth. If users stop coming back, every acquisition pound leaks away, and growth stalls however much you spend. Cohort analysis shows retention properly: group users by when they started, follow each group over time, and see whether the curve flattens (people who stay, stay) or keeps falling towards zero. It also shows whether recent changes made newer cohorts better than older ones.

This skill builds and reads cohort retention analyses for users, accounts and revenue, segments them to find who retains and why, identifies behaviours linked to retention and turns findings into retention work.

## Operating principles
1. **Use cohorts, not averages.** Blended retention mixes old and new users and hides change.
2. **Look for the flattening.** A curve that levels off shows product-market fit for that segment; one that keeps falling doesn't.
3. **Define "retained" by value.** Returning to do the core action beats simply logging in.
4. **Choose the right frame.** Daily for social apps, weekly for work tools, monthly for many SaaS and e-commerce, by purchase cycle for consumables.
5. **Revenue retention matters too.** Expansion can make revenue curves rise even when user curves fall.

## Types of retention
| Type | Definition | Use |
|---|---|---|
| N-day / N-week retention | Share active exactly on day or week N | Engagement products |
| Unbounded (rolling) retention | Share active on day N or later | Lower-frequency products |
| Bracket retention | Share active in a window (for example days 7 to 13) | Smoother curves for irregular use |
| Logo retention (B2B) | Share of accounts still customers | Subscription health |
| Net revenue retention (NRR) | Revenue from a cohort including expansion, minus churn and contraction | SaaS growth efficiency |
| Repeat purchase rate | Share buying again within a window | E-commerce |

## When to use, and when not to
Use it in growth audits, before scaling acquisition, after onboarding or product changes, when comparing channels or segments, and to find the activation moment.

Don't use it for short-term conversion steps (`funnel-analysis`) or to run retention campaigns (the CRM and Lifecycle `retention-churn-prevention` skill).

## Inputs to ask for, in one message
1. Event or order data with user or account IDs and timestamps.
2. The core action that represents value.
3. Segments: acquisition channel, plan, country, device, use case, company size.
4. Revenue data for revenue retention.
5. Dates of major product or pricing changes.

## Workflow

### Step 1. Define the cohort and activity
Cohort by sign-up or first-purchase week or month; activity as the core value action.

### Step 2. Build the cohort table
Rows are cohorts, columns are periods since start, cells are share retained.

### Step 3. Plot curves
One line per cohort or segment; look for flattening and its level.

### Step 4. Compare cohorts over time
Are newer cohorts retaining better after changes? Annotate change dates.

### Step 5. Segment
By channel, plan, use case and company size. Find segments with flat, high curves (your best customers) and those that never flatten.

### Step 6. Find retention-linked behaviours
Compare early behaviours of retained and churned users; candidate activation moments (validate with experiments).

### Step 7. Add revenue retention
NRR or revenue cohort curves for subscription and B2B businesses.

### Step 8. Recommend actions
Onboarding to the value moment, focusing acquisition on high-retention segments, product fixes for drop-off points, and lifecycle interventions.

## Reading curves
| Pattern | Meaning | Action |
|---|---|---|
| Falls then flattens at a healthy level | Core users found value | Scale acquisition of similar users |
| Keeps falling towards zero | No lasting value for this group | Fix product or narrow the target segment |
| Newer cohorts flatten higher | Changes are working | Keep going; measure which change |
| One channel much lower | Channel brings poor-fit users | Change targeting or reduce spend |
| Revenue curve rises above 100% | Expansion outweighs churn | Invest in expansion levers |

## Cohort table example
| Sign-up week | Users | Week 1 | Week 2 | Week 4 | Week 8 | Week 12 |
|---|---|---|---|---|---|---|
| 2026-06-01 | 2,100 | 48% | 36% | 27% | 22% | 21% |
| 2026-06-08 | 2,300 | 51% | 39% | 30% | 25% | 24% |
| 2026-07-06 (new onboarding) | 2,250 | 58% | 46% | 36% | 31% | |
Illustrative; note the flattening after week 8 and the higher curve after the onboarding change.

## Cohort query example (SQL)
```sql
WITH first_seen AS (
  SELECT user_id, DATE_TRUNC('week', MIN(ts)) AS cohort_week
  FROM events WHERE event = 'signed_up' GROUP BY user_id
), activity AS (
  SELECT DISTINCT user_id, DATE_TRUNC('week', ts) AS active_week
  FROM events WHERE event = 'completed_lesson'
)
SELECT f.cohort_week,
       DATE_DIFF(a.active_week, f.cohort_week, WEEK) AS week_n,
       COUNT(DISTINCT a.user_id) AS active_users
FROM first_seen f JOIN activity a USING (user_id)
GROUP BY 1, 2 ORDER BY 1, 2;
```
Divide by cohort size to get retention rates; adapt syntax to your warehouse.

## Retention benchmarks: use with care
Published retention benchmarks vary widely by category, platform and definition. Compare your own cohorts over time and across segments first; use outside benchmarks only as rough context, with their definitions checked.

## Finding retention-linked behaviours
1. Take users from cohorts at least 90 days old.
2. Split into retained and churned by your definition.
3. Compare their first 7 to 14 days: actions taken, features used, invites sent, settings completed.
4. Rank behaviours by the retention difference and by how many users do them.
5. Pick candidates the team can influence and test them with experiments.

## Revenue retention view
| Cohort | Month 0 revenue | Month 6 | Month 12 | NRR at 12 months |
|---|---|---|---|---|
A cohort whose revenue rises above its starting point shows expansion outweighing churn, a strong sign for subscription businesses.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Irregular usage | Use bracket or unbounded retention |
| Seasonal products | Compare like-for-like cohorts year on year |
| B2B with seats | Track account retention and seat expansion separately |
| Small cohorts | Group into months or quarters; show confidence |
| Free and paid users mixed | Analyse separately and together |

## Handoffs to related skills
- Growth model inputs: `growth-model`
- North star validation: `north-star-metric-tree`
- Funnel before retention: `funnel-analysis`
- Event definitions: `tracking-plan`
- Retention programmes: the CRM and Lifecycle skills

## Worked example
A language learning app saw monthly active users growing but revenue flat. Weekly cohort curves for the core action (completing a lesson) never flattened for users from a paid social campaign, while organic and referral cohorts flattened around a much higher level. Users who completed three lessons in their first week retained far better. The team shifted paid social targeting, rebuilt the first week around three short lessons and a streak, and newer cohorts began to flatten at a higher level within two months.

## Output format
```
# Cohort retention analysis: <product>, <date>
## Definitions (cohort, activity, frame)
## Cohort table and curves
## Changes over time (annotated)
## Segment comparison
## Retention-linked behaviours (labelled correlation)
## Revenue retention
## Recommendations
```

## Common mistakes
- Blended retention instead of cohorts.
- Defining retention as any login.
- Wrong time frame for the product.
- Ignoring revenue retention and expansion.
- Treating correlated behaviours as proven causes.

## Questions to ask before you analyse
- What action shows a user got value?
- How often should a healthy user do it?
- What changed in the product or acquisition recently?

## Self-check before you answer
- Are cohorts and activity defined by value?
- Did I check for flattening and compare cohorts over time?
- Did I segment by channel and plan?
- Are behaviours labelled as correlation with tests planned?

## Further reading
- Amplitude, retention analysis guide: https://amplitude.com/blog
- Mixpanel, retention reports: https://docs.mixpanel.com/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/cohort-retention-analysis/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
