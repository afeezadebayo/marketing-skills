---
name: free-model-design
description: "Design free offers that drive revenue: freemium, time-limited trials, reverse trials, usage-based free tiers, open-source cores and free tools, usage, seat, feature, time, history, branding and support gates placed where value grows, limit analysis with data, trial length by time to value, the limit experience and fair migrations. Use whenever someone asks about freemium versus free trial, reverse trials, free plan limits, feature gating, trial length, card upfront for trials, free users not upgrading or redesigning a free plan."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/free-model-design/
  category: marketing
  subcategory: product-led-growth
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Free Model Design: Freemium, Free Trials and Reverse Trials

The free offer is the front door of a product-led business. Too generous, and most users never need to pay; too stingy, and they never experience enough value to want to. The wrong type of free offer for the product (a 14-day trial for something that takes a month to set up, or freemium for a product whose value is all in advanced features) quietly caps growth. Designing the free model means choosing the type, the limits and gates, the upgrade triggers and the experience when users hit them.

This skill designs and reviews free models: freemium, free trials, reverse trials, usage-based free tiers and open-source cores, with limits, feature gates, trial length, card requirements and the upgrade experience, judged on activation, paid conversion and revenue.

## Operating principles
1. **Free must deliver real value.** Users should succeed at something meaningful on the free offer.
2. **Paid must solve a bigger problem.** Gates should sit where value grows: teams, scale, control, advanced outcomes.
3. **Limits should be hit by the right users.** Growing, engaged users should reach them; casual users shouldn't be pushed away.
4. **Upgrade moments should feel natural.** Prompts appear when users need more, not randomly.
5. **Judge on revenue, not sign-ups.** More free users is only good if paid conversion and retention follow.

## Free model types
| Type | How it works | Fits when | Risks |
|---|---|---|---|
| Freemium | Free plan forever with limits | Large market, low cost to serve, network or viral effects | Too generous; support costs |
| Free trial (time-limited) | Full or most features for 7 to 30 days | Value appears quickly; clear paid need | Trial ends before value; pressure |
| Reverse trial | Start with premium features for a period, then drop to free | You want users to experience premium value and keep a free base | Confusion if not explained |
| Usage-based free tier | Free up to a usage amount | Value scales with usage (API calls, messages) | Bill shock later; abuse |
| Open-source or community core | Core free; paid hosting, features or support | Developer tools, infrastructure | Hard to monetise if paid value unclear |
| Free tool or assessment | A standalone free tool that leads to the product | Complex products with clear early insights | Tool doesn't lead to product use |

## Limits and gates
| Gate type | Example | Works when |
|---|---|---|
| Usage limit | 3 projects, 1,000 contacts, 10 GB | Usage grows with value |
| Seat limit | Up to 3 users | Value grows with team size |
| Feature gate | Automation, integrations, SSO on paid | Advanced features matter to growing teams |
| Time limit | 14-day trial | Value is quick and obvious |
| History limit | 90 days of history on free | Long-term data has value |
| Branding | "Made with" badge on free | Visibility drives acquisition |
| Support level | Community support on free | Businesses value faster support |

## When to use, and when not to
Use it when launching a free offer, when free-to-paid conversion is low, when free usage costs are high, when switching between trial and freemium and when packaging changes.

Don't use it to set list prices and tiers in depth (the Product Marketing `pricing-packaging` skill) or optimise the sign-up form (the CRO `signup-flow-optimisation` skill).

## Inputs to ask for, in one message
1. Product, value moment and how value grows with use.
2. Current free offer, limits and plan distribution.
3. Free-to-paid conversion, time to convert and churn by plan.
4. Usage data: how many free users hit each limit, and their behaviour.
5. Cost to serve free users.
6. Competitor free offers.

## Workflow

### Step 1. Map how value grows
By usage, team size, advanced needs, history or outcomes.

### Step 2. Choose the type
Match to time to value, market size, cost to serve and how value grows.

### Step 3. Set gates
Place limits where growing, engaged users naturally need more.

### Step 4. Check with data
What share of free users reach each limit, and do they look like paying customers?

### Step 5. Design the limit experience
Clear messages before and at the limit, what upgrading adds, easy self-serve checkout and a way to talk to sales for larger needs.

### Step 6. Decide trial details
Length based on time to value, card upfront or not, what happens at the end (downgrade to free or lock).

### Step 7. Test and measure
Activation, free-to-paid conversion, revenue per sign-up, support cost and retention; test changes on new cohorts.

## Trial length guide
| Time to value | Suggested trial |
|---|---|
| Minutes to a day | 7 days |
| A few days | 14 days |
| One to three weeks | 21 to 30 days, or a reverse trial |
| Longer | Freemium, guided pilot or free assessment instead |

## Limit analysis template
```
| Limit | Free users reaching it (90 days) | Share who upgrade after reaching it | Their profile | Change? |
| 3 projects | 18% | 22% | Small agencies | Keep |
| 2 seats | 6% | 35% | Growing teams | Consider 3 seats to drive invites |
| 90-day history | 3% | 5% | Long-term users | Not a strong trigger |
```

## Reverse trial messaging
Tell users at sign-up that they have premium features for a set period, remind them before it ends, show what they used that is premium and explain what stays free. Clear messages turn the drop to free into a natural upgrade moment instead of a surprise.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Free plan too generous | Tighten gates for new users; grandfather existing users fairly |
| High abuse or fraud | Verification, rate limits and risk scoring |
| Card-upfront debate | Test on paid revenue per sign-up, not sign-up volume |
| Enterprise buyers | Free plan for individuals; trials or pilots for enterprise features |
| Infrastructure costs for free users | Usage caps, inactivity clean-up, lighter free infrastructure |

## Handoffs to related skills
- Strategy: `plg-strategy`
- Upgrade prompts: `in-app-upgrade-prompts`
- Seat growth and invites: `team-expansion-invites`
- Metrics: `plg-metrics`
- Pricing and packaging: the Product Marketing `pricing-packaging` skill
- Pricing page: the CRO `pricing-page-optimisation` skill

## Worked example
A form builder offered unlimited forms and responses on its free plan; 98% of users never paid. Analysis showed teams that grew paid for integrations and branding removal, while response volume tracked business value. The new model limited free plans to 100 responses a month and three forms, kept the "made with" badge on free, moved integrations to paid and launched a 14-day reverse trial of premium features for new sign-ups. Existing free users kept old limits for six months. Free-to-paid conversion rose several times over, and the badge continued to bring in new sign-ups.

## Output format
```
# Free model design: <product>, <date>
## How value grows
## Recommended type and rationale
## Limits and gates (with data)
## Limit and upgrade experience
## Trial details
## Migration plan for existing users
## Metrics and tests
```

## Common mistakes
- Free plans that cover most users' needs.
- Trials shorter than time to value.
- Gates on features users never reach.
- Judging changes on sign-ups.
- Surprising existing free users with sudden limits.

## Questions to ask before you design
- How does value grow as customers succeed?
- Which limits do your best paying customers hit first?
- How long does a new user take to reach value?

## Self-check before you answer
- Does free deliver real value?
- Are gates placed where value grows?
- Is the limit experience clear and helpful?
- Are changes judged on revenue and retention?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/product-led-growth/free-model-design/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
