---
name: growth-audit
description: "Audit a company's growth system end to end: north star and goals, growth model, acquisition, activation, retention, monetisation, referral and loops, data and tracking, experimentation practice and reporting, find the single biggest constraint with evidence, check retention before acquisition and produce a scored, ranked 90-day plan. Use whenever someone asks for a growth audit, why growth stalled, where to focus growth efforts, how to plan a growth quarter, what the biggest growth lever is, or for a review of a growth team's work."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/growth-audit/
  category: marketing
  subcategory: growth-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Growth Audit

Growth teams often start with tactics: a referral programme because a competitor has one, a new channel because someone read about it, an experiment because it was easy to ship. Without a clear picture of where growth comes from and where it leaks, those tactics are guesses. A growth audit builds that picture first: the metric that matters, the model that drives it, the biggest constraint, and the evidence the team has (or lacks) to act on.

This skill audits a company's growth system end to end: goals and metrics, the growth model, acquisition, activation, retention, monetisation and referral, data and tracking, experimentation practice and reporting. It returns the single biggest constraint and a ranked plan, and hands each finding to a specialist skill.

## Operating principles
1. **Find the constraint.** Growth is limited by one step at a time; improving anything else has little effect.
2. **Retention first.** Acquiring users who leave quickly is the most expensive form of growth.
3. **Models over tactics.** Understand how inputs (traffic, conversion, retention, referral) combine into outcomes before choosing work.
4. **Evidence labels.** Separate what data shows, what tests proved and what the team believes.
5. **Speed of learning matters.** A team that runs good experiments weekly outgrows one that ships big bets quarterly.

## The audit areas
| Area | Key questions | Typical finding |
|---|---|---|
| Goals and north star | Is there one metric that reflects customer value and predicts revenue? | Team chases sign-ups while revenue depends on weekly active teams |
| Growth model | Do we know how inputs produce the outcome, with numbers? | No model; targets set top-down |
| Acquisition | Which channels bring retained users, at what cost and scale? | One channel provides most growth and is saturating |
| Activation | What share reach first value, and how fast? | Most sign-ups never reach the value moment |
| Retention | Do cohort curves flatten, and at what level? | Curves never flatten for some segments |
| Monetisation | Pricing, conversion to paid, expansion | Few users hit the limits that trigger upgrades |
| Referral and loops | Do users bring other users? | No loop; growth is linear with spend |
| Data and tracking | Are key events reliable and defined? | Activation event fires inconsistently |
| Experimentation | How many tests, how rigorous, how quickly? | Few tests, mostly underpowered |
| Reporting | Does the team review the right metrics weekly? | Dashboards of vanity metrics |

## When to use, and when not to
Use it when growth stalls, when a new growth lead joins, before planning a quarter, after product-market fit when scaling begins, and when leadership asks where to invest.

Don't use it to fix one funnel step in depth (use `funnel-analysis`), to run a single experiment (`experiment-design`) or for paid media accounts (the Performance Marketing skills).

## Inputs to ask for, in one message
1. Business model, customer types, pricing and revenue for 12 to 24 months.
2. Current goals and the metrics the team reviews.
3. Acquisition data by channel: volume, cost and downstream retention.
4. Funnel data from visit or sign-up to activation, paid and retained.
5. Cohort retention curves by sign-up month and segment.
6. Tracking plan or event list, and the analytics tools in use.
7. Experiment history: what was tested, results and decisions.

## Workflow

### Step 1. Agree the goal and north star
Check whether the current north star reflects delivered customer value and predicts revenue. If not, propose one (`north-star-metric-tree`).

### Step 2. Build a quick growth model
Map inputs to outcome with current numbers: new users by channel × activation rate × retention × monetisation, plus referral or loop contributions (`growth-model`).

### Step 3. Read retention first
If cohort curves don't flatten, fix retention before scaling acquisition (`cohort-retention-analysis`).

### Step 4. Find the biggest leak
Compare each step's conversion and volume with benchmarks from your own history and segments; find where the most value is lost (`funnel-analysis`).

### Step 5. Review acquisition
Which channels bring users who retain? Where is the next scalable channel? (`acquisition-channel-testing`).

### Step 6. Check loops and referral
Do users invite, share or create content that brings others? (`growth-loops`, `referral-programmes`).

### Step 7. Check data and experimentation
Are events reliable (`tracking-plan`)? Are experiments well designed, powered and read correctly (`experiment-design`, `experiment-readout`)? Is there a steady experiment cadence (`growth-experiment-backlog`)?

### Step 8. Name the constraint and plan
One sentence: "Growth is constrained by X because Y." Then a 90-day plan focused on it.

## Scoring rubric
| Score | Meaning |
|---|---|
| 0 | Missing or unknown |
| 1 | Present but unreliable or unused |
| 2 | Solid and used in decisions |
| 3 | Strong, measured, improving through experiments |

## Common constraints and first moves
| Constraint | Sign | First move |
|---|---|---|
| Retention | Curves keep falling | Find the value moment; improve onboarding and core experience |
| Activation | Many sign-ups, few reach value | Remove friction to first value |
| Acquisition scale | Good retention, slow volume | Test new channels; build loops |
| Monetisation | Engaged users don't pay | Packaging, limits and upgrade prompts |
| Learning speed | Few, slow experiments | Backlog, cadence and sizing discipline |
| Data | Numbers disagree | Fix the tracking plan before anything else |

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Pre product-market fit | Focus on retention of a narrow segment, not scale |
| B2B with few large customers | Use account-level metrics; fewer, deeper experiments |
| Marketplace | Audit both sides and the liquidity between them |
| Very low traffic | Prefer qualitative research and big changes over A/B tests |
| Seasonal business | Compare like periods; model seasonality explicitly |

## Handoffs to specialist skills
- North star and metric tree: `north-star-metric-tree`
- Growth model and forecasts: `growth-model`
- Experiment backlog and cadence: `growth-experiment-backlog`
- Experiment design: `experiment-design`
- Experiment analysis: `experiment-readout`
- New channels: `acquisition-channel-testing`
- Loops: `growth-loops`
- Referral: `referral-programmes`
- Funnels: `funnel-analysis`
- Retention cohorts: `cohort-retention-analysis`
- Tracking: `tracking-plan`
- Reporting: `growth-reporting`

## Worked example
A B2B scheduling SaaS had flat revenue despite growing sign-ups. The audit found the team optimised for sign-ups, the activation event (first booking received) fired for only 18% of new accounts within 14 days, cohort curves flattened at a low level for solo users but much higher for teams, and most acquisition came from one paid channel near saturation. The constraint: activation for solo users. The 90-day plan made weekly active teams the north star, rebuilt onboarding around receiving a first booking, added a team invite loop after first value and tested two new channels with retention as the success metric.

## Output format
```
# Growth audit: <company>, <date>
## The constraint (one sentence) and evidence
## North star and growth model snapshot
## Area scores
| Area | Score 0-3 | Key findings | Evidence label |
## 90-day plan
| # | Action | Area | Expected impact | Effort | Skill | Owner | Re-check |
```

## Common mistakes
- Scaling acquisition before retention flattens.
- Copying tactics without a model.
- Treating sign-ups as growth.
- Running many small, underpowered tests.
- Ignoring data problems until decisions go wrong.

## Questions to ask before you recommend changes
- What customer behaviour best predicts revenue?
- Where do cohort curves flatten, and for whom?
- How many experiments did the team run last quarter, and what changed because of them?

## Self-check before you answer
- Did I name one constraint with evidence?
- Did I check retention before acquisition?
- Is each finding labelled by evidence type?
- Does every action have a skill, owner and re-check date?

## Further reading
- Reforge growth frameworks: https://www.reforge.com/blog
- Amplitude North Star Playbook: https://amplitude.com/books/north-star

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/growth-audit/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
