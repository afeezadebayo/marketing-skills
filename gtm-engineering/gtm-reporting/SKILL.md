---
name: gtm-reporting
description: "Report GTM and outbound results from source to revenue: agreed funnel definitions, attribution by workflow, segment, signal, play and copy version, reply classification, health and unit-cost metrics, dashboards for operators, teams and leaders, weekly and monthly templates and experiments on the weakest stage. Use whenever someone needs outbound or GTM reporting, a pipeline dashboard for Clay workflows, meeting and opportunity metrics instead of opens, results by segment or signal, or a monthly report for leadership."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/gtm-reporting/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-13"
---

# GTM Reporting

Outbound and GTM automation are often judged on the wrong numbers: emails sent, open rates (unreliable since mail privacy features began loading images automatically) and total replies, including "unsubscribe" and "not interested". These numbers rise while pipeline stays flat. Leaders need to see whether the system produces qualified meetings, opportunities and revenue, at what cost, and which segments, signals, plays and copy drive the results.

This skill builds GTM reporting from source to revenue: a full funnel with clear definitions, attribution of meetings and pipeline to workflows, segments, signals, plays and prompt versions, data quality and deliverability health metrics, unit costs, dashboards for different audiences, a weekly and monthly reporting rhythm and experiments to improve weak stages.

## Operating principles
1. **Pipeline over activity.** Meetings, opportunities and revenue are the outcome metrics.
2. **Define every metric.** "Positive reply" and "meeting held" mean the same thing to everyone.
3. **Attribute to the cause.** Results by segment, signal, play, sequence and copy version.
4. **Health and cost alongside results.** Deliverability and unit costs explain changes.
5. **Reports drive decisions.** Every report ends with what to keep, change or stop.

## The GTM funnel
| Stage | Definition | Typical owner |
|---|---|---|
| Accounts sourced | Accounts added to a workflow | GTM engineer |
| Accounts qualified | Accounts in tiers A or B | GTM engineer |
| Contacts ready | Contacts with verified email and QA pass | GTM engineer |
| Contacted | Contacts who received at least one step | SDR or automation |
| Delivered | Sent minus bounces | Automation |
| Replies | Any human reply | SDR |
| Positive replies | Interested, asked a question or referred | SDR |
| Meetings booked | Meeting scheduled | SDR |
| Meetings held | Meeting happened with a qualified person | AE |
| Opportunities | Qualified opportunity created in CRM | AE |
| Closed won | Revenue | AE |

## Core metrics
| Metric | Formula |
|---|---|
| Qualification rate | Qualified accounts / sourced accounts |
| Match rate | Contacts with valid email / contacts sought |
| Bounce rate | Bounces / sent |
| Positive reply rate | Positive replies / delivered |
| Meeting rate | Meetings held / delivered (or per 1,000 contacted) |
| Show rate | Meetings held / meetings booked |
| Opportunity rate | Opportunities / meetings held |
| Win rate | Closed won / opportunities |
| Pipeline created | Value of opportunities from the workflow |
| Cost per meeting and opportunity | Total spend / meetings or opportunities |
| Time to meeting | Days from first touch to meeting |

## When to use, and when not to
Use it to set up GTM dashboards, run weekly and monthly reviews, report to leadership, compare workflows and decide where to invest.

Don't use it for full marketing attribution across all channels (the Growth Marketing `growth-reporting` skill) or for cost analysis alone (`gtm-cost-control`).

## Inputs
- CRM data with source and workflow stamps.
- Sequencer data: sends, bounces, replies and classifications.
- Table data: sourced, qualified, enriched, QA results, segments, signals, prompt versions.
- Costs by workflow.
- Targets for meetings, pipeline and revenue.

## Workflow

### Step 1. Agree definitions
Write the definition of each funnel stage and metric; agree with sales leadership.

### Step 2. Make attribution possible
Stamp every record with workflow, segment, signal, play and copy version, and carry these into the CRM.

### Step 3. Classify replies
Positive, neutral, negative, out of office, wrong person, unsubscribe; use rules or AI with human checks.

### Step 4. Build the funnel
Counts and conversion rates by stage, overall and by segment, signal and play.

### Step 5. Add health and cost
Match rate, bounce rate, complaint rate, QA pass rate and unit costs per workflow.

### Step 6. Build dashboards
An operator view (daily health and pipeline), a team view (weekly funnel and experiments) and a leadership view (monthly meetings, pipeline, revenue, cost).

### Step 7. Set the rhythm
Weekly: health, funnel, experiments. Monthly: pipeline, revenue, unit costs, decisions. Quarterly: strategy and model updates.

### Step 8. Turn findings into experiments
Pick the weakest stage; test one change at a time with a clear success metric.

## Weekly report template
```
Week <n>
Health: match 76% | bounce 1.4% | QA pass 98.9% | complaints 0.04%
Funnel: contacted 1,820 | positive replies 41 (2.3%) | meetings booked 19 | held 15
Best segment: Fintech UK tier A, 3.8% positive replies
Best signal: new head of growth, 5 meetings
Weakest stage: show rate 79% -> test reminder sequence
Experiments: subject line v5 vs v4 (running), new DACH waterfall (complete: +12% match)
Decisions: pause job-post signal; scale funding play
```

## Monthly leadership summary
```
Meetings held: 64 (target 60) | Opportunities: 21 | Pipeline: £410,000
Wins this month from GTM-sourced opportunities: 3 (£68,000)
Cost per meeting: £72 (ceiling £300) | Pipeline per £1 spent: £44
What worked: funding and new-leader plays
What changes next month: expand tier A in Netherlands; stop generic job-post play
```

## Reply classification guide
| Class | Examples | Counts as positive |
|---|---|---|
| Interested | "Sure, let's talk", "Send more info" | Yes |
| Referral | "Speak to my colleague" | Yes |
| Question | "How does pricing work?" | Yes |
| Not now | "Try next quarter" | No, but schedule follow-up |
| Not interested | "No thanks" | No |
| Unsubscribe | "Remove me" | No; suppress |
| Out of office or wrong person | Auto-replies, left company | No; update records |

## Experiment log
Record each experiment with hypothesis, change, segment, start and end dates, sample size, result and decision, so learning builds over time instead of being repeated.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Long sales cycles | Report pipeline and opportunity rates as leading indicators |
| Open rates requested | Explain unreliability; show replies and meetings instead |
| Several channels touch the same account | Use first-touch and influenced views; avoid double counting |
| Small numbers | Report rolling 4 to 8-week windows; avoid over-reading weekly changes |
| Reply classification disputes | Sample-check AI classifications weekly |
| No CRM source stamps | Start stamping now; estimate history carefully |

## Handoffs to related skills
- Costs: `gtm-cost-control`
- Scoring and tiers: `icp-account-scoring`
- Signals and plays: `signal-based-outbound`
- Copy versions: `ai-copy-columns`
- Deliverability: `outbound-infrastructure`
- Wider growth reporting: the Growth Marketing `growth-reporting` skill

## Worked example
A team reported 12,000 emails sent and a 45% open rate each month, while leadership questioned outbound's value. The new reporting stamped workflow, segment, signal and copy version on every record, classified replies and built a funnel to revenue. It showed 64 meetings and £410,000 of pipeline a month at £72 per meeting, revealed that the funding and new-leader plays drove most meetings while generic job-post triggers produced none, and flagged a weak show rate. The team stopped the weak play, added a reminder sequence that lifted show rate to 88% and secured budget to expand.

## Common mistakes
- Reporting sends and opens.
- Counting all replies as success.
- No source stamps, so results cannot be attributed.
- Reports without decisions.
- Over-reading small weekly numbers.

## Output format
```
1. Metric definitions
2. Attribution fields and stamping plan
3. Funnel by segment, signal and play
4. Health and cost metrics
5. Dashboards by audience
6. Weekly and monthly templates
7. Experiment backlog
```

## Self-check before you answer
- Does reporting reach meetings, opportunities and revenue?
- Are metrics defined and agreed with sales?
- Can results be attributed to segment, signal, play and copy version?
- Does every report end with decisions?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/gtm-reporting/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
