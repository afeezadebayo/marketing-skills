---
name: paid-media-audit
description: "Audit paid media across Google Ads, Microsoft Ads, Meta, TikTok and LinkedIn in eight layers (tracking and consent, goals and values, structure, bidding and budgets, audiences, search terms and placements, creative and landing pages, incrementality and allocation), reconcile platform results with GA4, CRM and finance, and replace platform ROAS with blended MER, new-customer CAC, contribution margin and payback. Use whenever someone asks for a Google Ads audit, Meta ads audit, PPC audit, paid social review, why ROAS looks good but revenue doesn't grow, before changing agencies or before scaling ad spend."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/paid-media-audit/
  category: marketing
  subcategory: performance-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Paid Media Audit

Paid media accounts drift. Campaigns pile up, automation takes over bidding and targeting, conversion tracking breaks quietly after a site release, and reports keep showing healthy platform ROAS while the business wonders why revenue isn't growing. In 2026 the drift is faster: Google pushes AI Max and Performance Max, Meta pushes Advantage+, and every platform grades its own homework.

This skill audits paid media across Google Ads, Microsoft Ads, Meta, TikTok, LinkedIn and others in one pass. It checks measurement first, then structure, bidding, audiences, creative, landing pages and budget allocation, and asks the question platforms won't: how much of this is incremental?

## Operating principles
1. **Measurement before optimisation.** Broken or duplicated conversions make every bidding decision wrong.
2. **Platforms report in their own favour.** Compare platform-reported results with analytics, the CRM, finance and incrementality tests.
3. **Automation needs good inputs.** Value-based conversions, clean audiences, strong creative and clear exclusions decide what AI bidding learns.
4. **Margin, not ROAS.** A campaign can show high ROAS while losing money once product costs, returns and fees are counted.
5. **Test before you scale.** Changes in budget and structure should be measured, not assumed.

## The eight layers
| Layer | What to check | Typical high-impact finding |
|---|---|---|
| 1. Tracking and consent | Conversion actions, duplicates, primary vs secondary goals, Consent Mode, Conversions API, enhanced conversions, offline imports | Purchases counted twice (tag plus GA4 import) |
| 2. Goals and values | What bidding optimises for; value rules; new-customer goals; profit data | Optimising for leads, not qualified pipeline |
| 3. Account structure | Campaign split by margin, intent, geography and funnel; overlap | Brand and non-brand mixed, hiding true acquisition cost |
| 4. Bidding and budgets | Bid strategies, targets, learning periods, budget-limited campaigns | tROAS targets set from platform data, not margin |
| 5. Audiences and signals | First-party lists, exclusions, lookalikes, audience signals | Existing customers counted as new acquisition |
| 6. Search terms and placements | Search terms, negatives, brand exclusions, placement quality | AI Max or broad match spending on irrelevant queries |
| 7. Creative and landing pages | Asset variety, fatigue, message match, page speed and conversion rate | One video for 18 months; slow mobile landing page |
| 8. Incrementality and allocation | Lift tests, geo tests, MMM, blended metrics | No evidence that retargeting adds sales |

## When to use, and when not to
Use it when inheriting accounts, before an agency change, when blended efficiency falls while platform ROAS looks fine, before scaling budget, after a tracking or site change, and quarterly as a health check.

Don't use it to build one channel from scratch (use the channel skills: `google-search-ads`, `performance-max-shopping`, `meta-ads`, `paid-social-tiktok-linkedin`) or to design a lift test in depth (`incrementality-testing`).

## Inputs to ask for, in one message
1. Read access to ad accounts, or exports of campaigns, ad groups, search terms, assets and conversions for 90 days.
2. Conversion action setup, tag implementation, Consent Mode and Conversions API status.
3. GA4 and CRM or commerce data for the same period (orders, revenue, new versus returning customers, leads to pipeline).
4. Margins by product or service, return rates and customer lifetime value if known.
5. Business goals: growth, profitability, new customers, payback period.
6. Any lift tests, geo tests or MMM results.

## Workflow

### Step 1. Audit tracking
List every conversion action per platform. Check which are primary for bidding, find duplicates, test tags with platform tools (Tag Assistant, Meta Events Manager), check Consent Mode in consent-required markets, Conversions API event match quality and deduplication, and offline conversion imports for lead businesses.

### Step 2. Reconcile results
Compare platform conversions and revenue with GA4, CRM and finance for the same dates. Large gaps reveal double counting, view-through credit or broken tags.

### Step 3. Check goals and values
Is bidding optimising for what makes money? For e-commerce, pass revenue and consider profit or new-customer values. For lead generation, import qualified or closed outcomes so bidding learns which leads matter.

### Step 4. Review structure
Separate brand from non-brand, prospecting from retargeting, high-margin from low-margin products and key markets from the rest. Remove overlap that splits learning or inflates costs.

### Step 5. Review bidding and budgets
Check targets against margins, learning status, budget limits and how often changes reset learning.

### Step 6. Review search terms, placements and audiences
Search term relevance (especially with broad match and AI Max), negatives, brand exclusions, placement exclusions, audience exclusions for existing customers.

### Step 7. Review creative and landing pages
Asset count and variety, performance by asset, fatigue signals, message match between ad and page, mobile speed, conversion rate by page.

### Step 8. Assess incrementality and allocation
What evidence exists that each channel adds sales? Compare blended metrics (total revenue over total spend, new customers over spend) with platform claims. Recommend tests where evidence is missing.

### Step 9. Score and plan
Score each layer 0 to 3 and write a 90-day plan ranked by money at stake and effort.

## Metrics that matter more than platform ROAS
| Metric | Definition | Why |
|---|---|---|
| Blended MER | Total revenue ÷ total marketing spend | Can't be inflated by one platform's attribution |
| New-customer CAC | Spend ÷ new customers (from your own data) | Separates acquisition from retargeting existing buyers |
| Contribution margin after ads | Revenue minus product costs, fees, returns and ad spend | Shows profit, not just revenue |
| Payback period | Months to recover CAC from gross margin | Sets how aggressively you can scale |
| Incremental ROAS | Incremental revenue from tests ÷ spend | The real return |

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Lead generation with long sales cycles | Import offline outcomes (qualified, opportunity, closed) and bid on them |
| Very small budgets | Fewer campaigns, simpler structure, more data per campaign |
| Marketplaces (Amazon) significant | Treat retail media separately; check halo effects on brand search |
| Heavy brand search spend | Test whether brand ads are incremental where competitors don't bid |
| Agency reports only platform numbers | Ask for reconciliation with your own data |
| Regulated categories | Check platform policies (finance, health, gambling) and approvals first |

## Handoffs to specialist skills
- Budget and channel plan: `media-planning-budgeting`
- Tracking, consent and server-side: `conversion-tracking-capi`
- Lift and geo tests: `incrementality-testing`
- Marketing mix modelling: `marketing-mix-modelling`
- Google Search and AI Max: `google-search-ads`
- Performance Max and Shopping: `performance-max-shopping`
- Meta: `meta-ads`
- TikTok, LinkedIn and other social: `paid-social-tiktok-linkedin`
- Creative: `ad-creative-testing`
- Landing pages: `landing-page-cro`
- Audiences and first-party data: `audience-first-party-data`
- Reporting: `paid-media-reporting`

## Worked example
A DTC furniture brand spent heavily across Google and Meta with platform ROAS above target, yet blended MER had fallen for three quarters. The audit found purchases counted twice in Google Ads (a native tag plus an imported GA4 conversion, both primary), Performance Max spending a large share on brand queries and existing customers, Meta retargeting with no evidence of incrementality, and a mobile product page loading slowly. Fixes: remove the duplicate conversion, add brand exclusions and customer list exclusions to PMax, run a geo holdout on retargeting, pass profit-based values and speed up the page. Platform ROAS fell on paper, but blended MER and contribution margin rose over the next quarter.

## Output format
```
# Paid media audit: <business>, <date>
## Summary (biggest leak, biggest opportunity, first move)
## Reconciliation: platform vs analytics vs CRM vs finance
## Layer scores
| Layer | Score 0-3 | Key findings | Evidence |
## 90-day plan
| # | Action | Channel | Money at stake | Effort | Skill | Owner | Re-check |
```

## Common mistakes
- Optimising campaigns before fixing tracking.
- Taking platform ROAS at face value.
- Mixing brand and non-brand results.
- Letting automation optimise for the wrong conversion.
- Scaling without margin or payback data.

## Questions to ask before you recommend changes
- What does finance consider the true revenue and margin?
- Which conversion actions drive bidding today?
- What evidence exists that each channel is incremental?
- What payback period can the business afford?

## Self-check before you answer
- Did I audit tracking and reconcile with first-party data first?
- Are goals and values aligned with profit?
- Did I separate brand, retargeting and new-customer results?
- Does every action have a skill, owner and re-check date?

## Official documentation
- Google Ads conversion tracking: https://support.google.com/google-ads/answer/1722022
- Google consent mode: https://support.google.com/google-ads/answer/10000067
- Meta Conversions API: https://developers.facebook.com/docs/marketing-api/conversions-api
- Google Ads Performance Max: https://support.google.com/google-ads/answer/10724817

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/paid-media-audit/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
