---
name: in-app-messaging
description: "Plan in-app messaging that guides rather than interrupts: announcements, contextual tips, action nudges, surveys, upgrade prompts, service notices and help, behavioural targeting and triggers, priority and frequency rules, short copy, coordination with email, one owner and calendar, retirement of stale messages and outcome metrics. Use whenever someone asks about in-app messages, product announcements, tooltips, in-app surveys or NPS, too many pop-ups in the product, coordinating in-app and email messages or governance for product messaging."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/in-app-messaging/
  category: marketing
  subcategory: product-led-growth
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# In-App Messaging

In-app messages reach users while they're using the product: announcements of new features, tips at the right moment, nudges towards key actions, surveys, upgrade prompts, maintenance notices and help. Used well, they guide users towards value without leaving the product. Used badly, they become a stream of pop-ups that interrupt work, get dismissed without reading and train users to ignore every message. As more teams gain access to in-app messaging tools, coordination becomes as important as copy.

This skill plans in-app messaging programmes: message types, targeting and triggers, frequency and priority rules, copy, coordination with email and other channels, governance across teams, surveys and feedback, and measurement.

## Operating principles
1. **Context beats broadcast.** Messages tied to what the user is doing outperform announcements to everyone.
2. **Fewer, better messages.** Each message should earn the interruption.
3. **One owner, one calendar.** Coordinate messages across product, marketing, success and sales.
4. **Match the format to the urgency.** Banners, tooltips, modals and inboxes suit different needs.
5. **Measure the outcome, not the view.** Did the user take the action that matters?

## Message types and formats
| Type | Format | Example |
|---|---|---|
| Feature announcement | Inbox item, small banner, modal for major launches | "Scheduled reports are here" |
| Contextual tip | Tooltip or hotspot | Suggest a shortcut when the user repeats an action |
| Action nudge | Checklist item, slideout | "Connect your calendar to see availability" |
| Survey | NPS or one-question survey | "How easy was setting up your first report?" |
| Upgrade prompt | Contextual paywall or banner | At limits or premium features |
| Service notice | Top banner | Maintenance or incident updates |
| Help | Help widget, chat, resource centre | Searchable help in context |

## When to use, and when not to
Use it when launching features, guiding users to key actions, collecting feedback, coordinating messages across teams and reducing reliance on email for product guidance.

Don't use it for email or SMS lifecycle programmes (the CRM and Lifecycle skills) or website pop-ups for visitors (the CRO `popups-onsite-messaging` skill).

## Inputs to ask for, in one message
1. In-app messaging tool and current messages.
2. Product events available for targeting.
3. User segments (role, plan, lifecycle stage, activity).
4. Upcoming launches and campaigns.
5. Which teams send messages today.
6. Engagement and outcome data for past messages.

## Workflow

### Step 1. Inventory messages
List all live messages with triggers, audiences, owners and results.

### Step 2. Define goals per message type
Adoption, activation, feedback, upgrades or service information.

### Step 3. Set targeting and triggers
By behaviour (did or didn't do something), plan, role, lifecycle stage and page.

### Step 4. Set priority and frequency rules
Maximum messages per session and per week; priority order when several qualify.

### Step 5. Write the message
Short headline, one benefit, one action, easy dismissal.

### Step 6. Coordinate channels
In-app for guidance during use; email for users who aren't active; avoid sending both for the same thing at once.

### Step 7. Govern
One owner, a shared calendar, review for new message types, retirement of stale messages.

### Step 8. Measure
View, click, dismissal and, most importantly, the target action and downstream retention.

## Priority and frequency rules (example)
- Service notices override everything.
- Then onboarding guidance for new users.
- Then contextual tips and adoption nudges.
- Then announcements and surveys.
- At most one modal per session and two non-blocking messages per day per user.
- No marketing announcements during first-run onboarding.

## Message copy template
```
Headline (5-8 words): what's new or what to do
Body (1-2 sentences): the benefit for this user
Action: one button with a clear verb
Dismiss: visible close or "Not now"
```

## Targeting examples
| Audience | Trigger | Message |
|---|---|---|
| Activated users who haven't connected an integration | Third visit to reports | "Connect your CRM to keep reports up to date automatically." |
| Admins on Team plan | Login after a security feature launch | "New: require SSO for your workspace." |
| Users who completed a key task | Task completion | One-question survey about ease |
| Inactive for 14 days | Next login | "Here's what changed since your last visit." |
| Free users at 80% of a limit | Limit threshold | Limit warning with upgrade option |

## Format guide
| Format | Interruption | Use for |
|---|---|---|
| Tooltip or hotspot | Low | Explaining a feature in context |
| Inbox or resource centre | Very low | Announcements and updates users can browse |
| Slideout | Medium | Nudges and short surveys |
| Banner | Medium | Service notices, account-wide information |
| Modal | High | Major launches for relevant users, critical changes |

## Metrics
| Metric | Why |
|---|---|
| Target action completion | Whether the message worked |
| Click-through and dismissal rate | Relevance and annoyance |
| Messages seen per user per week | Fatigue risk |
| Feature adoption or upgrade lift versus holdout | Real impact |
| Survey response rate and scores | Feedback quality |

## Governance checklist
- Named owner for in-app messaging.
- Shared calendar visible to all teams.
- Templates and copy guidelines.
- Review for new message types and major launches.
- Monthly clean-up of expired or low-performing messages.
- Holdout groups for important nudges.

## Surveys inside the product
Ask one question at a meaningful moment, such as after a first report or a support interaction, rather than random NPS pop-ups. Sample a share of users, limit surveys to one per user per quarter, and close the loop by sharing what changed. Route detractors to success or support quickly.

## Channel coordination
In-app messages reach active users; email reaches people who haven't logged in. Use shared events so a user who completes an action stops receiving both, and never send the same announcement through every channel at once.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Many teams want to message users | Central calendar and approval for new campaigns |
| Major launch | Modal for the relevant segment only, plus inbox and email for others |
| Survey fatigue | Sample users; limit surveys per user per quarter |
| Mobile apps | Shorter messages; respect notification permissions |
| Enterprise customers | Let admins control certain announcements |

## Handoffs to related skills
- Onboarding guidance: `in-product-onboarding`
- Feature adoption: `feature-adoption`
- Upgrade prompts: `in-app-upgrade-prompts`
- Education resources: `product-education`
- Lifecycle emails: the CRM and Lifecycle skills
- Website pop-ups: the CRO `popups-onsite-messaging` skill

## Worked example
A SaaS company let product, marketing and success all send in-app messages, and some users saw four modals in one session. Engagement with messages fell and support complaints rose. The company created a single owner and calendar, set priority and frequency rules, replaced most announcements with an inbox and contextual tips, kept modals for major launches to relevant segments and retired 60% of stale messages. Click-through on remaining messages rose, feature adoption from tips improved and complaints dropped.

## Output format
```
# In-app messaging plan: <product>, <date>
## Inventory and retirement list
## Message types and goals
## Targeting and triggers
## Priority and frequency rules
## Copy guidelines
## Channel coordination and governance
## Metrics
```

## Common mistakes
- Broadcasting every announcement as a modal.
- No frequency limits.
- Several teams messaging without coordination.
- Measuring views instead of actions.
- Stale messages left running for years.

## Questions to ask before you plan
- What should users do differently after each message?
- Who owns in-app messages across teams?
- How many messages does a typical user see per week?

## Self-check before you answer
- Are messages targeted by behaviour and context?
- Are priority and frequency rules set?
- Is there one owner and calendar?
- Are outcomes, not views, measured?

## Further reading
- Intercom on in-app messaging: https://www.intercom.com/blog/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/in-app-messaging/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
