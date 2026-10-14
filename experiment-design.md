---
name: experiment-design
description: "Design trustworthy growth experiments: specific hypotheses, the right design (A/B, A/B/n, holdout, geo or quasi-experiment), randomisation units, primary, secondary and guardrail metrics, sample size, minimum detectable effect and duration, variance reduction, pre-registered stopping rules and segments, and pre-launch QA. Use whenever someone asks how to design an A/B test, how many users a test needs, what to measure in an experiment, minimum detectable effect, randomisation, or how to test pricing, onboarding or features."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/experiment-design/
  category: marketing
  subcategory: growth-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Experiment Design for Growth

Most failed experiments fail before launch: the hypothesis is vague, the metric doesn't match the change, the sample is too small to detect a realistic effect, or users are randomised in a way that leaks between groups. Good design makes the result trustworthy whichever way it goes.

This skill designs A/B tests, multivariate tests, holdouts and quasi-experiments for growth work across websites, apps, emails, pricing and onboarding: hypotheses, randomisation units, primary and guardrail metrics, sample size and duration, and pre-registered analysis plans.

## Operating principles
1. **One clear hypothesis.** Evidence, change, audience, expected effect and metric in one sentence.
2. **Choose metrics before launch.** One primary metric, a few secondary metrics and guardrails, written down.
3. **Power the test.** Calculate the sample needed to detect the smallest effect worth acting on.
4. **Randomise at the right unit.** User, account, session or region, depending on how the change spreads.
5. **Pre-register the analysis.** Decide duration, stopping rules and segments in advance.

## Choosing the design
| Design | When to use | Notes |
|---|---|---|
| A/B test | One change, enough traffic | The default |
| A/B/n | Several variants of one idea | Needs more traffic; correct for multiple comparisons |
| Multivariate | Several elements interacting, very high traffic | Rarely practical for most teams |
| Holdout | Measuring a whole feature, flow or channel | Long-running; small control |
| Geo or market test | Changes that can't be randomised per user (pricing, offline, brand) | Matched regions; synthetic control |
| Before and after (quasi) | No randomisation possible | Weakest; control for seasonality and other changes |

## Randomisation units
| Unit | Use when | Risk if wrong |
|---|---|---|
| User | Most product and website tests | Same user sees both versions if logged out on several devices |
| Account or team | B2B products where users interact | Contamination between colleagues |
| Session | Low-risk UI tweaks without persistence | Inconsistent experience |
| Region or market | Pricing, marketing, offline | Fewer units, need longer tests |

## When to use, and when not to
Use it before launching any experiment that will inform a decision: onboarding changes, pricing tests, landing pages, email flows, feature launches and channel tests.

Don't use it to analyse results already collected (`experiment-readout`) or to manage the backlog (`growth-experiment-backlog`).

## Inputs to ask for, in one message
1. The change and the decision it informs.
2. Baseline rate of the primary metric and its variance.
3. Weekly traffic or users eligible for the test.
4. Experimentation tool and randomisation options.
5. Other tests running on the same audience.
6. Business cycle and seasonality.

## Workflow

### Step 1. Write the hypothesis
"Because 40% of trial users abandon at data import (funnel data), we believe offering a sample dataset will increase week-1 activation for new trials, measured by activation rate within 7 days."

### Step 2. Choose metrics
Primary: the one metric that decides the outcome. Secondary: metrics that explain why. Guardrails: metrics that must not get worse (revenue per user, unsubscribes, error rates, support tickets, page speed).

### Step 3. Size the test
Use baseline rate, minimum detectable effect (MDE), significance level (often 5%) and power (often 80%) in a calculator. If the required sample takes too long, test a bigger change, use a more sensitive metric, or use variance reduction (such as CUPED) if your platform supports it.

### Step 4. Set duration
At least one full weekly cycle, usually two; long enough to reach the sample and to observe the metric (retention needs longer).

### Step 5. Plan randomisation and exposure
Assign at the right unit; log exposure only when users actually see the change; exclude internal users and bots.

### Step 6. Pre-register
Write duration, stopping rules, segments of interest and how the decision will be made. If you need to monitor early, use a method designed for it (sequential testing) rather than repeatedly checking a fixed-horizon test.

### Step 7. Pre-launch QA
Check variants render correctly on key devices, tracking fires for both groups and the split is as expected in a short ramp.

## Sample size reality check
| Baseline | Relative MDE | Approximate users per variant |
|---|---|---|
| 5% | 5% | Over 100,000 |
| 5% | 10% | Around 30,000 |
| 5% | 20% | Around 8,000 |
| 20% | 10% | Around 6,000 |
Rough orders of magnitude at 5% significance and 80% power; always calculate for your numbers.

## Choosing a sensitive primary metric
| Goal | Less sensitive | More sensitive (if it predicts the goal) |
|---|---|---|
| Retention | 90-day retention | Week-1 core actions (validated as a leading indicator) |
| Revenue | Revenue per visitor (high variance) | Conversion to paid, with revenue as guardrail |
| Activation | Activation within 30 days | Activation within 7 days |
A more sensitive metric reaches a result faster, but only use it when your data shows it predicts the real goal.

## Guardrail examples
| Change | Guardrails |
|---|---|
| Onboarding simplification | 30-day retention, support tickets |
| Pricing page test | Revenue per visitor, refund rate |
| Email frequency | Unsubscribes, spam complaints |
| Discount offer | Margin per order, repeat purchase |
| Performance change | Error rate, page load time |

## Pre-launch QA checklist
- Both variants render correctly on top devices and browsers.
- Assignment is consistent for the same user or account across sessions.
- Exposure events fire only when the change is seen.
- Primary and guardrail metrics are recorded for both groups.
- Internal traffic and bots are excluded.
- A short ramp (a few percent of traffic) shows the expected split.

## Fixed-horizon versus sequential testing
Fixed-horizon tests decide the sample in advance and analyse once at the end; checking repeatedly inflates false positives. Sequential methods allow valid monitoring along the way at some cost in power. Choose one before launch, and make sure your experimentation tool implements it correctly.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Low traffic | Bigger changes, more sensitive metrics, longer tests or qualitative research |
| Network effects (marketplaces, social) | Randomise by cluster or region to avoid spillover |
| Pricing tests | Consider legal and fairness issues; often test by region or new users only |
| Novelty effects | Run long enough for novelty to fade; check effect over time |
| Many tests at once | Use mutually exclusive layers or check for interactions |

## Handoffs to related skills
- Backlog and priority: `growth-experiment-backlog`
- Analysis: `experiment-readout`
- Event tracking: `tracking-plan`
- Funnel evidence for hypotheses: `funnel-analysis`

## Worked example
A SaaS team planned to test a new onboarding checklist, measuring clicks on the checklist. Redesign made activation within 7 days the primary metric, with 30-day retention and support tickets as guardrails, randomised by account rather than user because team members shared workspaces. The baseline activation rate of 24% and a 10% relative MDE required about 5,000 accounts per variant, roughly three weeks of sign-ups, so the test was planned for four weeks to cover full weekly cycles. The pre-registered plan named two segments (solo and team accounts) in advance.

## Output format
```
# Experiment design: <name>, <date>
Decision it informs:
Hypothesis:
Design and randomisation unit:
Primary, secondary and guardrail metrics:
Baseline, MDE, significance, power, sample size:
Duration and stopping rules:
Segments pre-registered:
QA checklist:
```

## Common mistakes
- Vague hypotheses with no metric.
- Measuring clicks on the change instead of the outcome.
- Underpowered tests read as "no effect".
- Peeking and stopping when results look good.
- Randomising users when accounts share the experience.

## Questions to ask before you design
- What decision depends on this test?
- What is the smallest effect worth acting on?
- How many eligible users or accounts arrive each week?

## Self-check before you answer
- Is the hypothesis specific and evidence-based?
- Are metrics and guardrails defined in advance?
- Is the test powered with a realistic duration?
- Is randomisation at the right unit and the analysis pre-registered?

## Further reading
- Kohavi, Tang and Xu, Trustworthy Online Controlled Experiments (Cambridge University Press, 2020)
- Evan Miller sample size calculator: https://www.evanmiller.org/ab-testing/sample-size.html

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/experiment-design/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
