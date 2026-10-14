---
name: meta-ads
description: "Build, audit and scale Meta ads on Facebook and Instagram: pixel and Conversions API with deduplication and event match quality, consolidated Advantage+ structures with existing-customer controls, creative volume and diversity as targeting, testing campaigns, budgets and scaling rules, incremental attribution and lift tests, and checks against first-party data. Use whenever someone asks about Facebook ads, Instagram ads, Meta Advantage+, rising Meta CPA, creative fatigue, Meta campaign structure, CAPI, scaling Meta spend or why Ads Manager results don't match sales."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/meta-ads/
  category: marketing
  subcategory: performance-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Meta Ads (Facebook and Instagram)

Meta advertising has moved from detailed targeting to automation. Advantage+ campaigns choose audiences, placements and budgets; the delivery system picks which ad to show which person, and creative has become the main targeting signal. Practitioners widely report that Meta's newer ad retrieval systems reward many clearly different creatives over small variations of one idea. [Consensus] Meta also introduced an incremental attribution option in 2025 that optimises for conversions it estimates would not have happened otherwise. [Reported, Meta]

This skill builds, audits and scales Meta campaigns: account structure, Advantage+ settings, conversion signals with the Conversions API, creative volume and diversity, audiences and exclusions, budgets, and measurement beyond Ads Manager.

## Operating principles
1. **Signal quality first.** Pixel plus Conversions API, deduplicated, with good event match quality and the right optimisation event.
2. **Fewer campaigns, more data.** Consolidated structures learn faster than many small ad sets.
3. **Creative is targeting.** Different angles, formats and people reach different audiences.
4. **Separate new customers from existing ones** in goals and reporting where the business cares about acquisition.
5. **Measure outside Ads Manager.** View-through and click windows inflate results; use lift tests and your own data.

## Account structure (typical e-commerce)
| Campaign | Purpose | Notes |
|---|---|---|
| Advantage+ sales (prospecting) | Main acquisition | Existing customer budget cap or exclusions where available; broad delivery |
| Testing campaign | New creative concepts | Fixed budget; graduate winners to the main campaign |
| Retargeting (small) | Cart and product viewers | Only if lift tests show value |
| Catalogue (dynamic product ads) | Product-level personalisation | Needs a clean catalogue |
| Lead generation (B2B or services) | Instant forms or site leads | Import qualified outcomes via CAPI |

## When to use, and when not to
Use it for new Meta accounts, audits, scaling plateaus, rising CPAs, creative fatigue, Advantage+ adoption and measurement disputes.

Don't use it for TikTok, LinkedIn or other social platforms (`paid-social-tiktok-linkedin`) or for creative production processes in depth (`ad-creative-testing`).

## Inputs to ask for, in one message
1. Ads Manager exports: campaigns, ad sets, ads, results and breakdowns for 90 days.
2. Events Manager status: pixel, CAPI, deduplication, event match quality, domain verification.
3. Business goals: new customers, revenue, leads, payback.
4. Creative library and production capacity.
5. Customer lists and any lift test results.

## Workflow

### Step 1. Fix signals
Pixel plus CAPI with deduplication; prioritised events set; improve event match quality with hashed email and phone where consented; optimise for purchase or qualified lead, not clicks.

### Step 2. Consolidate structure
Move to fewer campaigns with broad delivery; avoid audience overlap between ad sets; keep a separate testing campaign for new concepts.

### Step 3. Configure Advantage+
Set existing customer definitions with customer lists and pixel audiences; use budget caps for existing customers when acquisition is the goal; review placement and creative enhancements for brand safety.

### Step 4. Build creative volume and diversity
Aim for many distinct concepts: different problems, benefits, formats (UGC, demo, testimonial, founder, static, carousel), hooks and people. Refresh before fatigue.

### Step 5. Set budgets and bidding
Campaign budget optimisation for consolidated campaigns; cost cap or ROAS goals only when you understand the trade-off in volume; avoid frequent large changes that reset learning.

### Step 6. Read results properly
Compare Ads Manager with GA4 and your own orders; check attribution settings (click and view windows); use breakdowns for placement, age and creative.

### Step 7. Test incrementality
Conversion lift studies or geo tests for prospecting and retargeting before scaling.

### Step 8. Scale
Increase budgets in steps; add creative as you scale; watch frequency and new-customer share.

## Creative testing routine
- Launch 3 to 5 new concepts per week or fortnight in the testing campaign, depending on budget.
- Judge on cost per acquisition or new customer from your data, plus hook rate and hold rate for video.
- Move winners into the main campaign without editing them.
- Retire ads when frequency rises and results fall for two consecutive weeks.

## Creative diversity matrix
| Dimension | Options to vary |
|---|---|
| Angle | Problem, benefit, social proof, price or value, comparison, founder story, how it works |
| Format | UGC video, demo, testimonial, static image, carousel, collection, motion graphic |
| Hook (first 3 seconds) | Question, bold claim with proof, surprising visual, result first |
| Person | Customer, creator, expert, founder, no person |
| Length | 6 to 15 seconds, 15 to 30 seconds, longer explainers |
| Offer | No offer, bundle, free shipping, limited-time (sparingly) |
A concept is a new combination of angle and format, not a new colour or caption on the same video.

## Reading Ads Manager without fooling yourself
- Check the attribution setting (for example 7-day click and 1-day view) and compare click-only results.
- Compare purchases and revenue with your commerce data for the same period.
- Separate new and returning customers in your own data.
- Treat view-through conversions as a hypothesis to test, not proof.
- Use breakdowns to find what works, then confirm with lift tests before shifting large budgets.

## Scaling rules
1. Raise budgets by about 20% at a time, a few days apart, unless a test shows strong headroom.
2. Add new creative as you scale; frequency rises fast with fixed creative.
3. Watch new-customer CPA and blended MER, not only platform ROAS.
4. If CPA rises for a week after a change, hold rather than reverse immediately; learning needs time.
5. Log every major change with the date for later analysis.

## Lead generation on Meta
- Use higher-intent instant forms (with a review step and qualifying questions) or send traffic to a fast site form.
- Send CRM outcomes back via CAPI so delivery learns which leads become customers.
- Remove fields that add friction without improving qualification.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Low budget | One campaign, few ads, broad delivery; give learning time |
| Lead quality poor | Higher-intent forms, qualifying questions, CAPI with CRM outcomes |
| Special ad categories (housing, employment, credit, politics) | Follow restricted targeting rules and authorisations |
| Brand safety concerns | Review placements and inventory filters; exclude where necessary |
| Creative production bottleneck | Use customer UGC, creators, simple statics and iterations of winning angles |

## Handoffs to related skills
- Tracking and CAPI: `conversion-tracking-capi`
- Creative concepts and testing: `ad-creative-testing`
- Audiences and customer lists: `audience-first-party-data`
- Lift and geo tests: `incrementality-testing`
- Landing pages: `landing-page-cro`

## Worked example
A skincare brand ran 22 Meta campaigns with interest targeting and five ads each. CPA had risen for months. The rebuild created one Advantage+ sales campaign with an existing-customer budget cap, a testing campaign launching four new concepts a week (creator demos, dermatologist explainer, before-and-after with disclaimers, founder story, static benefit cards), CAPI with deduplication raising event match quality, and a geo test on retargeting. CPA for new customers fell, retargeting proved weakly incremental and was cut back, and budget scaled in 20% steps while new creative kept frequency in check.

## Output format
```
# Meta Ads plan: <account>, <date>
## Signal health (pixel, CAPI, dedup, EMQ, events)
## Structure and Advantage+ settings
## Creative plan (concepts, formats, cadence)
## Budgets, bidding and scaling rules
## Measurement (Ads Manager vs own data, lift tests)
## Monitoring routine
```

## Common mistakes
- Many small ad sets fighting each other.
- Too few, too similar creatives.
- Optimising for clicks or landing page views.
- Counting existing customers as acquisition.
- Trusting view-through results without tests.

## Questions to ask before you change the account
- Is the goal new customers, revenue or leads, and how is each measured?
- How much creative can the team produce each week?
- What does your own data say compared with Ads Manager?

## Self-check before you answer
- Are pixel and CAPI deduplicated with good match quality?
- Is the structure consolidated with a testing path?
- Is creative diverse and refreshed?
- Are results checked against first-party data and tests?

## Official documentation
- Meta Conversions API: https://developers.facebook.com/docs/marketing-api/conversions-api
- Meta Business Help Centre: https://www.facebook.com/business/help
- Meta Advantage+ overview: https://www.facebook.com/business/ads/meta-advantage-plus

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/meta-ads/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
