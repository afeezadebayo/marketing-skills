---
name: growth-experiment-backlog
description: "Set up and run a growth experimentation system: ideas tied to the metric tree from data, research and support, one backlog, ICE, PIE or RICE prioritisation calibrated by growth model sensitivity, a weekly growth meeting, experiment cards, a tagged learning library and velocity and win-rate tracking. Use whenever someone asks how to run growth experiments, build an experiment backlog, prioritise growth ideas, run a growth meeting, increase experiment velocity or document test results."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/growth-experiment-backlog/
  category: marketing
  subcategory: growth-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Growth Experiment Backlog and Cadence

The growth teams that win aren't the ones with the best single idea; they're the ones that learn fastest. That takes a system: a backlog of ideas tied to the metric tree, a consistent way to prioritise, a weekly rhythm for launching and reviewing experiments, and a record of what was learned. Without it, teams run whatever the loudest person suggests, forget past results and repeat failed tests.

This skill sets up and runs a growth experimentation process: idea generation, the backlog, prioritisation, the weekly growth meeting, experiment documentation and a learning library.

## Operating principles
1. **Tie every idea to a metric.** Each idea names the input metric it should move.
2. **Prioritise consistently.** Use one scoring method and revisit scores as evidence arrives.
3. **Cadence beats heroics.** A steady weekly rhythm compounds learning.
4. **Write it down.** Hypotheses, designs, results and decisions in one place.
5. **Celebrate learning, not just wins.** Null and negative results prevent repeated mistakes.

## Idea sources
| Source | Example |
|---|---|
| Funnel and cohort data | Activation drops at step 3 for mobile users |
| Customer research | Interviews show confusion about pricing tiers |
| Support tickets | Many questions about importing data |
| Competitor and market scans | A competitor added a free tool that ranks well |
| Past experiments | A winning onboarding change could apply elsewhere |
| Team brainstorms on one metric | "How might we raise week-1 retention?" |

## Prioritisation frameworks
| Framework | Scores | Best for |
|---|---|---|
| ICE | Impact, confidence, ease (1 to 10) | Fast, simple backlogs |
| PIE | Potential, importance, ease | Page and funnel optimisation |
| RICE | Reach, impact, confidence, effort | Larger initiatives with known reach |
Pick one and use it consistently; calibrate impact against the growth model's sensitivity.

## When to use, and when not to
Use it when starting a growth team, when experiments are ad hoc, when velocity is low, when results aren't shared, and when planning a quarter's experiments.

Don't use it to design a single test in detail (`experiment-design`) or analyse results (`experiment-readout`).

## Inputs to ask for, in one message
1. The north star and metric tree, with owners.
2. Current ideas, wherever they live.
3. Past experiments and results.
4. Team size, engineering and design capacity for experiments.
5. Tools: experimentation platform, analytics, project tracker.

## Workflow

### Step 1. Set up the backlog
One list (spreadsheet, Notion, Linear or Jira) with fields: idea, hypothesis, target metric, lever, ICE scores, effort, owner, status, links.

### Step 2. Fill it
Run focused ideation on the input metric the growth model ranks highest. Pull ideas from data, research and support.

### Step 3. Prioritise
Score with ICE or RICE. Adjust impact using the model: a 5% gain on a high-sensitivity input beats a 20% gain on a low one.

### Step 4. Plan the week
Pick experiments that fit capacity, mixing quick wins and bigger bets; check traffic so tests don't collide on the same users.

### Step 5. Run the weekly growth meeting
A fixed 45 to 60 minute agenda: metrics review, last week's results, this week's launches, backlog grooming.

### Step 6. Document each experiment
Hypothesis, design, metrics, sample size, dates, result, decision and lessons.

### Step 7. Build the learning library
Tag experiments by area, lever and outcome; review quarterly for patterns.

### Step 8. Track velocity and win rate
Experiments launched per week, completion rate, share with a clear result, and impact on input metrics.

## Weekly growth meeting agenda
```
1. North star and input metrics vs target (10 min)
2. Experiment results and decisions (15 min)
3. Launches this week and owners (10 min)
4. Backlog: new ideas and re-scoring (10 min)
5. Blockers and asks (5 min)
```

## Experiment card template
```
Name:
Target input metric:
Hypothesis: Because [evidence], we believe [change] for [audience] will [effect on metric].
Design (A/B, holdout, before/after):
Primary metric and guardrails:
Sample size and expected duration:
Launch and end dates:
Result (with interval):
Decision (ship, iterate, stop) and lessons:
```

## Ideation session format (60 minutes)
1. Share the target input metric and its current value (5 min).
2. Review relevant data: funnel, cohorts, research quotes (10 min).
3. Silent idea writing, one idea per card with the metric it moves (15 min).
4. Group and discuss (15 min).
5. Quick ICE scoring (10 min).
6. Pick owners for the top ideas (5 min).

## Velocity metrics
| Metric | Definition | Healthy direction |
|---|---|---|
| Experiments launched per week | Count of tests started | Steady or rising |
| Completion rate | Tests that reached planned sample | High |
| Clear result rate | Tests with a conclusive outcome | Rising as sizing improves |
| Win rate | Share with positive significant results | Often 20 to 40%; very high may mean tests are too safe |
| Input metric impact | Sum of shipped wins' measured effects | Rising |

## Learning library tags
Area (acquisition, activation, retention, monetisation, referral), lever (copy, design, pricing, onboarding step, channel), audience, outcome (win, loss, null), effect size and a one-line lesson. Quarterly reviews of the library reveal which levers reliably move which metrics.

## Backlog hygiene
- Archive ideas untouched for two quarters unless new evidence appears.
- Merge duplicates and link related ideas.
- Re-score ideas when the growth model or north star changes.
- Keep a "parked" status for good ideas blocked by engineering, with the dependency noted.
- Review the top 20 every week and the full list every month.

## Coordinating with product and engineering
Agree a fixed share of each sprint for growth experiments, a lightweight review for experiment code, and feature flags so tests can be launched and stopped without full releases.

Share a monthly digest of results with the wider company to spread what the team learns.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Low traffic | Fewer, bigger tests; qualitative research; sequential tests where appropriate |
| Engineering bottleneck | Favour no-code tests (copy, pricing pages, emails) and plan engineering experiments a sprint ahead |
| Leadership wants only wins | Show the value of nulls: money saved and mistakes avoided |
| Many teams testing on the same users | Coordinate through a shared calendar and mutually exclusive groups |
| Big strategic bets | Run them as tracked initiatives with milestones, not as A/B tests |

## Handoffs to related skills
- Metric tree: `north-star-metric-tree`
- Lever sensitivity: `growth-model`
- Test design: `experiment-design`
- Analysis: `experiment-readout`
- Reporting: `growth-reporting`

## Worked example
A consumer finance app shipped two or three experiments a quarter, chosen by the founders. The new process created one backlog tied to the metric tree, scored ideas with ICE weighted by model sensitivity, introduced a weekly growth meeting and experiment cards. Velocity rose to three to four experiments a week, mostly onboarding copy, email and pricing page tests. After a quarter, the library showed that reducing steps beat adding education in onboarding, which shaped the next quarter's bigger product changes.

## Output format
```
# Growth experimentation system: <company>, <date>
## Backlog structure and fields
## Prioritisation method and calibration
## Weekly meeting agenda and owners
## Experiment card template
## Learning library tags
## Velocity and win-rate metrics
```

## Common mistakes
- Ideas with no target metric.
- Inconsistent prioritisation driven by opinion.
- No regular cadence, so tests stall.
- Results not documented or shared.
- Overlapping tests contaminating each other.

## Questions to ask before you set up
- Which input metric matters most this quarter?
- How much experiment capacity does the team have?
- Where are past results recorded, if anywhere?

## Self-check before you answer
- Is every idea tied to a metric?
- Is prioritisation consistent and calibrated?
- Is there a weekly cadence with owners?
- Are results documented in a searchable library?

## Further reading
- Sean Ellis and Morgan Brown, Hacking Growth (2017)
- GrowthBook documentation (open-source experimentation): https://docs.growthbook.io/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/growth-experiment-backlog/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
