---
name: growth-reporting
description: "Build growth reporting around the north star and metric tree: a metric dictionary, north star and input views against targets, channel quality by activation and retention, cohort curves, labelled attribution combining last touch, self-reported and test-based evidence, experiment impact, annotations and a weekly growth review that ends with decisions. Use whenever someone asks for a growth dashboard, weekly growth report, growth metrics review, attribution for growth, 'how did you hear about us' data, board growth reporting or why growth numbers disagree."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/growth-reporting/
  category: marketing
  subcategory: growth-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Growth Reporting and Attribution

Growth reporting should answer three questions every week: are we on track for the goal, what changed and why, and what are we doing about it? Most dashboards answer none of them. They show dozens of charts, mix vanity metrics with real ones, and credit growth to whichever channel the attribution model favours. Teams spend meetings debating numbers instead of decisions.

This skill builds growth reporting around the north star and metric tree, with clear definitions, attribution that is labelled for what it is, cohort and channel views, experiment impact and a weekly review that ends with decisions.

## Operating principles
1. **North star first.** Every report starts with the north star and its inputs against targets.
2. **One definition per metric,** shared across tools and teams.
3. **Attribution is a lens, not the truth.** Label models, compare with self-reported and test-based evidence.
4. **Explain changes.** A number without the reason is trivia.
5. **Decisions, not decoration.** Reports end with actions and owners.

## Report layers
| Layer | Contents | Audience |
|---|---|---|
| North star and inputs | Current value, target, trend, week-on-week and year-on-year | Everyone |
| Acquisition | New users by channel with quality (activation, retention) | Growth and marketing |
| Activation and engagement | Funnel conversion, time to value, depth of use | Product and growth |
| Retention | Cohort curves, churn, NRR | Leadership, product |
| Monetisation | Conversion to paid, ARPU, expansion | Leadership, finance |
| Experiments | Launched, completed, wins, measured impact | Growth team |
| Annotations | Releases, campaigns, incidents, seasonality | Everyone |

## Attribution approaches for growth
| Approach | Strength | Limit |
|---|---|---|
| First touch | Shows what introduced users | Ignores what convinced them |
| Last touch | Simple, close to conversion | Over-credits bottom-funnel channels |
| Multi-touch | Spreads credit | Depends on tracking; still not causal |
| Self-reported ("How did you hear?") | Captures dark social, podcasts, word of mouth | Memory bias |
| Incrementality tests | Causal | Point-in-time; needs volume |
| Marketing mix modelling | Full-channel view | Needs history |
Combine at least two (for example last touch plus self-reported) and use tests for big decisions.

## When to use, and when not to
Use it to build or rebuild growth dashboards, set up the weekly growth review, prepare board or leadership updates and settle attribution debates.

Don't use it for paid media reporting in depth (the Performance Marketing `paid-media-reporting` skill) or for lifecycle email reporting (the CRM and Lifecycle reporting skill).

## Inputs to ask for, in one message
1. North star, metric tree and targets.
2. Data sources and tools (analytics, warehouse, BI).
3. Current dashboards and how they're used.
4. Attribution setup and any self-reported source data.
5. Experiment log.
6. Who attends the weekly review and what decisions they make.

## Workflow

### Step 1. Define metrics
A metric dictionary with formulas, sources, owners and refresh times.

### Step 2. Build the north star view
North star and inputs with targets from the growth model, trends and annotations.

### Step 3. Add channel quality
New users by channel with downstream activation, retention and revenue, not just volume.

### Step 4. Add cohorts
Retention and revenue curves by cohort and segment.

### Step 5. Label attribution
Show the model used; add self-reported source data; reference incrementality tests where available.

### Step 6. Add experiment impact
Experiments launched and completed, wins shipped and their estimated impact on inputs.

### Step 7. Run the weekly review
A fixed agenda: north star and inputs, what changed and why, experiment results, decisions and owners.

### Step 8. Keep it clean
Retire unused charts quarterly; fix definitions when they drift.

## Weekly growth report template
```
# Growth weekly: <week>
## North star: value, target, trend, one-line explanation
## Inputs (new activated, retained, reactivated; conversion; ARPU) vs target
## What changed and why (with annotations)
## Channel quality (volume, activation, week-4 retention)
## Experiments: completed, results, decisions
## Decisions and owners for next week
```

## Self-reported attribution
Add a short, open or multiple-choice "How did you hear about us?" question at sign-up or checkout. Group answers (search, podcast, friend, community, social, other) and compare with last-touch attribution each month. Large gaps usually reveal word of mouth, podcasts, communities and AI assistants that tracking misses.

| Channel | Last-touch share | Self-reported share | Interpretation |
|---|---|---|---|
| Paid search | 38% | 14% | Search captures demand created elsewhere |
| Podcasts | 1% | 17% | Under-credited; consider a test |
| Friend or colleague | 0% | 22% | Word of mouth strong; referral programme candidate |
| AI assistant (ChatGPT, Perplexity) | 2% | 6% | Emerging; track with AEO work |
Illustrative numbers.

## Channel quality view
| Channel | New users | Activation rate | Week-4 retention | Paid conversion | Cost per retained user |
|---|---|---|---|---|---|
Judging channels by retained users rather than sign-ups often reverses rankings.

## Metric dictionary example
| Metric | Definition | Source | Owner |
|---|---|---|---|
| Weekly active teams | Teams with 50+ messages from 2+ members in 7 days | Warehouse | Growth analyst |
| Activation rate | New teams reaching activation within 7 days ÷ new teams | Product analytics | Growth PM |
| Week-4 retention | Activated teams active in week 4 ÷ activated teams | Warehouse | Analyst |
| Cost per retained team | Channel spend ÷ teams retained at week 4 | Warehouse + ad spend | Acquisition lead |

## Board update structure
North star and trend, revenue and retention, efficiency (CAC and payback), the two biggest wins and the two biggest risks, and what the team will do next quarter.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Numbers disagree between tools | Pick one source of truth per metric; document why others differ |
| Dark social and word of mouth significant | Add self-reported attribution at sign-up |
| Board wants simple numbers | North star, revenue, retention and burn or efficiency, with context |
| Long B2B cycles | Report pipeline by source and cohort, not monthly revenue alone |
| Too many dashboards | Consolidate into one growth report with drill-downs |

## Handoffs to related skills
- Metric tree and targets: `north-star-metric-tree`, `growth-model`
- Funnel and cohort detail: `funnel-analysis`, `cohort-retention-analysis`
- Experiment impact: `experiment-readout`
- Event definitions: `tracking-plan`
- Paid media reporting: the Performance Marketing `paid-media-reporting` skill

## Worked example
A B2B SaaS growth team reviewed four dashboards with conflicting sign-up numbers and argued about channel credit every week. The new reporting defined each metric once in the warehouse, led with weekly active teams and its inputs against targets, showed channels by activated and retained teams rather than sign-ups, added a "How did you hear about us?" field that revealed podcasts and communities driving far more than last-touch credited, and listed experiment results with decisions. Meetings shifted from debating numbers to deciding actions, and budget moved towards community and podcast sponsorship after a small geo test confirmed the effect.

## Output format
```
# Growth reporting plan: <company>, <date>
## Metric dictionary
## North star and input views
## Channel quality and attribution approach
## Cohort views
## Experiment impact tracking
## Weekly review agenda and owners
```

## Common mistakes
- Dashboards without targets or explanations.
- Several definitions of the same metric.
- Treating last-touch attribution as truth.
- Channel reports by volume only.
- Reviews that end without decisions.

## Questions to ask before you build
- What decisions does the weekly review make?
- Which source is the truth for each metric?
- How do users say they found you, in their own words?

## Self-check before you answer
- Does the report start with the north star and inputs against targets?
- Are metrics defined once and attribution labelled?
- Are channels judged on downstream quality?
- Does every report end with decisions and owners?

## Further reading
- Amplitude North Star Playbook: https://amplitude.com/books/north-star
- GA4 attribution settings: https://support.google.com/analytics/answer/10596866

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/growth-reporting/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
