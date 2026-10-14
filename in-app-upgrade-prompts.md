---
name: in-app-upgrade-prompts
description: "Design in-app upgrade experiences: upgrade moments at limits, premium features, team growth, trial and reverse trial endings and milestones, soft, hard, metered and preview paywalls, task-based copy, in-app checkout that returns users to their work, admin request flows, frequency rules and conversion measurement. Use whenever someone asks about upgrade prompts, paywalls, in-app upsells, converting free users at plan limits, trial ending messages, feature gating messages or self-serve upgrade flows inside a product."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/in-app-upgrade-prompts/
  category: marketing
  subcategory: product-led-growth
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# In-App Upgrade Prompts and Paywalls

In a self-serve business, the upgrade moment usually happens inside the product: a user hits a limit, tries a premium feature, invites one teammate too many or sees what a higher plan would add. These moments convert well when they arrive at the point of need, explain the value clearly and make upgrading easy. They convert badly when prompts fire on day one for everyone, block users mid-task without explanation or lead to a confusing checkout.

This skill designs in-app upgrade experiences: identifying upgrade moments, soft and hard paywalls, limit warnings, premium feature previews, trial and reverse trial endings, upgrade copy, in-app checkout and measurement.

## Operating principles
1. **Prompt at the moment of need.** Upgrade asks work best when the user is trying to do something paid plans allow.
2. **Explain value, not just price.** Show what the user gets and why it matters to their task.
3. **Don't trap users.** Let them finish their work or save progress where possible.
4. **Make upgrading easy.** In-app checkout, clear plan comparison, few steps.
5. **Respect dismissals.** Repeated nagging erodes trust and engagement.

## Upgrade moments
| Moment | Example | Prompt type |
|---|---|---|
| Approaching a limit | 80% of storage or projects used | Warning with option to upgrade |
| Reaching a limit | Fourth project on a three-project plan | Soft or hard paywall |
| Premium feature use | Clicking automation on free plan | Feature preview with upgrade |
| Team growth | Inviting a fourth member on a three-seat plan | Seat upgrade prompt |
| Trial ending | Three days left | Reminder with summary of value |
| Reverse trial ending | Premium features about to drop | List of premium features they used |
| Success milestone | 100th invoice sent | Gentle prompt for advanced features |

## Paywall types
| Type | Behaviour | Use when |
|---|---|---|
| Soft paywall | Explains benefit; user can continue or try once | Encouraging trials of premium value |
| Hard paywall | Action blocked until upgrade | Clear limit that protects paid value |
| Metered | Allows a few uses, then requires upgrade | Letting users experience value first |
| Preview | Shows the result or a demo of the feature | Value is visual or easy to show |

## When to use, and when not to
Use it when free-to-paid conversion is low, when users hit limits without upgrading, when trials end without conversion and when adding new paid features.

Don't use it to choose free limits themselves (`free-model-design`) or design the public pricing page (the CRO `pricing-page-optimisation` skill).

## Inputs to ask for, in one message
1. Plans, limits and premium features.
2. Current prompts, where they appear and their conversion.
3. Data on users reaching limits and trying premium features.
4. Checkout flow inside the product.
5. Trial or reverse trial details.
6. Support tickets about billing and limits.

## Workflow

### Step 1. Map upgrade moments
List every moment users meet a limit or premium feature, with volume.

### Step 2. Choose prompt types
Soft, hard, metered or preview, based on the value and risk of frustration.

### Step 3. Write the prompt
What the user tried to do, what the paid plan adds, the price or plan, and a clear action with an alternative.

### Step 4. Design the path
In-app checkout with saved context, so users return to their task after upgrading.

### Step 5. Handle team decisions
If the user can't pay, offer to request an upgrade from their admin with a pre-written message.

### Step 6. Design trial endings
Reminders, usage summaries and a clear choice between upgrading and the free plan.

### Step 7. Set frequency rules
Limit repeat prompts after dismissal.

### Step 8. Measure and test
Prompt views, upgrade clicks, checkout completion, revenue and effects on engagement.

## Prompt copy template
```
Headline: what they tried to do ("Add more projects")
Body: what the paid plan adds, tied to their task ("Team gives you unlimited projects, shared templates and guest access.")
Price or plan: "From £10 per user per month"
Primary action: "Upgrade to Team"
Secondary: "Ask your admin" or "Not now"
```

## Admin request flow
```
Prompt to member: "Your workspace is on the Free plan. Ask Sam (admin) to upgrade?"
Pre-written message: "Hi Sam, I'd like to add more projects for our team. The Team plan adds unlimited projects and shared templates. Could we upgrade? [link]"
Admin receives: email and in-app notice with one-click upgrade
```
Many prompts fail because the person who hits the limit isn't the person who pays; this flow connects them.

## Trial ending sequence
| Day | Message |
|---|---|
| 3 days before end | Summary of what they've done and premium features used |
| 1 day before | Reminder with clear choice: upgrade or move to free |
| End day | What changes now, with easy upgrade |
| 7 days after | Offer help or a short extension if usage was high |

## Frequency rules
- A given prompt at most once per session.
- After two dismissals, pause that prompt for 14 days.
- Never show upgrade prompts during first-run onboarding.
- Suppress prompts for users already in a sales conversation.

## Metrics
| Metric | Why |
|---|---|
| Prompt view to upgrade click rate | Prompt relevance |
| Checkout completion | Friction in the path |
| Upgrades per 100 users reaching a limit | Limit effectiveness |
| Admin requests sent and approved | Team buying path |
| Engagement after prompts | Whether prompts harm usage |
| Revenue per sign-up | Overall monetisation |

## Further reading
- Kyle Poyar on freemium and paywalls: https://www.growthunhinged.com/

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| User isn't the buyer | Request-upgrade flow to admin or billing owner |
| Hard paywall mid-task | Save work first; explain what happens next |
| Many free users never hit limits | Revisit the free model rather than adding more prompts |
| Enterprise needs | Route to sales instead of self-serve checkout |
| Students or non-profits | Clear discount paths where offered |

## Handoffs to related skills
- Free model: `free-model-design`
- PQLs and sales assist: `product-qualified-leads`, `product-led-sales`
- Seat growth: `team-expansion-invites`
- In-app messaging rules: `in-app-messaging`
- Pricing page: the CRO `pricing-page-optimisation` skill
- Checkout: the CRO `checkout-optimisation` skill

## Worked example
A note-taking app showed an upgrade banner to every user from day one and a generic plan page when users hit the storage limit. Conversion was low and the banner was the most-complained-about feature. The redesign removed the banner, added an 80% storage warning, a soft paywall at the limit explaining what the premium plan adds with a one-click in-app checkout that returned users to their note, a preview of offline access when users went offline and an admin request flow for team members. Free-to-paid conversion rose substantially and complaints about upgrade prompts fell.

## Output format
```
# Upgrade experience plan: <product>, <date>
## Upgrade moments with volume
## Prompt types and copy
## In-app checkout path
## Admin request flow
## Trial and reverse trial endings
## Frequency rules
## Metrics and tests
```

## Common mistakes
- Prompts for everyone on day one.
- Blocking users mid-task without saving work.
- Generic plan pages instead of contextual value.
- No path for users who can't pay.
- Endless repeated prompts.

## Questions to ask before you design
- Where do users meet paid value naturally?
- Who in the account can actually pay?
- What happens to users' work at a limit?

## Self-check before you answer
- Do prompts appear at moments of need?
- Does copy explain value tied to the task?
- Is upgrading easy and does it return users to their work?
- Are frequency and admin paths handled?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/in-app-upgrade-prompts/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
