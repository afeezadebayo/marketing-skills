---
name: marketing-mix-modelling
description: "Scope, build or review a marketing mix model with Google Meridian, Meta Robyn or PyMC-Marketing: two to three years of weekly first-party data, adstock and saturation, price, promotions and seasonality, calibration with lift and geo tests, validation, contribution, ROI and marginal ROI with ranges, response curves and budget scenarios. Use whenever someone asks about marketing mix modelling, MMM, Meridian, Robyn, media mix, measuring TV or YouTube, budget allocation without cookies, or how channels really contribute to sales."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/marketing-mix-modelling/
  category: marketing
  subcategory: performance-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Marketing Mix Modelling

Marketing mix modelling (MMM) estimates how each channel contributes to sales using aggregated data over time: weekly spend, impressions, prices, promotions, seasonality and outside factors. It needs no user-level tracking, so it survives consent rules, cookie limits and walled gardens. Open-source tools such as Google's Meridian and Meta's Robyn have made it practical for mid-sized advertisers, not just big brands with consultancies.

This skill scopes, builds or reviews an MMM, calibrates it with experiments, and turns its outputs (contribution, ROI, response curves) into budget decisions.

## Operating principles
1. **Garbage in, garbage out.** Two to three years of clean weekly data matter more than model choice.
2. **Calibrate with experiments.** Lift and geo tests anchor the model to causal evidence.
3. **Show uncertainty.** Every ROI estimate comes with a range; decisions should respect it.
4. **Model what you can change.** Include controllable levers (spend by channel, price, promotions) and important outside factors.
5. **Use it to plan, not to grade.** MMM is best at allocation and scenario planning, not daily optimisation.

## When to use, and when not to
Use it when spending across several channels (typically including offline or upper-funnel media), when attribution is unreliable because of consent or walled gardens, for annual and quarterly planning, and to settle debates between platform claims.

Don't use it for very small budgets or one or two channels with little variation (test instead with `incrementality-testing`), or for daily bid decisions.

## Inputs to ask for, in one message
1. Two to three years of weekly data: sales or conversions (from your own systems), spend and impressions by channel.
2. Prices, promotions, discounts and distribution changes.
3. Seasonality markers, holidays, weather or macro factors relevant to the business.
4. Competitor activity if known.
5. Lift or geo test results for calibration.
6. The planning questions the model must answer.

## Workflow

### Step 1. Define the questions
Allocation across channels, optimal total budget, the value of upper-funnel media, the effect of price and promotions.

### Step 2. Prepare data
Weekly, consistent definitions, no gaps, spend and impressions by channel, outcome from your own systems. Document every transformation.

### Step 3. Choose the tool
| Tool | Approach | Notes |
|---|---|---|
| Google Meridian | Bayesian, open source, supports geo-level data and calibration priors | Good for advertisers with regional data and experiment results |
| Meta Robyn | Open source (R), ridge regression with automated hyperparameter search | Mature community, many examples |
| PyMC-Marketing | Bayesian, Python | Flexible for analysts comfortable with PyMC |
| Vendor or consultancy models | Varies | Ask for transparency on assumptions and validation |

### Step 4. Specify the model
Adstock (carryover) and saturation (diminishing returns) for each channel; baseline and seasonality; price and promotion effects; external factors.

### Step 5. Calibrate
Use lift and geo test results as priors or constraints for the channels they cover.

### Step 6. Validate
Out-of-sample fit, sensible coefficients (no negative effects for media that clearly can't hurt sales), stability across runs, comparison with test results.

### Step 7. Interpret
Contribution by channel, ROI and marginal ROI with ranges, response curves, carryover lengths.

### Step 8. Plan
Run budget scenarios with the response curves; recommend allocation changes within the uncertainty; plan tests for the least certain channels.

### Step 9. Refresh
Update quarterly or twice a year with new data and new tests.

## Reading MMM outputs
| Output | What it tells you | Watch out for |
|---|---|---|
| Contribution | Share of sales attributed to each driver | Baseline often large; that's normal |
| ROI | Average return per pound | Average, not marginal |
| Marginal ROI | Return on the next pound | The number for allocation decisions |
| Response curve | How sales change with spend | Extrapolation beyond observed spend is risky |
| Adstock | How long effects last | Long carryover favours steady spend |

## Data checklist
- At least 104 weeks of data, ideally 156.
- Spend varies over time in each channel (models can't learn from flat lines).
- Outcome from finance or commerce systems, not ad platforms.
- Promotions and price changes recorded weekly.
- Major events logged (stock-outs, site outages, PR spikes).

## Key concepts in plain words
| Concept | Meaning | Example |
|---|---|---|
| Adstock (carryover) | Effects of advertising continue after the ad runs | A TV burst still lifts sales two weeks later |
| Saturation | Each extra pound adds less than the one before | Doubling search spend doesn't double sales |
| Baseline | Sales that would happen without paid media | Brand strength, organic, repeat customers |
| Priors (Bayesian models) | Starting beliefs, updated by data | A geo test showing YouTube iROAS around a value |
| Marginal ROI | Return on the next unit of spend | Used to decide where the next pound goes |

## Validation checks before trusting a model
1. Holdout fit: predict the last 8 to 12 weeks without training on them; compare with actuals.
2. Coefficient sense: media effects positive, price effects in the expected direction.
3. Stability: rerun with different seeds or slightly different data; results shouldn't swing wildly.
4. Test agreement: channels with lift tests should land near the tested values.
5. Business sense: contribution and ROI should be explainable to someone who knows the market.

## Turning outputs into a budget decision
- Rank channels by marginal ROI at current spend, not average ROI.
- Move budget from low marginal ROI to high marginal ROI channels in steps (for example 10 to 20%).
- Stay within the observed spend range; flag scenarios that extrapolate.
- Pair each major shift with a confirming geo test.
- Re-run the model after the next quarter of data.

## Working with a vendor model
Ask for: the data used and its sources, the model specification, how adstock and saturation were set, calibration with experiments, validation results, uncertainty ranges and the ability to run your own scenarios. Avoid models that only output a single ROI per channel with no ranges or methodology.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Channels always move together | The model can't separate them; create variation through tests |
| Very short history | Start with tests; build MMM when data accumulates |
| Model says a channel has negative ROI | Check data and priors; negative media effects are usually artefacts |
| Results disagree with tests | Trust well-run tests and recalibrate |
| Leadership wants one number | Show the range and the decision it supports |

## Handoffs to related skills
- Calibration experiments: `incrementality-testing`
- Budget plans from the model: `media-planning-budgeting`
- Reporting: `paid-media-reporting`
- Data and tracking quality: `conversion-tracking-capi`

## Worked example
A mid-sized consumer brand spent across search, Meta, YouTube, TV and retail media. Attribution credited search with most sales and gave TV almost nothing. Using Meridian with three years of weekly regional data and two geo test results as priors, the model found TV and YouTube had long carryover and drove brand search, while non-brand search was close to saturation. Scenarios suggested moving a modest share of search budget into YouTube. A follow-up geo test confirmed YouTube lift, and the next quarter delivered more sales at the same budget.

## Output format
```
# MMM plan or review: <business>, <date>
## Questions the model answers
## Data inventory and gaps
## Tool and specification (adstock, saturation, controls)
## Calibration with tests
## Validation results
## Outputs: contribution, ROI, marginal ROI with ranges, response curves
## Budget scenarios and recommendations
## Refresh and test plan
```

## Common mistakes
- Using ad platform conversions as the outcome.
- Too little data or no spend variation.
- Ignoring price and promotions.
- Reporting ROI without ranges.
- Using average ROI instead of marginal ROI for allocation.

## Questions to ask before you model
- Which decisions should the model support?
- How many weeks of clean data exist, and does spend vary?
- Which channels have experiment results for calibration?

## Self-check before you answer
- Is the data sufficient and from first-party sources?
- Are adstock, saturation, price and seasonality modelled?
- Is the model calibrated with tests and validated?
- Are recommendations within the uncertainty ranges?

## Official documentation and tools
- Google Meridian: https://developers.google.com/meridian
- Meta Robyn: https://facebookexperimental.github.io/Robyn/
- PyMC-Marketing: https://www.pymc-marketing.io/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/marketing-mix-modelling/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
