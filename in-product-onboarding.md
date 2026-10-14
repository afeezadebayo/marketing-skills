---
name: in-product-onboarding
description: "Design in-product onboarding from first login to value: the minimum steps to the value moment, role-based routing, first screens, empty states with one action, templates and sample data, short checklists, contextual tooltips and walkthroughs, celebrations with next steps, sessions two and three, and activation and retention by segment. Use whenever someone asks about user onboarding, in-app onboarding, product tours, empty states, onboarding checklists, time to value, first-run experience or why new users don't activate."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/in-product-onboarding/
  category: marketing
  subcategory: product-led-growth
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# In-Product Onboarding

The minutes after sign-up decide whether a new user becomes a customer. In-product onboarding is everything inside the product that helps a user reach value quickly: the first screen, empty states, templates and sample data, checklists, tooltips, guided tours, contextual help and the next step after the first success. Many products greet new users with a blank workspace or a ten-step tour that people click through without learning anything, then lose most of them before they experience what makes the product useful.

This skill designs in-product onboarding from first login to the value moment and beyond: user segmentation, first-run experience, empty states, templates, checklists, contextual guidance, progressive disclosure, the second and third sessions and measurement. Sign-up forms sit in the CRO `signup-flow-optimisation` skill; onboarding emails sit in the CRM and Lifecycle `onboarding-activation` skill.

## Operating principles
1. **Shortest path to value.** Remove every step that doesn't move the user towards the value moment.
2. **Show, don't tell.** Templates, sample data and interactive steps beat explanations.
3. **Personalise by job.** Different roles and use cases need different first steps.
4. **Guide in context.** Help appears where and when users need it, not as a tour on login.
5. **Plan beyond the first session.** Habit and team adoption happen in later sessions.

## Onboarding patterns
| Pattern | Use | Watch out for |
|---|---|---|
| Welcome survey (1 to 3 questions) | Personalise first steps by role or goal | Questions that change nothing |
| Templates and sample data | Show what good looks like instantly | Templates nobody can adapt |
| Empty states with a single action | Turn blank screens into next steps | Several competing actions |
| Onboarding checklist | Three to five steps to value | Long lists that feel like homework |
| Contextual tooltips | Explain a feature when it's first relevant | Tooltip overload |
| Interactive walkthrough | Users do the task with guidance | Long linear tours |
| Progress indicators | Motivate completion | Fake progress |
| Celebrations | Mark the value moment and point to next step | Overdone confetti |
| Help and chat | Answer questions in context | Hidden help |

## When to use, and when not to
Use it when activation is low, time to value is long, new users churn in the first week, after redesigns and when launching to new segments.

Don't use it for the sign-up form (the CRO skill) or onboarding email sequences (the CRM skill), though all three should work together.

## Inputs to ask for, in one message
1. Value moment and activation definition.
2. Screens and flows a new user sees, with recordings if possible.
3. Funnel from first login to activation and week-4 retention.
4. User segments (roles, use cases, company size).
5. Onboarding tools available (in-app guide tools or custom).
6. Support questions from new users.

## Workflow

### Step 1. Define the value moment and steps to it
List the minimum actions a user must take; remove or automate the rest.

### Step 2. Segment
Pick two or three segments with different first steps; ask one or two questions at sign-up to route them.

### Step 3. Design the first screen
One clear action, a template or sample data and a visible path to value.

### Step 4. Replace empty states
Each blank screen gets a short explanation and one action.

### Step 5. Add a short checklist
Three to five steps towards activation, with progress and the option to dismiss.

### Step 6. Add contextual guidance
Tooltips and hints when features first become relevant.

### Step 7. Celebrate and point forward
At the value moment, acknowledge it and suggest the next step (often inviting a teammate or a second key action).

### Step 8. Plan sessions two and three
What should bring users back and what they should do next.

### Step 9. Measure and test
Step completion, time to value, activation, week-1 and week-4 retention, by segment.

## Onboarding map template
```
| Step | Screen | User goal | What we show | Action | Drop-off today | Change |
| 1 | Welcome | Get started | Role question | Choose role | 5% | Keep |
| 2 | Workspace | See value | Empty workspace | Create project | 40% | Template gallery by role |
| 3 | Project | Do first task | Blank board | Add task | 25% | Sample tasks with tooltip |
```

## Empty state formula
```
What this space is for (one line)
Why it matters to the user (one line)
One primary action (button)
Optional: template or sample data link
```
Example: "Projects keep client work in one place. Start with a template built for agencies." [Use agency template]

## Checklist rules
- Three to five items, each a real step towards value.
- First item easy to complete for quick progress.
- Each item opens the place where the action happens.
- Dismissible, and hidden once complete.
- Shown again only if the user hasn't activated after a few days.

## Metrics by stage
| Metric | Why |
|---|---|
| Step completion rates | Where users drop off |
| Time to value | Speed of onboarding |
| Activation rate by segment | Overall success |
| Day-7 and week-4 retention | Whether onboarding led to habit |
| Support tickets from new users | Confusion points |

## Coordinating with email and humans
In-product guidance, onboarding emails and any human onboarding should follow the same steps. Emails remind users of the next step they haven't taken; in-product prompts help them do it; success managers handle larger accounts that need setup help. Shared event tracking keeps messages from contradicting each other.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Complex product | Guided setup, sample data and optional human onboarding for larger accounts |
| Several user roles in one account | Role-based first steps; admin versus member flows |
| Mobile app | Shorter steps, permissions after value, offline-friendly guidance |
| Data import needed | Offer sample data first, import later |
| Users skip everything | Make guidance contextual rather than upfront |

## Handoffs to related skills
- Sign-up flow: the CRO `signup-flow-optimisation` skill
- Onboarding emails: the CRM and Lifecycle `onboarding-activation` skill
- Feature adoption after activation: `feature-adoption`
- Invites: `team-expansion-invites`
- In-app messages: `in-app-messaging`
- Metrics: `plg-metrics`

## Worked example
A project management tool showed new users an empty workspace and a ten-step tour; fewer than a third created a project. The redesign asked one question about the type of work, opened a matching template with sample tasks, replaced the tour with a four-step checklist (customise a task, assign it, set a due date, invite a teammate), added tooltips the first time each feature appeared and celebrated the first completed task with a prompt to invite a colleague. Activation and week-4 retention rose substantially.

## Output format
```
# In-product onboarding plan: <product>, <date>
## Value moment and minimum steps
## Segments and routing
## First screen and empty states
## Checklist and contextual guidance
## Celebrations and next steps
## Sessions two and three
## Metrics and tests
```

## Common mistakes
- Blank first screens.
- Long product tours on login.
- Same onboarding for every role.
- No plan after the first session.
- Measuring tour completion instead of activation.

## Questions to ask before you design
- What is the fewest number of steps to the value moment?
- How do needs differ by role or use case?
- Where do new users drop off today?

## Self-check before you answer
- Is the path to value as short as possible?
- Are first steps personalised?
- Is guidance contextual?
- Are activation and retention measured by segment?

## Further reading
- Appcues onboarding resources: https://www.appcues.com/blog
- Nielsen Norman Group on onboarding patterns: https://www.nngroup.com/articles/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/in-product-onboarding/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
