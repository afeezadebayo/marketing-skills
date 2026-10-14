---
name: north-star-metric-tree
description: "Choose and validate a north star metric that reflects delivered customer value and predicts revenue, then build the metric tree beneath it: candidate tests, data validation, input metrics with owners and levers, targets, counter-metrics that stop gaming, tracking requirements and a weekly review cadence for SaaS, marketplaces, media, e-commerce, fintech and APIs. Use whenever someone asks about a north star metric, OMTM, metric trees, KPI trees, input metrics, growth goals, aligning teams on one metric or replacing vanity metrics."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/north-star-metric-tree/
  category: marketing
  subcategory: growth-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# North Star Metric and Metric Tree

A north star metric is the one number that best captures the value customers get from a product and that, when it grows, revenue follows. A metric tree breaks it into the input metrics teams can actually move. Together they stop teams optimising for vanity numbers (sign-ups, page views) and align marketing, product and sales on the same goal.

This skill chooses or tests a north star, builds the metric tree beneath it, assigns owners and targets to inputs, and defines counter-metrics so the north star can't be gamed.

## Operating principles
1. **Value delivered, not value captured.** Revenue is an outcome; the north star measures the customer behaviour that leads to it.
2. **Leading, not lagging.** It should move within weeks of changes, not quarters.
3. **Inputs teams can influence.** Each branch of the tree has an owner and levers.
4. **Counter-metrics protect quality.** Pair every target with a guardrail.
5. **Stable but not sacred.** Revisit when the product or business model changes.

## Good north star examples
| Business | North star | Why |
|---|---|---|
| Collaboration SaaS | Weekly active teams doing core work | Teams retain and expand; captures shared value |
| Marketplace | Weekly successful transactions | Value for both sides |
| Subscription media | Weekly engaged subscribers (consumed X items) | Engagement predicts renewal |
| E-commerce | Repeat purchasers per month | Repeat buying drives lifetime value |
| Fintech app | Monthly active transacting users | Usage drives revenue and retention |
| B2B API | Weekly API calls from active paying accounts (or successful outcomes) | Usage reflects integration depth |

## When to use, and when not to
Use it when teams pull in different directions, when goals are vanity metrics, when setting annual or quarterly goals, after a pivot or new product line, and when building a growth model.

Don't use it to model forecasts in detail (`growth-model`) or to design reporting dashboards (`growth-reporting`).

## Inputs to ask for, in one message
1. Product, customers, business model and how revenue is earned.
2. Candidate metrics and how they're calculated today.
3. Event data linking user behaviour to retention and revenue.
4. Team structure: who owns acquisition, activation, engagement, monetisation.
5. Current goals and how they were set.

## Workflow

### Step 1. List candidates
Write five to ten candidate metrics describing customer value moments.

### Step 2. Test each candidate
| Test | Question |
|---|---|
| Value | Does it reflect value customers actually receive? |
| Revenue link | Does it predict revenue or retention in your data? |
| Leading | Does it respond to changes within weeks? |
| Actionable | Can teams influence it through inputs? |
| Understandable | Can everyone explain it in one sentence? |
| Hard to game | Would gaming it hurt customers or the business? |

### Step 3. Validate with data
Check correlation between the candidate and retention or revenue across cohorts and segments. Treat as correlation; confirm with experiments over time.

### Step 4. Build the tree
Break the north star into multiplicative or additive inputs. Example for weekly active teams: new teams activated + existing teams retained + reactivated teams; then each into its drivers (sign-ups by channel × activation rate; retention by segment; reactivation from lifecycle).

### Step 5. Assign owners and levers
Each input gets an owner and a list of levers (channels, onboarding, features, lifecycle messages, pricing).

### Step 6. Set targets and counter-metrics
Targets for inputs from the growth model; guardrails such as revenue per user, support tickets, unsubscribe rates or quality scores.

### Step 7. Instrument and review
Make sure each metric is tracked reliably; review the tree weekly in the growth meeting.

## Metric tree template
```
North star: Weekly active teams (WAT)
├─ New activated teams
│  ├─ Sign-ups by channel
│  └─ Activation rate (first core action within 7 days)
├─ Retained active teams
│  ├─ Week-4 retention by segment
│  └─ Depth of use (core actions per team per week)
└─ Reactivated teams
   └─ Reactivation rate from lifecycle campaigns
Counter-metrics: revenue per team, support tickets per team, NPS
```

## Validating a candidate with data
1. For each user or account, calculate the candidate metric in their first 4 to 8 weeks.
2. Group into bands (for example 0, 1 to 2, 3 to 5, 6+ weekly core actions).
3. Compare 6-month retention and revenue by band.
4. Look for a clear step change: the band where retention jumps is a candidate threshold for the definition.
5. Check the pattern holds across segments and acquisition channels.
6. Label the result as correlation and plan an experiment that pushes users towards the behaviour.

| Weekly messages sent (first 4 weeks) | Share of teams | 6-month retention | Paid conversion |
|---|---|---|---|
| 0 to 9 | 41% | low | low |
| 10 to 49 | 33% | medium | medium |
| 50+ | 26% | high | high |
Illustrative; use your own data.

## Writing a precise definition
A north star definition includes: the unit (user, team, account), the behaviour (the core action), the threshold (how much), the time window (weekly, monthly) and exclusions (internal users, test accounts, bots). Example: "Weekly active teams = paying or trial teams, excluding internal accounts, with at least 50 messages sent by at least two members in the last 7 days."

## Counter-metric examples
| Target | Risk if gamed | Counter-metric |
|---|---|---|
| Weekly active teams | Fake activity from notifications | Messages per member; churn rate |
| Activation rate | Lowering the bar for activation | 30-day retention of activated users |
| Sign-ups | Low-quality traffic | Activation rate by channel |
| Transactions (marketplace) | Discount-driven low-margin orders | Contribution margin per transaction |

## Review rituals
- **Weekly:** north star and inputs versus target, notable changes, experiments affecting each input.
- **Monthly:** input trends by segment and channel, owner updates.
- **Quarterly:** check the north star still predicts revenue; adjust targets from the growth model.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Several products | One company north star plus product-level stars that roll up |
| Two-sided marketplace | Transaction-based star with supply and demand inputs |
| Long purchase cycles | Use an engagement-based leading metric between purchases |
| Low usage frequency by nature (tax, travel) | Monthly or annual frame; avoid forcing weekly metrics |
| Leadership wants revenue as north star | Keep revenue as the business goal and use the north star as its leading indicator |

## Handoffs to related skills
- Forecasts from the tree: `growth-model`
- Retention validation: `cohort-retention-analysis`
- Event definitions: `tracking-plan`
- Weekly review: `growth-reporting`
- Overall audit: `growth-audit`

## Worked example
A team chat product used monthly sign-ups as its goal. Sign-ups grew, revenue didn't. Testing candidates showed "weekly active teams sending 50+ messages" predicted paid conversion and 6-month retention far better than sign-ups or monthly active users. The new tree split it into new activated teams, retained teams and reactivated teams, each with an owner. Counter-metrics tracked revenue per team and support load. Within two quarters, onboarding and lifecycle work focused on team activation, and paid conversions rose alongside the north star.

## Output format
```
# North star and metric tree: <company>, <date>
## Candidate evaluation (table)
## Chosen north star and definition
## Validation evidence (labelled correlation)
## Metric tree with owners and levers
## Targets and counter-metrics
## Tracking requirements and review cadence
```

## Common mistakes
- Choosing revenue or sign-ups as the north star.
- Metrics nobody can influence directly.
- No counter-metrics, so teams game the number.
- Definitions that differ between teams.
- Changing the north star every quarter.

## Questions to ask before you choose
- What does a successful customer do regularly?
- Which behaviour best predicts retention and revenue in your data?
- Who owns each input today?

## Self-check before you answer
- Does the north star reflect delivered value and predict revenue?
- Is the tree broken into actionable inputs with owners?
- Are counter-metrics defined?
- Are definitions precise and tracked?

## Further reading
- Amplitude North Star Playbook: https://amplitude.com/books/north-star
- Reforge on growth models and metrics: https://www.reforge.com/blog

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/north-star-metric-tree/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
