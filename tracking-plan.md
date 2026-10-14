---
name: tracking-plan
description: "Design tracking plans and event taxonomies for product analytics in Amplitude, Mixpanel, PostHog, GA4, Segment, RudderStack or the warehouse: events tied to metrics, object_action naming, event, user and group properties, identity and consent rules, client versus server decisions, audits of messy tracking, QA before release and governance with owners. Use whenever someone asks for a tracking plan, event taxonomy, analytics instrumentation, naming conventions for events, why analytics numbers disagree, cleaning up events or preparing analytics for a new app."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/tracking-plan/
  category: marketing
  subcategory: growth-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Tracking Plan and Event Taxonomy

Every growth decision depends on data, and most data problems start with tracking: events named differently on web and app, properties missing on half the events, activation defined three ways in three dashboards, and nobody sure what "signed_up" actually means. A tracking plan fixes this. It is a living document that defines which events and properties are tracked, why, where and how they're named, and who owns them.

This skill designs tracking plans and event taxonomies for product analytics (Amplitude, Mixpanel, PostHog, GA4, Segment, RudderStack or warehouse-first setups), audits existing tracking and sets governance so data stays trustworthy.

## Operating principles
1. **Track decisions, not everything.** Each event exists because a metric or question needs it.
2. **Consistent naming.** One convention (for example object_action in lower snake case) across platforms.
3. **Properties carry context.** Fewer events with rich properties beat many near-duplicate events.
4. **One definition per metric.** Activation, active user and conversion are defined once and reused.
5. **Governance keeps it clean.** Owners, reviews and QA before releases.

## Event design
| Element | Guidance | Example |
|---|---|---|
| Event name | object_action, past tense, lower snake case | project_created, invoice_sent |
| Event properties | Context about the action | template_used, item_count, source |
| User properties | Who the user is | plan, role, signup_channel, country |
| Group properties (B2B) | Account or workspace context | company_size, account_plan |
| Identity | Anonymous ID before sign-up, user ID after, merged | Consistent across web and app |
| Consent | Respect consent for analytics and advertising | Consent state recorded |

## When to use, and when not to
Use it when starting analytics, when numbers disagree between tools, before a redesign or new app, when adding a CDP, and when growth analyses keep hitting data gaps.

Don't use it for ad platform conversion tracking (the Performance Marketing `conversion-tracking-capi` skill) or for analysis itself (`funnel-analysis`, `cohort-retention-analysis`).

## Inputs to ask for, in one message
1. Product surfaces: web, iOS, Android, backend, marketing site.
2. Analytics and data tools in use.
3. Current event list and properties, with volumes.
4. Key metrics: north star, activation, retention, conversion definitions.
5. Engineering ownership and release process.
6. Consent requirements by market.

## Workflow

### Step 1. Start from metrics and questions
List the north star, inputs and key questions; each needs specific events and properties.

### Step 2. Audit current tracking
Export events and properties; find duplicates, inconsistent names, missing properties, dead events and client versus server mismatches.

### Step 3. Define the taxonomy
Naming convention, required properties per event, user and group properties, identity rules.

### Step 4. Write the tracking plan
One row per event: name, description, trigger, platform, properties with types and allowed values, owner, related metrics, status.

### Step 5. Decide client versus server
Business-critical events (sign-up, payment, subscription changes) from the server where possible; interaction events from the client.

### Step 6. Implement and QA
Test in a development environment with debug tools; check every property, identity merge and consent behaviour before release.

### Step 7. Govern
A change process (request, review, implement, QA), a named owner, quarterly clean-ups and alerts for volume anomalies.

## Tracking plan template
```
| Event | Description | Trigger | Platform | Properties (type, allowed values) | Owner | Metrics | Status |
| signed_up | Account created | Server, after account record saved | Server | method (email/google/sso), signup_channel, plan | Growth eng | Sign-ups, activation denominator | Live |
| project_created | First or later project created | Client after save | Web, iOS, Android | template_used (bool), project_type | Product eng | Activation | Live |
```

## Core events most products need
| Area | Events |
|---|---|
| Acquisition | page_viewed (marketing), signed_up |
| Activation | onboarding_step_completed, first core action (for example project_created) |
| Engagement | core actions with counts and types |
| Collaboration | user_invited, invite_accepted |
| Monetisation | trial_started, subscription_started, plan_changed, payment_failed, subscription_cancelled |
| Experiments | experiment_exposed (experiment, variant) |

## QA checklist before release
- Event fires once per action, on every platform listed.
- All required properties present with valid values.
- Anonymous and identified IDs merge correctly at sign-up and login.
- Consent state respected for analytics tools.
- Server events match client events for the same action where both exist.
- Volumes in the debug view match manual test counts.

## Naming convention rules
| Rule | Good | Avoid |
|---|---|---|
| object_action, past tense | invoice_sent | SendInvoice, sending_invoice |
| Lower snake case | project_created | ProjectCreated, project-created |
| Properties describe context | source: 'template' | Separate event per source |
| Consistent units | amount_minor (pence or cents) | Mixed currencies and units |
| No personal data in names | user_invited | invited_jane_doe |

## Change process
1. Request: who needs the event or property, for which metric or question.
2. Review: does an existing event cover it? Does it follow the taxonomy?
3. Implement: engineering adds it on the listed platforms.
4. QA: test in development with the checklist.
5. Publish: update the tracking plan status and notify analysts.
6. Monitor: volume alerts for sudden drops or spikes.

## Identity rules
| Moment | Rule |
|---|---|
| Before sign-up | Anonymous ID from the analytics tool |
| At sign-up or login | Call identify with the user ID; merge anonymous history |
| Logout | Reset identity so the next user isn't merged |
| Multiple devices | Same user ID across web and app |
| B2B | Group call with account ID for account-level analysis |
Wrong identity merges are one of the most common causes of inflated or deflated user counts.

## Deprecating events
Mark old events as deprecated in the plan, keep them flowing for a transition period while dashboards move to new events, then stop sending them and archive their definitions.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Legacy mess of events | Map old to new, run both for a transition, then deprecate |
| Several analytics tools | Use a CDP or warehouse as source, send consistent events to each tool |
| Ad blockers and consent | Server-side for critical events; respect consent; expect gaps in client data |
| B2B accounts | Group analytics for account-level metrics |
| Personal data | Don't send emails or names as event properties to analytics tools unless policy allows |

## Handoffs to related skills
- Metric definitions: `north-star-metric-tree`
- Funnels and cohorts built on events: `funnel-analysis`, `cohort-retention-analysis`
- Experiment exposure events: `experiment-design`
- Reporting: `growth-reporting`
- Ad conversion tracking: the Performance Marketing `conversion-tracking-capi` skill

## Worked example
A marketplace app had 340 events across web and mobile, including signup, sign_up, user_signed_up and SignUp, and activation defined differently in Amplitude and the warehouse. The audit cut to 62 events with object_action naming, required properties for source and platform, server-side sign-up and transaction events, and one activation definition used everywhere. A change process with QA before release stopped new duplicates. Funnel and cohort numbers finally matched across tools, and analysis time fell sharply.

## Output format
```
# Tracking plan: <product>, <date>
## Metrics and questions to support
## Audit findings (duplicates, gaps, mismatches)
## Taxonomy and naming convention
## Tracking plan table
## Client vs server decisions
## QA checklist and governance process
```

## Common mistakes
- Tracking everything with no purpose.
- Inconsistent naming across platforms.
- Critical events only on the client.
- Several definitions of the same metric.
- No owner or QA, so tracking decays.

## Questions to ask before you design
- Which metrics and decisions must the data support?
- Which events are business-critical?
- Who owns tracking changes and QA?

## Self-check before you answer
- Does every event support a metric or question?
- Is naming consistent with required properties?
- Are critical events server-side and identity rules clear?
- Is there a governance and QA process?

## Further reading
- Segment, tracking plan best practices: https://segment.com/docs/protocols/tracking-plan/best-practices/
- Amplitude, data taxonomy guide: https://amplitude.com/blog

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/tracking-plan/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
