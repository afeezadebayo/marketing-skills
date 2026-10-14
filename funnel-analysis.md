---
name: funnel-analysis
description: "Build and analyse funnels from event data to find where and for whom value leaks: step definitions with windows, step and overall conversion, time between steps, segment breakdowns by device, channel, plan and cohort, opportunity sizing, diagnosis with recordings, surveys and support tickets, evidence-based hypotheses for the backlog and weekly monitoring. Use whenever someone asks for funnel analysis, conversion drop-off, why users don't convert, sign-up or activation funnels, checkout drop-off, where the biggest leak is or how to size a funnel opportunity."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/funnel-analysis/
  category: marketing
  subcategory: growth-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Funnel Analysis

A funnel shows how many people move through each step towards a goal: visit, sign up, activate, pay, renew. The point isn't the chart; it's finding the step where the most value is lost, understanding why, and choosing what to fix. Many funnel analyses stop at "conversion is low at step three", which describes the problem without explaining it.

This skill builds funnels from event data, segments them to find where and for whom value leaks, combines numbers with qualitative evidence to explain the leak, sizes the opportunity and turns it into experiments.

## Operating principles
1. **Define steps from events.** Each step is a tracked event with a clear definition and time window.
2. **Segment before concluding.** Averages hide problems; device, channel, plan and cohort often explain differences.
3. **Size the opportunity.** A small improvement at a high-volume step can beat a big one at a low-volume step.
4. **Find the why.** Recordings, surveys, interviews and support tickets explain what numbers can't.
5. **End with experiments.** A funnel analysis that doesn't change the backlog was a report, not an analysis.

## Common funnels
| Business | Funnel |
|---|---|
| SaaS self-serve | Visit, sign-up, onboarding step(s), activation, trial to paid, retained month 2 |
| E-commerce | Visit, product view, add to cart, checkout start, purchase, repeat purchase |
| Marketplace | Search, listing view, contact or request, transaction, review |
| Mobile app | Install, open, sign-up, key action, day-7 return, subscription |
| B2B sales-led | Visit, lead, MQL, SQL, opportunity, won |

## When to use, and when not to
Use it when a conversion rate drops, when planning experiments, after a redesign, when comparing channels or segments, and in growth audits.

Don't use it for long-term retention curves (`cohort-retention-analysis`) or landing page tests specifically (the Performance Marketing `landing-page-cro` skill).

## Inputs to ask for, in one message
1. The goal and the steps between entry and goal.
2. Event data or analytics access (GA4, Amplitude, Mixpanel, PostHog, warehouse).
3. Segments of interest: device, channel, plan, country, new versus returning.
4. Qualitative sources: recordings, surveys, support tickets, interviews.
5. Recent changes (releases, campaigns, pricing).

## Workflow

### Step 1. Define the funnel
List steps as events, with the time window (for example sign-up to activation within 7 days) and whether steps must happen in order.

### Step 2. Measure overall conversion
Step-to-step and overall conversion, plus median time between steps.

### Step 3. Segment
Break down by device, channel, plan, country, cohort and new versus returning. Look for segments with very different conversion.

### Step 4. Size the opportunity
For each step: users lost × value per converted user. Model what a realistic improvement (for example closing half the gap to the best segment) would add.

### Step 5. Diagnose the why
Watch session recordings at the leaking step, run a one-question survey ("What stopped you?"), read support tickets and talk to users.

### Step 6. Form hypotheses
Write evidence-based hypotheses for the biggest leaks.

### Step 7. Feed the backlog
Score hypotheses and add them to the experiment backlog.

### Step 8. Monitor
Track the funnel weekly with alerts for sudden drops.

## Opportunity sizing example
| Step | Users entering | Conversion | Best segment conversion | Users gained if gap halved | Value per user | Monthly value |
|---|---|---|---|---|---|---|
| Sign-up to activation | 10,000 | 22% | 35% (desktop) | 650 | £40 | £26,000 |
| Activation to paid | 2,200 | 18% | 24% (team plans) | 66 | £300 | £19,800 |
Illustrative; use your own values.

## Qualitative methods at the leaking step
| Method | What it shows | Effort |
|---|---|---|
| Session recordings | Where people hesitate, error out or rage-click | Low |
| One-question exit survey | "What stopped you?" in users' words | Low |
| Support ticket review | Recurring problems and confusion | Low |
| Five-user usability test | Why the step is hard | Medium |
| Customer interviews | Motivations and alternatives | Medium |
Five to ten recordings or interviews at the leaking step usually reveal the main pattern.

## Funnel health dashboard
- Step conversion and overall conversion, weekly, with last year and target.
- Segment view for device, channel and plan.
- Median time between key steps.
- Alerts when any step falls by more than its normal weekly variation.
- Annotations for releases, campaigns and tracking changes.

## Open versus closed funnels
| Type | Counts | Use when |
|---|---|---|
| Closed (strict order) | Users who complete steps in sequence | The path is fixed (checkout, sign-up form) |
| Open (any order) | Users who complete each step at any point | Users can skip or reorder steps (onboarding checklists) |
| Path analysis | The actual routes users take | You don't know the real path yet |
Choose deliberately; the same data can show very different conversion depending on the type.

## Funnel query example (SQL)
```sql
WITH s AS (
  SELECT user_id,
         MIN(CASE WHEN event = 'signed_up' THEN ts END) AS signed_up,
         MIN(CASE WHEN event = 'connected_bank' THEN ts END) AS connected,
         MIN(CASE WHEN event = 'first_transaction' THEN ts END) AS activated
  FROM events
  WHERE ts >= '2026-09-01'
  GROUP BY user_id
)
SELECT COUNT(signed_up) AS signed_up,
       COUNT(CASE WHEN connected <= signed_up + INTERVAL '14 days' THEN 1 END) AS connected_14d,
       COUNT(CASE WHEN activated <= signed_up + INTERVAL '14 days' THEN 1 END) AS activated_14d
FROM s WHERE signed_up IS NOT NULL;
```
Adapt event names and date syntax to your warehouse.

## Funnel review cadence
- Weekly: step conversion against last year and target, with alerts.
- Monthly: segment breakdowns and the largest gaps.
- Quarterly: full analysis with sizing, diagnosis and a refreshed hypothesis list.
Annotate every release, campaign and tracking change so movements can be explained.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Steps out of order | Use open funnels or path analysis instead of strict sequences |
| Long time between steps | Use cohort-based funnels with appropriate windows |
| Tracking gaps | Fix tracking before drawing conclusions (`tracking-plan`) |
| Small numbers | Combine periods; focus on large differences; add qualitative evidence |
| Sudden drop | Check releases, tracking changes and traffic mix before redesigning |

## Handoffs to related skills
- Experiments: `experiment-design`, `growth-experiment-backlog`
- Retention after the funnel: `cohort-retention-analysis`
- Event definitions: `tracking-plan`
- Weekly monitoring: `growth-reporting`
- Landing pages for paid traffic: the Performance Marketing `landing-page-cro` skill

## Worked example
A fintech app's sign-up to activation conversion (first card transaction within 14 days) was 22%. Segmenting showed Android users converted at half the rate of iOS users, mostly at identity verification. Recordings revealed the camera step failed on many older Android phones, and support tickets confirmed it. Sizing showed closing half the gap was worth more than any other funnel change. The team added a document upload fallback and clearer instructions; an experiment confirmed a large lift in Android verification completion and activation.

## Output format
```
# Funnel analysis: <funnel>, <date>
## Funnel definition (steps, events, windows)
## Overall conversion and time between steps
## Segment breakdown and biggest gaps
## Opportunity sizing
## Diagnosis (quantitative and qualitative evidence)
## Hypotheses and backlog entries
## Monitoring and alerts
```

## Common mistakes
- Concluding from averages without segmenting.
- Optimising low-volume steps first.
- Describing leaks without explaining them.
- Trusting funnels with broken tracking.
- Analyses that never become experiments.

## Questions to ask before you analyse
- What is the goal, and which events define each step?
- Which segments might behave differently?
- What changed recently in the product or traffic?

## Self-check before you answer
- Are steps defined from events with windows?
- Did I segment and size opportunities?
- Did I combine numbers with qualitative evidence?
- Did hypotheses go into the backlog?

## Further reading
- Amplitude, funnel analysis guides: https://amplitude.com/blog
- PostHog, funnels documentation: https://posthog.com/docs/product-analytics/funnels

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/funnel-analysis/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
