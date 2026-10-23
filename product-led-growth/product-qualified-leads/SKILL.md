---
name: product-qualified-leads
description: "Define, score and route product-qualified leads and accounts: analysis of past conversions, usage, breadth, intent, limit, premium feature, fit and engagement signals, clear PQL definitions, simple scores, a routing matrix to sales, success or automated plays, CRM sync and conversion metrics that refine the model. Use whenever someone asks about product-qualified leads, PQLs, PQAs, which free users sales should contact, usage-based lead scoring, routing self-serve accounts to sales or combining product usage with ICP fit."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/product-qualified-leads/
  category: marketing
  subcategory: product-led-growth
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Product-Qualified Leads

In product-led businesses, the best sales leads are often already using the product. A product-qualified lead (PQL) is a user or account whose behaviour in the product shows they are getting value and are likely to buy or expand: several active teammates, heavy use of a key feature, hitting plan limits, visiting the pricing page, or a company that fits the ideal customer profile. Without PQLs, sales either ignores free users or calls everyone, wasting time and annoying people who just signed up.

This skill defines, scores and routes product-qualified leads and accounts: choosing signals, combining usage with fit, setting thresholds, building scores, routing to sales or automated plays, and measuring conversion so the model improves.

## Operating principles
1. **Usage plus fit.** Behaviour shows readiness; firmographics show whether a deal is worth sales time.
2. **Accounts, not just users.** In B2B, several active users in one company often matter more than one power user.
3. **Signals tied to value.** Use actions that predict paid conversion and expansion, validated with data.
4. **Right play for each lead.** Some PQLs need a salesperson; most need automated nudges.
5. **Close the loop.** Track which PQLs convert and refine the model regularly.

## Signal types
| Type | Examples |
|---|---|
| Activation and depth | Reached value moment, completed key setup, weekly active use |
| Breadth | Several active users, multiple teams, workspace growth |
| Intent | Pricing page visits, upgrade page views, plan comparison, contact requests |
| Limits | Approaching or hitting free or plan limits |
| Feature usage | Use of premium features in a trial or reverse trial |
| Fit | Company size, industry, region, tech stack, email domain |
| Engagement | Event attendance, help centre use, replies to onboarding emails |

## When to use, and when not to
Use it when adding sales to a self-serve product, when sales can't prioritise free users, when conversion of free accounts is low and when expansion opportunities are missed.

Don't use it for marketing-qualified lead scoring based on content downloads alone (the CRM and Lifecycle `lead-scoring-routing` skill) or for fully self-serve products with no sales team (focus on `in-app-upgrade-prompts`).

## Inputs to ask for, in one message
1. Product events tracked and product analytics access.
2. Historical data: which free or trial accounts converted and expanded.
3. Ideal customer profile and enrichment data.
4. CRM and how sales currently picks leads.
5. Sales capacity and deal size thresholds.
6. Automation tools for in-app and email plays.

## Workflow

### Step 1. Analyse past conversions
Compare accounts that converted or expanded with those that didn't: usage, breadth, limits, intent and fit.

### Step 2. Choose signals
Pick a small set that predicts conversion and can be measured reliably.

### Step 3. Define PQL criteria
For example: three or more active users in the last 14 days, reached activation, company with 50+ employees, and a pricing page visit or limit reached.

### Step 4. Build a score (optional)
Weight usage, breadth, intent and fit; keep it simple enough to explain to sales.

### Step 5. Set routing
High fit and high usage: sales outreach. Low fit and high usage: automated upgrade prompts. High fit, low usage: onboarding help. Low on both: nurture.

### Step 6. Write sales plays
What reps see (usage summary), what they say (value-led, based on usage) and what they offer (help, trials of higher plans, security reviews).

### Step 7. Sync data
Push PQL status and usage summaries into the CRM.

### Step 8. Measure and refine
PQL-to-opportunity and PQL-to-paid rates, deal sizes and cycle times; review the model quarterly.

## Routing matrix
| | High usage | Low usage |
|---|---|---|
| High fit | Sales assist outreach | Onboarding help from success or sales |
| Low fit | Automated upgrade prompts | Automated nurture |

## PQL definition template
```
Name: Team PQL
Account fit: 50+ employees OR target industry
Usage: 3+ active users in last 14 days AND activation reached
Intent or limits: pricing page visit OR 80% of plan limit
Routing: assign to product-led sales rep within 1 working day
Play: usage-based outreach offering a team plan review
Review date: quarterly
```

## Usage summary for reps
```
Account: Northwind Design (240 employees, agency)
Active users (14 days): 6 editors, 11 viewers
Key actions: shared library created, 38 files, 2 integrations
Intent: pricing page visited twice this week
Limits: 85% of free storage
Suggested play: offer a team plan review and security documentation
```
Reps who see this before reaching out can lead with the customer's own usage instead of a generic pitch.

## Simple scoring example
| Signal | Points |
|---|---|
| Activation reached | 20 |
| 3+ active users in 14 days | 25 |
| Premium feature used (trial) | 15 |
| Pricing page visit in 7 days | 15 |
| 80%+ of a plan limit | 15 |
| Company fits ICP | 10 |
Accounts above 70 points route to sales; 40 to 70 get automated plays. Check thresholds against real outcomes.

## Metrics
| Metric | Why |
|---|---|
| PQLs per week | Volume for sales capacity |
| PQL to opportunity rate | Signal quality |
| PQL to paid rate and time to close | Model value |
| Average deal size from PQLs | Fit quality |
| Conversion of non-PQL accounts | What the model misses |

## Rules of engagement
Agree when sales may contact a self-serve user, how quickly, how often and when to step back. Users who upgrade themselves during outreach shouldn't receive further sales calls, and opt-outs must be respected.

Review the model quarterly with sales and data teams together.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Personal email domains | Use usage and enrichment where possible; route mostly to automated plays |
| Very large company with one user | High fit, low breadth: help them spread inside the company |
| Too many PQLs for sales | Raise thresholds or add automated tiers |
| Too few PQLs | Lower thresholds or add earlier signals; check tracking |
| Privacy rules | Use product data within your terms and privacy policy; be transparent |

## Handoffs to related skills
- Sales assist motion: `product-led-sales`
- Upgrade prompts for self-serve: `in-app-upgrade-prompts`
- Expansion: `team-expansion-invites`
- Metrics: `plg-metrics`
- Lead scoring and routing in CRM: the CRM and Lifecycle `lead-scoring-routing` skill
- ICP definition: the Product Marketing `ideal-customer-profile` skill

## Worked example
A design tool's sales team called every new sign-up from a company email and converted few. Analysis of past deals showed accounts that converted to team plans typically had four or more active editors within two weeks, used shared libraries and belonged to companies with 100+ employees. The new PQL model required at least three active editors, shared library use and company fit, routed those accounts to two product-led sales reps with a usage summary, and sent smaller active teams automated upgrade prompts. Sales conversion rates improved markedly, and reps spent most of their time on accounts that became paying teams.

## Output format
```
# PQL model: <product>, <date>
## Analysis of past conversions
## Signals and definitions
## Score (if used)
## Routing matrix and plays
## CRM sync
## Metrics and review cadence
```

## Common mistakes
- Calling every sign-up.
- Usage signals without fit, or fit without usage.
- Models too complex for sales to trust.
- No feedback loop from outcomes.
- Ignoring account-level breadth.

## Questions to ask before you build
- Which behaviours did paying accounts show before they bought?
- Which accounts are worth a salesperson's time?
- How will sales see usage in their tools?

## Self-check before you answer
- Are signals validated against past conversions?
- Do definitions combine usage, breadth, intent and fit?
- Does each segment have a play?
- Are results tracked and the model reviewed?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/product-qualified-leads/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
