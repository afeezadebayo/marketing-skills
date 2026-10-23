---
name: cro-test-planning
description: "Build a CRO test roadmap: evidence-based hypotheses, traffic and duration estimates per page, PIE, ICE or PXL scoring, decisions to test, implement, research or drop, low-traffic strategies, scheduling without overlap, test briefs with metrics and decision rules, and a shared learning log. Use whenever someone asks how to prioritise A/B test ideas, build a CRO roadmap, what to test first, testing with low traffic, PIE or PXL scoring, test briefs or running several tests at once."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/conversion-rate-optimization/cro-test-planning/
  category: marketing
  subcategory: conversion-rate-optimization
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# CRO Test Planning and Prioritisation

A CRO programme succeeds or fails on what it chooses to test. Teams with more ideas than traffic must decide which hypotheses deserve scarce test slots, which changes should simply be implemented and which need more research first. Without a plan, teams test whatever someone suggested last, run underpowered tests on low-traffic pages and overlap experiments that contaminate each other.

This skill builds a CRO test roadmap: collecting hypotheses, scoring and prioritising them, matching tests to pages with enough traffic, scheduling to avoid overlap, defining success metrics and keeping a learning log. Detailed experiment statistics are covered by the Growth Marketing experiment skills.

## Operating principles
1. **Hypotheses from evidence.** Every test idea links to research or data.
2. **Traffic decides what can be tested.** Low-traffic pages need bigger changes or a different approach.
3. **Prioritise consistently.** One scoring method, revisited as evidence arrives.
4. **Avoid overlap.** Tests on the same audience and funnel step can interfere.
5. **Learn from every test.** Wins, losses and nulls go into a shared log.

## Prioritisation frameworks
| Framework | Scores | Notes |
|---|---|---|
| PIE | Potential, importance, ease | Common for page-level CRO |
| ICE | Impact, confidence, ease | Simple and fast |
| PXL (CXL) | Yes or no questions on evidence, visibility, ease and more | Reduces subjective scoring |
Any framework works if applied consistently and backed by evidence.

## When to use, and when not to
Use it when starting a CRO programme, when the backlog is long and unprioritised, when tests rarely reach significance, when several teams test on the same site and for quarterly planning.

Don't use it for experiment statistics and readouts (the Growth Marketing `experiment-design` and `experiment-readout` skills) or for company-wide growth experimentation cadence (the Growth Marketing `growth-experiment-backlog` skill).

## Inputs to ask for, in one message
1. Hypothesis backlog with evidence.
2. Traffic and conversions per page and funnel step per week.
3. Testing tool and capacity (design, development, analysis).
4. Business priorities and upcoming changes (launches, redesigns, campaigns).
5. Past test results.

## Workflow

### Step 1. Collect hypotheses
From the CRO audit, research, analytics, support and sales, each written with evidence, change, audience and metric.

### Step 2. Check traffic
For each target page, estimate how long a test needs to detect a meaningful lift. Pages that can't reach significance in a few weeks need bigger changes, before-and-after monitoring or research.

### Step 3. Score
Use PIE, ICE or PXL; weight potential by traffic and value at that step.

### Step 4. Decide the action
Test, implement, research more or drop.

### Step 5. Schedule
One test per page or funnel step at a time unless the tool supports isolated layers; avoid peak periods unless the test is about them.

### Step 6. Define success
Primary metric, guardrails, duration and minimum sample for each test.

### Step 7. Review results
Record results, decisions and learnings in the log; update the backlog.

### Step 8. Report
Monthly roadmap view: running, next, completed, wins and impact.

## Test brief template
```
Name:
Hypothesis: Because [evidence], changing [element] for [audience] will [effect] on [metric].
Page and funnel step:
Weekly visitors and conversions:
Estimated duration to reach sample:
Primary metric and guardrails:
Variants (with screenshots or descriptions):
QA checklist owner:
Launch date and end date:
Decision rule:
```

## Low-traffic strategies
| Strategy | When |
|---|---|
| Test bigger changes | Small tweaks can't be detected |
| Test higher in the funnel | More visitors at earlier steps |
| Use micro-conversions carefully | When they predict the final outcome |
| Implement and monitor | Strong evidence, low risk |
| Run qualitative research | Unclear causes |
| Pool similar pages | Templates with shared layouts |

## Duration estimate example
| Page | Weekly visitors | Baseline conversion | Lift to detect | Approx. weeks needed |
|---|---|---|---|---|
| Checkout | 20,000 | 60% | 3% relative | 2 to 3 |
| Pricing page | 6,000 | 8% | 10% relative | 4 to 6 |
| Product page (one item) | 800 | 3% | 10% relative | Too long: implement and monitor |
Illustrative; calculate with a sample size calculator for your own numbers.

## PXL-style questions
- Is the change above the fold or on a high-visibility element?
- Is it noticeable within five seconds?
- Does it add or remove a meaningful element?
- Is it backed by user testing, qualitative feedback or analytics?
- Does it address a known drop-off point?
- Is it easy to implement?
Scoring yes or no answers reduces debate about subjective 1-to-10 ratings.

## Learning log fields
| Field | Example |
|---|---|
| Test name | Delivery costs on product pages |
| Hypothesis and evidence | Exit survey: surprise costs top reason |
| Page and step | Product page, add to cart |
| Result | Positive; checkout completion up; interval above zero |
| Decision | Shipped |
| Lesson | Cost transparency matters early for mobile visitors |
Review the log quarterly to find patterns worth turning into bigger changes.

## QA before launch
- Variants render correctly on top browsers and devices.
- Tracking records the primary metric for every variant.
- Flicker is minimised and pages stay fast.
- Internal traffic is excluded.
- A short ramp confirms the expected traffic split.

## Roadmap review cadence
- Weekly: check running tests for tracking issues and traffic delivery; never stop early on promising numbers.
- Monthly: review completed tests, update the learning log and re-score the backlog.
- Quarterly: compare the roadmap with business priorities, retire stale ideas and plan larger changes built from accumulated lessons.

## Implement and monitor
For strong-evidence, low-risk fixes on low-traffic pages, implement the change, annotate the date and compare conversion over matching periods before and after, allowing for seasonality and traffic mix. This is weaker evidence than a test but far better than leaving known problems unfixed.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Several teams testing | Shared calendar and ownership by page or step |
| Seasonal peaks | Avoid testing major changes during peaks unless the test is seasonal |
| Redesign planned | Test key hypotheses before the redesign; avoid testing pages about to change |
| HiPPO pressure (highest-paid person's opinion) | Score their idea like any other; test if worthwhile |
| Many small wins | Combine learnings into larger changes |

## Handoffs to related skills
- Hypotheses: `cro-audit`, `conversion-research`
- Page-specific test ideas: `landing-page-optimisation`, `form-optimisation`, `pricing-page-optimisation`, `checkout-optimisation`
- Reporting: `cro-reporting`
- Experiment design and analysis: the Growth Marketing `experiment-design` and `experiment-readout` skills

## Worked example
An e-commerce company had 80 test ideas from different teams and ran tests that rarely reached significance. The new roadmap rewrote ideas as hypotheses with evidence, estimated test duration for each page, moved low-traffic product page tweaks to implement-and-monitor, prioritised checkout and cart tests with PXL scoring and scheduled one test per funnel step. Over the next two quarters, more tests reached clear results, and the checkout tests produced the largest measured revenue gains.

## Output format
```
# CRO test roadmap: <site>, <quarter>
## Hypothesis backlog with evidence and scores
## Traffic and duration estimates
## Decisions (test, implement, research, drop)
## Schedule by page and funnel step
## Test briefs for upcoming tests
## Learning log
```

## Common mistakes
- Testing ideas without evidence.
- Running tests on pages that can't reach significance.
- Overlapping tests on the same step.
- Inconsistent prioritisation.
- No learning log.

## Questions to ask before you plan
- Which pages have enough traffic for testing?
- What evidence supports each idea?
- Who owns each page and funnel step?

## Self-check before you answer
- Is every test backed by evidence?
- Are durations realistic for the traffic?
- Are tests scheduled to avoid overlap?
- Are results recorded in a shared log?

## Further reading
- CXL PXL prioritisation framework: https://cxl.com/blog/
- Evan Miller sample size calculator: https://www.evanmiller.org/ab-testing/sample-size.html

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/conversion-rate-optimization/cro-test-planning/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
