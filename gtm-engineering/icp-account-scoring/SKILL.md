---
name: icp-account-scoring
description: "Score accounts and contacts for GTM workflows: hard exclusions, a fit score from won and lost deal data, a timing score from expiring signals, contact scores by role and seniority, a fit-by-timing tier matrix with actions, validation against past deals and monthly monitoring. Use whenever someone needs account scoring, ICP scoring, prioritised target lists, tiers for outbound, a way to decide where to spend credits and personalisation, or scoring formulas in Clay or a CRM."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/icp-account-scoring/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-13"
---

# ICP and Account Scoring

Without scoring, outbound teams treat every account the same: equal effort on a perfect-fit company showing buying signals and on a poor-fit company that will never buy. Scoring fixes this by ranking accounts and contacts so time, credits and personalisation go where they pay off. Many scores fail because they are built from opinions, give points for everything so every account looks good, or mix fit and timing into one unexplained number.

This skill builds account and contact scoring for GTM workflows: separating fit (who should buy) from intent or timing (who might buy now), choosing attributes from won and lost deal data, setting weights and hard exclusions, creating tiers with clear actions, scoring contacts by role and seniority, validating against history and maintaining the model.

## Operating principles
1. **Fit and timing are different.** Score them separately, then combine into tiers.
2. **Use evidence.** Base weights on won, lost and churned customers, not guesses.
3. **Hard exclusions first.** Disqualifiers remove accounts before any points are added.
4. **Few attributes, clear weights.** Five to eight attributes beat thirty.
5. **Every tier has an action.** Scores exist to decide what happens next.

## Score structure
| Component | Examples | Output |
|---|---|---|
| Exclusions | Existing customer, competitor, unsupported country, too small | Excluded |
| Fit score (0 to 100) | Industry, employee range, revenue, region, tech stack, business model | Fit points |
| Intent or timing score (0 to 100) | Hiring for relevant roles, funding, tech changes, website visits, content engagement | Timing points |
| Contact score | Role, seniority, department, decision power | Contact priority |
| Tier | Combination of fit and timing | A, B, C, D |

## Tier matrix
| | High timing | Low timing |
|---|---|---|
| High fit | Tier A: personalised outreach now | Tier B: nurture, light outreach, watch signals |
| Low fit | Tier C: only if strong signal and capacity | Tier D: do not contact |

## When to use, and when not to
Use it when building target lists, prioritising outbound, routing accounts to reps, deciding where to spend credits and AI personalisation, or aligning sales and marketing on targets.

Don't use it for inbound lead scoring based on marketing engagement alone (the CRM and Lifecycle `lead-scoring-routing` skill) or for defining the ICP from scratch with research (the Product Marketing `ideal-customer-profile` skill).

## Inputs
- ICP description and segments.
- CRM data on won, lost and churned deals with firmographics.
- Available enrichment fields and signals.
- Sales capacity and routing rules.
- Exclusion lists.

## Workflow

### Step 1. Gather outcome data
Export won, lost and churned accounts for the last 12 to 24 months with firmographics and deal size.

### Step 2. Find patterns
Compare win rates and deal sizes by industry, size, region, tech stack and other attributes.

### Step 3. Set exclusions
Hard rules that remove accounts entirely.

### Step 4. Build the fit score
Pick five to eight attributes; give points proportional to their impact on win rate and value.

### Step 5. Build the timing score
Pick signals that preceded past deals, with points and an expiry window (for example, a funding round counts for 90 days).

### Step 6. Score contacts
Points for target roles, seniority and departments; mark buyers, champions and users.

### Step 7. Define tiers and actions
Thresholds for A, B, C and D with the action, owner and personalisation level for each.

### Step 8. Validate
Score past accounts and check that won deals fall mostly in A and B; adjust weights.

### Step 9. Implement and monitor
Formula columns in the table, synced to the CRM; review conversion by tier monthly.

## Fit score example
```
| Attribute | Value | Points |
| Industry | Fintech, payments | 30 |
| Industry | Other financial services | 15 |
| Employees | 50 to 1,000 | 25 |
| Region | UK, Ireland, Nigeria | 15 |
| Tech | Uses Stripe or Adyen | 15 |
| Business model | B2B or marketplace | 15 |
Maximum: 100
```

## Timing score example
```
| Signal | Points | Valid for |
| Hiring head of growth or marketing | 30 | 60 days |
| Raised funding | 25 | 90 days |
| New market launch announced | 20 | 90 days |
| Visited pricing page | 25 | 14 days |
Maximum: 100
```

## Contact score example
```
| Role | Points |
| Head of growth, VP marketing, CMO | 40 (buyer) |
| Growth or lifecycle manager | 25 (champion) |
| Analyst, specialist | 10 (user) |
```

## Validation check
```
| Tier | Past accounts | Won | Win rate |
| A | 120 | 18 | 15% |
| B | 340 | 20 | 6% |
| C | 410 | 5 | 1% |
| D | 900 | 1 | 0.1% |
```
A model that works shows win rates falling clearly from A to D.

## Explaining scores
Store the reasons with each score, such as "fintech (+30), 50 to 1,000 staff (+25), hiring head of growth (+30)". Reps trust and use scores they can read, and explanations make it easy to spot attributes that need new weights. Review conversion by tier every month and re-weight every quarter, or sooner if the product, pricing or market changes.

## Sharing the model
Publish the scoring tables, tier actions and last validation in one document that sales, marketing and leadership can read, and agree changes in a short monthly review rather than editing formulas quietly.

Keep old versions of the model so changes in results can be traced to changes in weights.

Revisit exclusions whenever the product or pricing changes.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Little deal history | Start with expert weights, label as provisional, revisit after 50 to 100 deals |
| Every account scores high | Tighten attributes; check for overlapping points |
| New market or product | Separate model until data exists |
| Signals are noisy | Fewer, stronger signals with expiry dates |
| Sales disagree with tiers | Review lost and won examples together; adjust openly |
| Large enterprise accounts | Score at account level; contacts mapped to buying groups |

## Handoffs to related skills
- ICP definition: the Product Marketing `ideal-customer-profile` skill
- Signals feeding timing: `signal-based-outbound`
- Table formulas: `clay-table-design`
- Routing by tier: `crm-sync-routing`
- Lead scoring for inbound: the CRM and Lifecycle `lead-scoring-routing` skill
- Reporting by tier: `gtm-reporting`

## Worked example
A payments company scored accounts with 22 attributes and 80% of its list was "high priority". Analysis of 18 months of deals showed industry, employee range, region and payment provider explained most wins, and hiring a growth leader or raising funding preceded many deals. The new model used five fit attributes, three timed signals, contact scoring by role and four tiers. Validation showed a 15% win rate in tier A versus 1% in tier C. Reps focused on tier A, AI personalisation ran only for A and B, and meetings per rep rose while credits per meeting fell.

## Common mistakes
- Mixing fit and timing in one unexplained score.
- Weights based on opinion rather than deal data.
- Too many attributes, so every account looks good.
- Signals that never expire.
- Tiers without actions.

## Output format
```
1. Exclusion rules
2. Fit score table
3. Timing score table with expiry windows
4. Contact score table
5. Tier matrix and actions
6. Validation against past deals
7. Monitoring plan
```

## Self-check before you answer
- Are fit and timing scored separately?
- Are weights grounded in deal data or labelled provisional?
- Do signals expire?
- Does validation show win rates falling from tier A to D?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/icp-account-scoring/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
