---
name: experiment-readout
description: "Analyse experiment results and write readouts that lead to sound decisions: sample ratio mismatch, exposure, tracking parity and balance checks, effect sizes with intervals, guardrails, secondary metrics, trends and novelty, pre-registered versus exploratory segments, practical significance translated into north star and revenue impact, and a ship, iterate or stop decision. Use whenever someone asks to analyse an A/B test, read experiment results, check statistical significance, investigate sample ratio mismatch, decide whether to ship a test or write an experiment readout."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/experiment-readout/
  category: marketing
  subcategory: growth-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Experiment Readouts and Analysis

A test can be designed perfectly and still mislead if the readout is wrong: a sample ratio mismatch nobody checked, a winner declared from one segment out of twenty, a novelty spike treated as a lasting effect, or a "no difference" result from a test that could never have detected one. The readout is where experiments earn trust or lose it.

This skill analyses experiment results and writes readouts that lead to sound decisions: data quality checks, primary and guardrail analysis with intervals, segment analysis that avoids fishing, practical significance, and a clear ship, iterate or stop decision.

## Operating principles
1. **Check data quality first.** Sample ratio mismatch, exposure logging and tracking issues invalidate results.
2. **Report effect sizes with intervals,** not just "significant or not".
3. **Stick to the pre-registered plan.** Extra segments are exploratory, not proof.
4. **Practical significance matters.** A real but tiny effect may not be worth shipping.
5. **Write for decisions.** Every readout ends with what happens next and why.

## Data quality checks
| Check | What to look for | If it fails |
|---|---|---|
| Sample ratio mismatch (SRM) | Group sizes differ from the planned split beyond chance (chi-square test) | Don't trust the result; find the cause (redirects, bots, assignment bugs) |
| Exposure | Users counted only when they saw the change | Re-analyse with correct exposure |
| Tracking parity | Events recorded equally in both groups | Fix tracking and re-run |
| Pre-period balance | Groups similar on key metrics before the test | Investigate randomisation |
| Duration | Planned sample and full weekly cycles reached | Extend or report as inconclusive |

## When to use, and when not to
Use it after every experiment, when results look surprising, when stakeholders disagree about a result, and when reviewing past tests for the learning library.

Don't use it to design tests (`experiment-design`) or manage the backlog (`growth-experiment-backlog`).

## Inputs to ask for, in one message
1. The experiment design: hypothesis, metrics, planned sample, duration, segments.
2. Raw or aggregated results by variant: users, conversions, revenue, guardrails.
3. Daily results to check trends and novelty.
4. Experimentation tool output and its statistical method.
5. Any incidents during the test (outages, campaigns, releases).

## Workflow

### Step 1. Run quality checks
SRM, exposure, tracking parity, balance and duration. Stop here if any fail badly.

### Step 2. Analyse the primary metric
Effect size (absolute and relative), confidence interval (or credible interval for Bayesian tools) and p-value or probability, using the method chosen in advance.

### Step 3. Check guardrails
Any significant harm? Weigh trade-offs explicitly.

### Step 4. Look at secondary metrics
Do they support the story behind the primary result?

### Step 5. Check trends over time
Plot cumulative and daily effects; look for novelty or learning effects.

### Step 6. Pre-registered segments
Report the segments planned in advance. Treat new segment findings as hypotheses for future tests, corrected for multiple comparisons.

### Step 7. Judge practical significance
Is the effect large enough, given costs and complexity, to ship? Translate it into the north star or revenue using the growth model.

### Step 8. Decide and document
Ship, iterate or stop, with reasons; add to the learning library.

## Interpreting results
| Result | Meaning | Typical decision |
|---|---|---|
| Positive, interval clearly above zero, guardrails fine | Likely real improvement | Ship; monitor |
| Positive but guardrail harmed | Trade-off | Decide on business value; consider iterating |
| Interval includes zero, test well powered | No meaningful effect at the size you care about | Stop; record lesson |
| Interval includes zero, test underpowered | Inconclusive | Re-test bigger or with more traffic, or move on |
| Negative, interval below zero | Change hurts | Don't ship; learn why |

## Readout template
```
# Experiment readout: <name>
Decision: SHIP / ITERATE / STOP
Summary (2 sentences): what changed, what happened, why it matters
Quality checks: SRM, exposure, tracking, balance, duration (pass/fail)
Primary metric: control X%, variant Y%, relative change Z% (95% interval A% to B%)
Guardrails: ...
Secondary metrics: ...
Trend over time: ...
Pre-registered segments: ...
Exploratory notes (not decisions): ...
Impact estimate on north star / revenue: ...
Lessons and next test:
```

## Checking for sample ratio mismatch
1. Take the planned split (for example 50/50) and the actual counts per group.
2. Run a chi-square goodness-of-fit test (most experimentation tools do this automatically).
3. A very small p-value (commonly below 0.001) signals a mismatch worth investigating.
4. Common causes: redirects that drop users in one variant, bot filtering applied unevenly, assignment logged after a page change, caching, or users excluded by a condition only one variant triggers.
5. Fix the cause and re-run; don't adjust the numbers to force balance.

## Multiple comparisons
Testing many metrics or segments raises the chance of a false winner. With 20 independent segments at a 5% significance level, one will look significant by chance on average. Pre-register the few that matter, and treat the rest as ideas for new tests, or apply a correction (such as Bonferroni or false discovery rate control) when exploring.

## Translating results into impact
| Step | Example |
|---|---|
| Effect on primary metric | Activation +2.1 points (interval 0.8 to 3.4) |
| Users affected per month | 12,000 new trials |
| Extra activated users per month | About 250 (range 100 to 410) |
| Downstream conversion to paid | 30% of activated users |
| Extra paying customers per month | About 75 (range 30 to 120) |
| Revenue impact | Monthly ARPU × extra customers, accumulated over their lifetime |
Show the range throughout; leadership decisions improve when uncertainty is visible.

## Bayesian and frequentist readouts
Frequentist tools report p-values and confidence intervals; Bayesian tools report probabilities that a variant is better and credible intervals. Either works if used as designed. Don't mix them in one readout, and don't switch methods after seeing results.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| SRM detected | Treat results as invalid until the cause is found |
| Winner only in one unplanned segment | Exploratory; design a new test for that segment |
| Revenue metric very noisy | Use conversion as primary and revenue per user as guardrail, or more data |
| Stakeholder wants to ship a null | Explain the cost and risk; ship only for non-metric reasons, stated plainly |
| Effect fades over time | Report the long-run effect; consider novelty |

## Handoffs to related skills
- Design of the next test: `experiment-design`
- Backlog updates and library: `growth-experiment-backlog`
- Impact on forecasts: `growth-model`
- Reporting wins: `growth-reporting`

## Worked example
A pricing page test showed the variant raising sign-ups by 8% with p = 0.03. The readout first ran an SRM check and found a 52/48 split instead of 50/50, traced to a redirect in the variant that dropped some bot traffic only in control. After filtering bots consistently, the split balanced and the effect fell to 3% with an interval including zero. Revenue per visitor, the guardrail, was flat. The decision: stop, fix the redirect implementation for future tests, and test a bolder pricing presentation next.

## Output format
The readout template above, plus a one-line entry for the learning library.

## Common mistakes
- Skipping SRM and tracking checks.
- Declaring winners from unplanned segments.
- Treating "not significant" as "no effect" in underpowered tests.
- Stopping early when results look good.
- Ignoring guardrails and long-term effects.

## Questions to ask before you conclude
- Did the split and exposure work as planned?
- Was the test powered for the effect we care about?
- Is the effect large enough to matter for the business?

## Self-check before you answer
- Did quality checks pass?
- Are effects reported with intervals and guardrails?
- Are segment findings labelled exploratory unless pre-registered?
- Is there a clear decision and lesson?

## Further reading
- Kohavi, Tang and Xu, Trustworthy Online Controlled Experiments (2020)
- Fabijan et al., Diagnosing Sample Ratio Mismatch in Online Controlled Experiments (KDD 2019)

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/experiment-readout/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
