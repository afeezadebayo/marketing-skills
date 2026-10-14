---
name: feature-adoption
description: "Drive adoption of features that change retention and expansion: impact analysis against matched non-users, adoption funnels from exposed to expanded, barrier diagnosis, fixes to setup and permissions, contextual triggers based on user behaviour, education, careful nudges and measurement with holdouts. Use whenever someone asks about feature adoption, low feature usage, feature discovery, driving usage of integrations or automations, in-app prompts for features, customers requesting features that already exist or improving retention through product usage."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/feature-adoption/
  category: marketing
  subcategory: product-led-growth
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Feature Adoption

Activation gets a user to first value; feature adoption keeps them growing. Most products have features that strongly predict retention and expansion (integrations, automations, sharing, reporting) that many customers never discover. Teams ship features, announce them once and move on, while usage stays low. In product-led businesses, adoption of the right features is often the difference between a user who churns after three months and an account that expands for years.

This skill drives adoption of features that matter: identifying retention-linked features, measuring adoption funnels, finding barriers, designing contextual discovery, in-app guidance, education and nudges, and measuring the effect on retention and expansion.

## Operating principles
1. **Focus on features that change outcomes.** Not every feature needs adoption; the ones linked to retention and expansion do.
2. **Discovery in context.** Introduce features when users face the problem they solve.
3. **Measure the adoption funnel.** Aware, tried, used again, used habitually.
4. **Remove barriers before adding prompts.** Confusing setup or permissions often block adoption more than awareness.
5. **Prove the effect.** Check whether adoption actually improves retention or revenue.

## Adoption funnel
| Stage | Definition | Typical barrier |
|---|---|---|
| Exposed | Saw the feature or a message about it | Hidden in menus |
| Tried | Used it once | Unclear value or setup effort |
| Repeated | Used it again within a set period | First experience disappointing |
| Habitual | Uses it regularly | Not part of the workflow |
| Expanded | Uses it across the team or account | Permissions, admin settings |

## When to use, and when not to
Use it after activation is in reasonable shape, when retention plateaus, when expansion is weak, after launching important features and when customers request features that already exist.

Don't use it for first-run onboarding (`in-product-onboarding`) or launch communications outside the product (the Product Marketing `product-launch` skill).

## Inputs to ask for, in one message
1. Feature list with usage data.
2. Retention and expansion by feature usage.
3. Product analytics access and event tracking for key features.
4. Support tickets and feature requests mentioning existing features.
5. In-app messaging tools.
6. Customer interviews or survey results.

## Workflow

### Step 1. Find retention-linked features
Compare retention and expansion for accounts that use each feature versus similar accounts that don't; check whether adoption comes before improved retention.

### Step 2. Measure adoption funnels
Exposed, tried, repeated, habitual and expanded for each priority feature.

### Step 3. Diagnose barriers
Recordings, interviews and support tickets: awareness, understanding, setup effort, permissions or poor fit.

### Step 4. Fix barriers first
Simplify setup, improve defaults, change permissions, improve the first-use experience.

### Step 5. Design contextual discovery
Trigger guidance when the user does something the feature helps with (for example exporting a report manually suggests scheduled reports).

### Step 6. Educate
Short videos, help articles, templates and webinars tied to the feature.

### Step 7. Nudge carefully
In-app messages, emails and success manager conversations for accounts that would benefit.

### Step 8. Measure effect
Adoption changes and their impact on retention and expansion, ideally with holdouts.

## Contextual trigger examples
| User behaviour | Feature to suggest | Message |
|---|---|---|
| Exports the same report weekly | Scheduled reports | "Want this report emailed every Monday?" |
| Copies data between tools | Integration | "Connect your CRM to sync this automatically." |
| Assigns many tasks manually | Automation rules | "Automate assignments for new tasks like these." |
| Shares screenshots of dashboards | Shared dashboards | "Share a live link instead of screenshots." |

## Feature impact analysis template
```
| Feature | Adoption rate | 6-month retention (users) | 6-month retention (non-users, matched) | Expansion difference | Priority |
| Integrations | 22% | 88% | 61% | +2 seats average | High |
| Custom fields | 40% | 70% | 66% | Small | Low |
```
Correlation isn't proof; confirm with experiments where possible.

## Barrier diagnosis
| Barrier | Signs | Fix |
|---|---|---|
| Awareness | Few users ever open the feature | Contextual discovery, better placement |
| Understanding | Users open it and leave quickly | Clearer copy, examples, short video |
| Setup effort | Many start setup, few finish | Simpler setup, defaults, one-click connections |
| Permissions | Members can't enable it | Admin prompts with team benefits |
| Poor first experience | Tried once, never again | Better defaults and templates |
| Poor fit | Segment doesn't need it | Stop pushing it to that segment |

## Nudge rules
- Target accounts that would benefit, based on behaviour.
- One feature nudge at a time per user.
- Stop nudging after adoption or two dismissals.
- Pair in-app prompts with a short help resource.
- Give success managers a list of high-value accounts not using key features.

## Metrics
| Metric | Why |
|---|---|
| Adoption funnel conversion | Where users stop |
| Repeat usage within 30 days | Real adoption, not curiosity |
| Accounts with key features adopted | Account health |
| Retention and expansion versus holdout | Business impact |
| Support tickets about the feature | Confusion and friction |

## Quarterly adoption review
Each quarter, choose two or three priority features, review their funnels, ship barrier fixes and discovery changes, and report the effect on retention and expansion. Retire features nobody uses and that don't help retention, so the product stays simpler for new users.

## Naming and placement
Features users can't find by name often look missing. Use the words customers use in support tickets and requests, place features where the related task happens and link to them from help articles and search inside the product.

Review naming whenever support tickets show users can't find a feature.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Feature used by power users only | Check whether it suits the broader audience before pushing it |
| Admin permissions block adoption | Prompt admins with the benefit for their team |
| Many features competing for attention | Prioritise two or three per quarter |
| Users request an existing feature | Fix discoverability and naming |
| Low adoption after launch | Interview non-adopters before adding more prompts |

## Handoffs to related skills
- First-run onboarding: `in-product-onboarding`
- In-app messages: `in-app-messaging`
- Education: `product-education`
- Expansion: `team-expansion-invites`
- Metrics: `plg-metrics`
- Retention analysis: the Growth Marketing `cohort-retention-analysis` skill

## Worked example
A CRM for small businesses found accounts using its email integration retained far better, but only 15% connected it. Recordings showed the setup page asked for technical server details most users didn't know. The team replaced manual setup with one-click sign-in for major email providers, added a contextual prompt when users logged emails manually, and recorded a two-minute video. Integration adoption roughly tripled over a quarter, and a holdout test showed better retention among accounts exposed to the new flow.

## Output format
```
# Feature adoption plan: <product>, <date>
## Retention-linked features (analysis)
## Adoption funnels for priority features
## Barriers and fixes
## Contextual discovery and education plan
## Nudges by channel
## Measurement and holdouts
```

## Common mistakes
- Pushing every feature equally.
- Announcing features once and moving on.
- Adding prompts before fixing setup problems.
- Measuring clicks on announcements instead of repeated use.
- Assuming correlation proves impact.

## Questions to ask before you plan
- Which features predict retention and expansion for your customers?
- Where in the adoption funnel do users stop?
- What makes a feature hard to start using?

## Self-check before you answer
- Are priority features chosen by impact on outcomes?
- Are barriers diagnosed and fixed first?
- Is discovery contextual?
- Is the effect on retention measured?

## Further reading
- Pendo product adoption resources: https://www.pendo.io/resources/
- Amplitude product analytics guides: https://amplitude.com/blog

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/feature-adoption/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
