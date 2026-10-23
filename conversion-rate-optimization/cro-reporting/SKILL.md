---
name: cro-reporting
description: "Report CRO programmes credibly: conversion by funnel step, device and source, revenue per visitor, average order value and qualified lead rate, test velocity, clear result and win rates, every result including losses and nulls, impact of shipped changes estimated with ranges and overlap discounts, learnings and a roadmap view. Use whenever someone asks for CRO reporting, how to show the value of conversion optimisation, A/B testing programme metrics, CRO dashboards, agency CRO reports or why test lifts don't show up in revenue."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/conversion-rate-optimization/cro-reporting/
  category: marketing
  subcategory: conversion-rate-optimization
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# CRO Programme Reporting

CRO programmes are often judged on the wrong numbers. Teams report the conversion lift of individual winning tests and add them up, claiming gains the business never sees, while losing and inconclusive tests disappear from the story. Leadership then either over-trusts CRO or stops funding it. Good reporting shows what the programme learned, what changed and what it is worth, with honest ranges and clear links to revenue.

This skill builds reporting for CRO programmes: conversion and revenue metrics by funnel step and segment, test velocity and outcomes, measured impact of shipped changes with realistic estimates, learning summaries and a roadmap view for stakeholders.

## Operating principles
1. **Report outcomes, not activity.** Revenue per visitor, conversion by step and qualified leads, not just tests run.
2. **Don't add up test lifts.** Effects overlap, fade and interact; estimate combined impact carefully.
3. **Show every result.** Wins, losses and nulls all teach something.
4. **Segment.** Device, source and new versus returning often tell different stories.
5. **Connect to decisions.** Every report ends with what changes next.

## Metrics
| Metric | Definition | Use |
|---|---|---|
| Conversion rate by funnel step | Step completions over step entries | Where the journey leaks |
| Revenue per visitor | Revenue over visitors | Captures both conversion and order value |
| Average order value | Revenue over orders | Effect of upsells and pricing presentation |
| Qualified lead rate (B2B) | Qualified leads over visitors or leads | Lead quality |
| Test velocity | Tests launched and completed per month | Programme throughput |
| Clear result rate | Tests reaching a conclusive outcome | Quality of planning and traffic use |
| Win rate | Share of tests with significant positive results | Idea quality (very high can mean tests are too safe) |
| Estimated impact of shipped changes | Annualised effect with ranges | Business value |

## When to use, and when not to
Use it to set up monthly CRO reporting, prepare leadership reviews, justify investment and evaluate agencies or tools.

Don't use it to analyse a single test (the Growth Marketing `experiment-readout` skill) or for company-wide growth dashboards (the Growth Marketing `growth-reporting` skill).

## Inputs to ask for, in one message
1. Analytics data by funnel step, device and source.
2. Test log with results, intervals and decisions.
3. Revenue and order data.
4. Shipped changes with dates.
5. Stakeholders and the decisions they make.

## Workflow

### Step 1. Define metrics and sources
One definition per metric, agreed with finance and analytics.

### Step 2. Build the funnel view
Step conversion by device and source, month by month, with annotations for releases and campaigns.

### Step 3. Summarise tests
Launched, completed, wins, losses, nulls, with links to readouts.

### Step 4. Estimate impact
For shipped wins, estimate annual impact using the measured effect, its interval and the traffic affected. Apply a discount for overlap and decay rather than adding lifts.

### Step 5. Share learnings
Top three lessons of the period and how they change the roadmap.

### Step 6. Show the roadmap
Running tests, next tests and research in progress.

### Step 7. Review with stakeholders
Monthly or quarterly, ending with decisions and owners.

## Impact estimation
| Step | Example |
|---|---|
| Measured effect | Checkout completion +2.0 points (interval +0.8 to +3.2) |
| Traffic affected | 240,000 checkout starts a year |
| Extra orders | About 4,800 (range 1,900 to 7,700) |
| Revenue | Extra orders multiplied by average order value |
| Adjustments | Discount for novelty fade and overlap with other changes |
Present the range, not just the midpoint, and revisit after six months with actual data.

## Monthly report template
```
# CRO report: <month>
## Summary (3 sentences)
## Funnel performance by step, device and source (vs last month and last year)
## Tests: launched, completed, wins, losses, nulls
## Shipped changes and estimated impact (ranges)
## Top lessons
## Roadmap: running, next, research
## Decisions and owners
```

## Why test lifts don't add up
Several effects reduce combined impact: tests overlap on the same visitors, novelty fades, some wins are false positives, and changes interact. A programme that reports eight wins of 6% each has not raised conversion by 48%. Estimate each shipped change separately with its interval, apply a discount for decay and overlap, and confirm with long-run holdouts or year-on-year trends.

## Why test lifts do not add up
Several effects reduce combined impact: tests overlap on the same visitors, novelty fades, some wins are false positives and changes interact. A programme that reports eight wins of 6% each has not raised conversion by 48%. Estimate each shipped change separately with its interval, apply a discount for decay and overlap, and confirm with long-run holdouts or year-on-year trends.

## Long-run holdouts
For programmes with enough traffic, keep a small share of visitors (for example 5%) on the original experience for a quarter. Comparing revenue per visitor between the holdout and everyone else gives the most credible estimate of total programme impact.

## Stakeholder views
| Audience | What they need |
|---|---|
| Leadership | Revenue per visitor trend, estimated impact with ranges, key decisions |
| Product and design | Lessons, research findings, upcoming tests on their pages |
| Marketing | Landing page and traffic-source performance |
| Engineering | Shipped changes, performance and QA issues |

## Annotations
Record every release, campaign, pricing change and outage on the funnel dashboard. Without annotations, CRO teams and other teams often claim the same change, or miss the real cause of a drop.

## Programme health checks
- Are tests reaching clear results, or stopping early?
- Are wins being shipped quickly and checked after launch?
- Is research feeding new hypotheses each month?
- Are lessons changing the roadmap?

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Leadership wants one number | Show revenue per visitor trend plus estimated programme impact with a range |
| Seasonality hides effects | Compare year on year and use holdouts for major changes |
| Agency reports inflated lifts | Ask for intervals, losses and nulls, and post-launch checks |
| Low traffic, few tests | Report research findings and implemented fixes alongside tests |
| Many teams change the site | Annotate every major release so effects are not misattributed |

## Handoffs to related skills
- Test log and roadmap: `cro-test-planning`
- Funnel data quality: `cro-audit`
- Experiment analysis: the Growth Marketing `experiment-readout` skill
- Company growth reporting: the Growth Marketing `growth-reporting` skill
- Paid traffic outcomes: the Performance Marketing `paid-media-reporting` skill

## Worked example
An e-commerce CRO agency reported a combined 48% conversion uplift from eight winning tests in a year, while the company's overall conversion rate had risen only slightly. The new reporting showed funnel conversion by step and device, listed all 22 tests including losses and nulls, estimated shipped impact with ranges and overlap discounts, and compared year-on-year revenue per visitor. The realistic estimate was a modest but valuable revenue gain, which leadership trusted, and the programme was refocused on checkout and mobile where the largest leaks remained.

## Output format
```
# CRO reporting plan: <site>, <date>
## Metric definitions
## Funnel dashboard design
## Test summary format
## Impact estimation method
## Monthly report template
## Review cadence and owners
```

## Common mistakes
- Adding up individual test lifts.
- Hiding losing and inconclusive tests.
- Reporting conversion rate without revenue per visitor.
- No segmentation by device or source.
- Reports without decisions.

## Questions to ask before you build
- Which outcomes matter most to the business?
- How are test results recorded today?
- What decisions will reports inform?

## Self-check before you answer
- Are outcomes, not just activity, reported?
- Is combined impact estimated with ranges and discounts?
- Are all test results shown?
- Does each report end with decisions?

## Further reading
- Kohavi, Tang and Xu, Trustworthy Online Controlled Experiments (2020)
- CXL on CRO reporting: https://cxl.com/blog/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/conversion-rate-optimization/cro-reporting/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
