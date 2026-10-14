---
name: product-led-sales
description: "Design product-led sales motions where humans help accounts the product has already won: engagement thresholds, roles, usage summaries in the CRM, usage-led outreach, team, security, rollout, annual and enterprise plays, enterprise assets, rules of engagement, compensation that does not fight self-serve and metrics for sales-assisted versus self-serve accounts. Use whenever someone asks about product-led sales, sales assist for PLG, adding a sales team to a self-serve product, converting free users at large companies, usage-based outreach or enterprise deals from self-serve accounts."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/product-led-sales/
  category: marketing
  subcategory: product-led-growth
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Product-Led Sales

Product-led sales combines self-serve adoption with human help for the accounts where it makes a difference. Users discover and adopt the product on their own; when usage signals show a team or company is ready for more (more seats, security reviews, annual contracts, enterprise features), a salesperson steps in to help them buy. Done well, sales accelerates deals that the product started. Done badly, reps cold-call free users with generic pitches, interrupt people who were about to upgrade themselves and damage the trust the product built.

This skill designs product-led sales motions: when sales engages, team roles, outreach based on usage, plays for different situations, enterprise needs, handoffs between self-serve and sales, compensation considerations and metrics.

## Operating principles
1. **Help, don't interrupt.** Sales adds value by solving buying problems users can't solve alone.
2. **Lead with usage.** Reps open with what the customer is already doing in the product.
3. **Engage at the right threshold.** Seat counts, spend or company fit decide when humans join.
4. **Let self-serve stay self-serve.** Users who can upgrade themselves shouldn't be forced into sales.
5. **Align incentives.** Compensation should reward helping accounts grow, without fighting self-serve conversions.

## When sales adds value
| Situation | Why sales helps |
|---|---|
| Team or company rollout | Planning, admin setup, training |
| Security and compliance reviews | Questionnaires, SSO, data processing agreements |
| Procurement and annual contracts | Invoicing, purchase orders, negotiation |
| Enterprise features | SSO, audit logs, advanced permissions, support plans |
| Expansion across departments | Introductions and internal champions |
| Complex use cases | Solution design and integrations |

## Roles
| Role | Focus |
|---|---|
| Product-led sales rep (or "product specialist") | Converts PQL accounts to paid team or business plans |
| Account executive | Larger, multi-stakeholder deals |
| Customer success manager | Onboarding, adoption and expansion for paying accounts |
| Sales development (optional) | Research and first outreach on high-fit PQLs |
| Growth or ops | PQL models, routing and tooling |

## When to use, and when not to
Use it when self-serve accounts outgrow self-serve plans, when large companies use the free product without buying, when adding sales to a PLG company and when sales and product teams conflict.

Don't use it for fully sales-led motions (the Product Marketing `sales-enablement` skill) or for defining PQL scores (`product-qualified-leads`).

## Inputs to ask for, in one message
1. Plans, prices and where self-serve stops (seat limits, enterprise features).
2. PQL definitions and data available to reps.
3. Current sales team, roles and compensation.
4. Conversion and expansion data by account size.
5. Common blockers in larger deals (security, procurement).
6. CRM and product data integrations.

## Workflow

### Step 1. Set engagement thresholds
For example: accounts with 10+ active users, companies above a size, enterprise feature interest or spend above a level.

### Step 2. Define roles and coverage
Who handles PQLs, who handles enterprise deals, who handles expansion.

### Step 3. Give reps product context
Usage summaries in the CRM: active users, teams, features, limits, intent signals.

### Step 4. Write usage-led outreach
Reference real usage, offer specific help and make it easy to say no.

### Step 5. Build plays
Team expansion, security review, enterprise trial, annual plan, department rollout.

### Step 6. Prepare enterprise assets
Security documentation, SSO setup guides, procurement information, ROI summaries.

### Step 7. Set rules of engagement
When reps may contact users, how often, and how self-serve upgrades are credited.

### Step 8. Align compensation
Credit reps for accounts they influence without discouraging self-serve; common approaches include pooled or overlay credit for PLG-influenced revenue.

### Step 9. Measure
Conversion of PQL accounts, deal size, cycle time, expansion and net revenue retention for sales-assisted versus self-serve accounts.

## Usage-led outreach example
```
Subject: Your team's 14 projects in Acme
Hi Priya,
I noticed your team at Northwind now has 9 people working across 14 projects, and you're close to the free plan's project limit.
Teams your size usually want shared templates, admin controls and SSO. Happy to set up a 2-week trial of the Business plan and walk your admin through it, or answer any security questions.
If you'd rather upgrade yourself, here's the link: [link]
[Name], Product specialist
```

## Plays
| Play | Trigger | Offer |
|---|---|---|
| Team upgrade | 5+ active users near limits | Team plan review, trial of higher plan |
| Security review | Visits security page or asks about SSO | Security pack, call with specialist |
| Department rollout | Several teams in one company using separately | Consolidation and admin controls |
| Annual plan | Monthly paying account with stable growth | Annual pricing with discount |
| Enterprise trial | Large company with enterprise feature interest | Guided enterprise trial |

## Enterprise readiness pack
- Security overview and certifications, with reports available on request.
- SSO and SCIM setup guides.
- Data processing agreement and privacy documentation.
- Admin controls and audit log overview.
- Procurement details: invoicing, purchase orders, payment terms.
- Support and service level options.
Having these ready shortens the security and procurement stages that usually slow larger deals.

## Metrics
| Metric | Why |
|---|---|
| PQL to paid conversion (sales-assisted) | Sales value on ready accounts |
| Average deal size, sales-assisted vs self-serve | Where humans add revenue |
| Sales cycle length | Efficiency |
| Expansion and net revenue retention by motion | Long-term value |
| Self-serve conversion rate | Check sales isn't cannibalising self-serve |

## Weekly review
Product-led sales reps, growth and success meet weekly to review new PQL accounts, open deals, blockers and feedback on the PQL model, so signals and plays improve together.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| User upgrades during outreach | Thank them, offer help, stop selling |
| Champion leaves the company | Identify new active users; offer to help |
| Free users in huge companies | Map usage across teams; find an internal champion |
| Reps prefer outbound to PQLs | Show PQL conversion rates and adjust targets |
| Discount pressure | Trade discounts for annual commitment or volume |

## Handoffs to related skills
- PQLs: `product-qualified-leads`
- Self-serve upgrades: `in-app-upgrade-prompts`
- Expansion: `team-expansion-invites`
- Metrics: `plg-metrics`
- Sales enablement: the Product Marketing `sales-enablement` skill
- Pricing and packaging: the Product Marketing `pricing-packaging` skill

## Worked example
A project management company had a strong self-serve business, but large companies used free and team plans across many departments without central contracts. It created a product-led sales team that engaged accounts with 25+ active users or enterprise feature interest, gave reps usage summaries in the CRM, built department rollout and security review plays and prepared an enterprise security pack. Reps opened with usage and offered help with consolidation and SSO. Within a year, enterprise contracts from existing users became a major share of new revenue, and self-serve conversion was unaffected.

## Output format
```
# Product-led sales plan: <product>, <date>
## Engagement thresholds
## Roles and coverage
## Usage context in CRM
## Outreach templates and plays
## Enterprise assets
## Rules of engagement and compensation
## Metrics
```

## Common mistakes
- Cold-calling every free user.
- Generic pitches that ignore usage.
- Forcing self-serve users into sales processes.
- Compensation that fights self-serve.
- No enterprise assets for security and procurement.

## Questions to ask before you design
- At what point do accounts need human help to buy or expand?
- What do reps know about an account before they reach out?
- How are self-serve and sales-assisted revenue credited?

## Self-check before you answer
- Are engagement thresholds clear?
- Does outreach lead with real usage?
- Do plays solve buying problems users can't solve alone?
- Are incentives aligned with self-serve?

## Further reading
- Kyle Poyar, Growth Unhinged, on product-led sales: https://www.growthunhinged.com/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/product-led-sales/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
