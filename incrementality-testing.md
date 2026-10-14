---
name: incrementality-testing
description: "Design and read incrementality tests that show whether ads create sales: platform conversion lift studies, matched-market geo experiments, geo holdouts, on and off tests and brand search tests, with decision rules, power analysis, clean execution, first-party outcomes, incremental ROAS and CAC with intervals, and calibration of plans and MMMs. Use whenever someone asks whether ads are incremental, how to run a geo test or lift study, whether retargeting or brand search works, why attribution and finance disagree, or how to prove marketing ROI."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/incrementality-testing/
  category: marketing
  subcategory: performance-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Incrementality Testing: Lift and Geo Experiments

Platform attribution answers "who touched this conversion?" Incrementality answers "would this conversion have happened without the ads?" The second question decides whether spend creates value. Retargeting, brand search and view-through credit often look excellent in attribution and turn out to add little when tested; upper-funnel video can look weak in attribution and turn out to drive sales.

This skill designs and reads incrementality tests: platform conversion lift studies, geo experiments (matched markets and holdouts), on and off tests, and brand search tests, so budget decisions rest on causal evidence.

## Operating principles
1. **Randomise or match.** Comparisons only work when test and control are equivalent before the test.
2. **Measure outcomes in your own data** where possible: orders, new customers, revenue from your systems.
3. **Plan power before spending.** Tests too small to detect a realistic effect waste money.
4. **One question per test.** "Is retargeting incremental?" not "is everything working?"
5. **Use results to calibrate.** Feed lift results into MMM and planning; don't let them sit in a slide.

## Test types
| Test | How it works | Best for | Limits |
|---|---|---|---|
| Platform conversion lift (Meta, Google) | Platform randomly withholds ads from a control group and compares conversions | Single-channel questions with enough volume | Measured inside the platform's own data |
| Geo experiment (matched markets) | Ads on in some regions, off or reduced in matched regions | Cross-channel, offline sales, brand search | Needs enough regions and stable baselines |
| Geo holdout at national level | Turn a channel off in a share of regions | Testing whole channels | Revenue risk during the test |
| On and off (time-based) | Switch spend on and off over periods | Small advertisers without geo options | Confounded by seasonality; weakest design |
| Brand search test | Pause brand ads in some regions or periods, watch total brand clicks | Brand search value | Competitor bidding changes results |

## When to use, and when not to
Use it before big budget shifts, when attribution and finance disagree, to test retargeting, brand search, video and new channels, and to calibrate an MMM.

Don't use it for creative A/B tests inside a channel (`ad-creative-testing`) or for routine reporting (`paid-media-reporting`).

## Inputs to ask for, in one message
1. The decision the test informs and the channel or tactic in question.
2. Weekly or daily outcome data by region for at least a year (orders, revenue, new customers).
3. Spend by channel and region.
4. Platform access for lift studies, if available.
5. Seasonality, promotions and other changes planned during the test window.

## Workflow

### Step 1. Frame the question
State the hypothesis and the decision: "If retargeting adds less than X new customers per £1,000, we cut it by half."

### Step 2. Choose the design
Platform lift for single-channel questions with volume; geo experiment for cross-channel effects, offline sales or when you don't trust platform measurement.

### Step 3. Select regions (geo tests)
Use historical data to match test and control regions on trend and seasonality, or use synthetic control methods (open-source tools such as Meta's GeoLift or Google's CausalImpact).

### Step 4. Power the test
Estimate the minimum detectable effect from historical variance, test duration and spend change. Increase spend change, duration or regions until the test can detect a meaningful effect.

### Step 5. Run cleanly
No other major changes in test or control regions; monitor spend delivery; log anything unusual.

### Step 6. Analyse
Compare actual outcomes in test regions with predicted outcomes from control; report incremental conversions, incremental revenue, incremental ROAS or CAC, with a confidence interval.

### Step 7. Decide and calibrate
Apply the decision rule; update the media plan and MMM priors; schedule the next test.

## Reading results
| Result | Meaning | Action |
|---|---|---|
| Large lift, tight interval | Clear incremental value | Scale in steps and re-test at higher spend |
| Small lift, interval includes zero | No evidence of value at this spend | Cut or redesign, or test with more power |
| Lift below attribution claims | Attribution over-credits | Use incrementality factors in reporting |
| Lift above attribution claims | Channel under-credited (common for video) | Consider increasing budget |

## Power analysis in plain terms
- **Minimum detectable effect (MDE):** the smallest lift the test can reliably detect.
- It shrinks when you run longer, include more regions, change spend more, or have steadier baselines.
- If the MDE is larger than the effect you expect, the test will probably say "no result" even if the channel works.
- Rule of thumb: aim for an MDE at or below the lift that would change your decision.

## Geo test checklist
1. Pick the outcome (orders, new customers, revenue) from your own systems, by region, daily or weekly.
2. Collect at least six to twelve months of history.
3. Choose test regions with a matching tool; check pre-period fit visually and statistically.
4. Decide the treatment: channel off, spend halved or spend doubled.
5. Freeze other changes in both groups for the test period.
6. Run for at least two full purchase cycles (often four to six weeks).
7. Analyse with the method chosen in advance; report the interval.
8. Include a cool-down period if effects may carry over.

## Converting results to planning numbers
| Measure | Formula |
|---|---|
| Incremental conversions | Actual minus counterfactual in test regions |
| Incremental ROAS (iROAS) | Incremental revenue ÷ test spend |
| Incremental CAC (iCAC) | Test spend ÷ incremental new customers |
| Incrementality factor | Incremental conversions ÷ platform-reported conversions |
Use the incrementality factor to adjust platform-reported results in weekly reporting until the next test.

## Test calendar example
| Quarter | Question | Design |
|---|---|---|
| Q1 | Is Meta retargeting incremental? | Geo holdout, 20% of regions |
| Q2 | What does YouTube add? | Matched-market geo test with spend increase |
| Q3 | Is brand search worth it where competitors don't bid? | Regional pause test |
| Q4 | Calibrate MMM before peak | Platform lift study on prospecting |

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| National-only advertiser, few regions | Use time-based tests with care, or platform lift studies |
| Heavy seasonality | Avoid peak periods or use longer pre-periods to model baselines |
| Brand search with competitor bidding | Test in regions with less competition and watch competitor share |
| Small budgets | Test whole channels rather than tactics; accept longer durations |
| Stakeholders fear revenue loss | Use partial reductions rather than full off, or smaller holdout regions |

## Handoffs to related skills
- Planning with results: `media-planning-budgeting`
- MMM calibration: `marketing-mix-modelling`
- Reporting incrementality factors: `paid-media-reporting`
- Channel changes after tests: `meta-ads`, `google-search-ads`, `performance-max-shopping`

## Worked example
An online retailer spent a fifth of its Meta budget on retargeting, which showed the best ROAS in Ads Manager. A four-week geo test turned retargeting off in a set of matched regions covering about 20% of sales. Total orders in test regions were statistically indistinguishable from the forecast based on control regions, while prospecting tests in a later quarter showed clear lift. Retargeting was cut to a small always-on budget for cart abandoners and the savings moved to prospecting, raising new customers at the same blended spend.

## Output format
```
# Incrementality test: <channel/tactic>, <date>
Decision and rule:
Design (lift / geo / time), regions or groups, duration:
Power analysis (minimum detectable effect):
Primary outcome (from own data) and guardrails:
Result: incremental conversions, revenue, iROAS or iCAC, interval
Decision and calibration notes:
```

## Common mistakes
- Treating attribution as proof of value.
- Running underpowered tests and reading noise.
- Changing other channels in test regions mid-test.
- Measuring only inside the platform being tested.
- Not using results to change budgets or models.

## Questions to ask before you test
- What decision depends on this test, and what threshold changes it?
- Do you have regional outcome data, and for how long?
- How much revenue risk can the business accept during the test?

## Self-check before you answer
- Are test and control equivalent before the test?
- Is the test powered for a meaningful effect?
- Are outcomes measured in first-party data with intervals?
- Is there a decision rule and a calibration step?

## Further reading and tools
- Meta GeoLift (open source): https://facebookincubator.github.io/GeoLift/
- Google CausalImpact: https://google.github.io/CausalImpact/
- Meta conversion lift: https://www.facebook.com/business/help/
- Google Ads conversion lift: https://support.google.com/google-ads/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/incrementality-testing/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
