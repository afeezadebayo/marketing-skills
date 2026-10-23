---
name: conversion-tracking-capi
description: "Audit and design conversion tracking for Google Ads, GA4, Meta, TikTok, LinkedIn and Microsoft Ads: one primary conversion per action, Consent Mode v2 in consent-required markets, enhanced conversions, Meta Conversions API and other server-side events with deduplication, revenue, profit or qualified-lead values, offline conversion imports, testing and daily monitoring. Use whenever someone mentions conversion tracking, duplicate conversions, Consent Mode v2, Meta CAPI, server-side tracking, enhanced conversions, offline conversion imports, event match quality or ad platforms reporting different numbers."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/conversion-tracking-capi/
  category: marketing
  subcategory: performance-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Conversion Tracking, Consent Mode and Conversions API

Every automated bidding system learns from the conversions you send it. Send duplicates and it overspends; send nothing for consent-denied users and it underbids in the markets that matter; send leads that never become customers and it finds more of them. In 2026, good tracking means consent-aware tags, server-side events, deduplication, offline outcomes and values that reflect profit.

This skill audits and designs conversion tracking for Google Ads, GA4, Meta, TikTok, LinkedIn and Microsoft Ads, including Consent Mode, enhanced conversions, the Meta Conversions API and other server-side APIs, and offline conversion imports.

## What has changed recently
| Change | What it means | Label |
|---|---|---|
| Consent Mode v2 required for Google Ads features with EEA and UK users since March 2024 | Without it, measurement and remarketing for those users are limited | Confirmed, Google |
| Google discontinued most Privacy Sandbox APIs (October 2025) and kept third-party cookies in Chrome under existing user choice | No sudden cookie cut-off in Chrome; Safari and Firefox still restrict tracking | Confirmed, Google (as reported) |
| From June 2026, Consent Mode is the control governing Google Ads use of identifiers from the Google tag | Consent Mode setup matters even more | Reported |
| Server-side APIs (Meta CAPI, TikTok Events API, LinkedIn CAPI, Google enhanced conversions) are standard practice | Recover signal lost to browsers and ad blockers, with consent | Consensus |

## Operating principles
1. **One source of truth per conversion.** Each platform should count each conversion once.
2. **Consent first.** Server-side tracking doesn't remove the need for consent under GDPR and similar laws.
3. **Optimise for value.** Pass revenue, profit or qualified outcomes, not just counts.
4. **Primary goals drive bidding.** Keep only the conversions you want to optimise for as primary.
5. **Test after every release.** Site changes break tags more than anything else.

## When to use, and when not to
Use it when results look too good or too bad, after site or checkout changes, when launching in consent-required markets, when platforms show poor event match quality, and for lead businesses that need offline outcomes.

Don't use it for attribution debates or channel allocation (`paid-media-reporting`, `incrementality-testing`).

## Inputs to ask for, in one message
1. List of conversion actions per platform and which are primary.
2. Tag setup: Google Tag Manager, gtag, platform pixels, server-side container.
3. Consent management platform and markets served.
4. Commerce or CRM platform and how orders or leads are recorded.
5. Recent site changes and any known discrepancies.

## Workflow

### Step 1. Inventory and map
For each platform: conversion actions, source (tag, GA4 import, API, offline import), primary or secondary, value setting, counting (one or every).

### Step 2. Remove duplicates
One primary purchase conversion per platform. If both a native tag and a GA4 import exist, choose one for bidding and set the other as secondary.

### Step 3. Set up Consent Mode
Default consent states set to denied before the banner where law requires; update on choice; all four signals (ad_storage, analytics_storage, ad_user_data, ad_personalization). Use advanced mode where your legal basis allows, so Google can model conversions for consent-denied users.

### Step 4. Add server-side events
Meta Conversions API, TikTok Events API, LinkedIn Conversions API and Google enhanced conversions, sending hashed first-party data with consent. Deduplicate browser and server events with a shared event ID.

### Step 5. Pass values
Revenue for every purchase; consider profit-based values or new-customer values. For leads, assign values by stage and import offline outcomes.

### Step 6. Import offline conversions
For lead businesses, send qualified lead, opportunity and closed-won events back to Google, Meta, LinkedIn and Microsoft with click IDs or hashed contact data.

### Step 7. Test
Tag Assistant, GA4 DebugView, Meta Events Manager test events and event match quality, platform diagnostics. Make a test purchase or lead and trace it through every system.

### Step 8. Monitor
Daily conversion counts by platform compared with orders or leads in your own system; alerts for drops or spikes.

## Tracking plan template
```
| Event | Trigger | Platforms | Method (tag/server/import) | Value | Primary? | Dedup key | Consent required |
| purchase | Order confirmed | Google, Meta, TikTok | Tag + server | Revenue (or profit) | Yes | order_id | Yes |
| qualified_lead | CRM stage = SQL | Google, Meta, LinkedIn | Offline import | Stage value | Yes (lead gen) | crm_id | n/a |
```

## Consent Mode signals
| Signal | Controls | Default before choice (consent-required markets) |
|---|---|---|
| ad_storage | Advertising cookies | denied |
| analytics_storage | Analytics cookies | denied |
| ad_user_data | Sending user data to Google for advertising | denied |
| ad_personalization | Personalised advertising (remarketing) | denied |
Basic mode loads Google tags only after consent; advanced mode sends cookieless pings before consent so Google can model conversions. Choose with your legal team.

## Deduplicating browser and server events
1. Generate one event ID per action (for example the order ID for a purchase).
2. Send the same event ID with the browser pixel event and the server event.
3. Use the same event name on both.
4. Check the platform's deduplication diagnostics (Meta Events Manager shows deduplicated events).
5. Monitor event match quality and improve it with more hashed identifiers (email, phone) where consented.

## Lead value ladder example
| Stage | Example value | Sent to |
|---|---|---|
| Form submitted | Low | All platforms (secondary) |
| Qualified lead (SQL) | Medium | Google, Meta, LinkedIn (primary for bidding) |
| Opportunity created | Higher | Google, LinkedIn |
| Closed won | Actual contract value | Google, Microsoft, LinkedIn |
Calibrate values from historical conversion rates between stages and average deal value.

## Release checklist (run after every site change)
- Test purchase or lead in each key template.
- Confirm one event per action in each platform's debug tool.
- Check consent banner still blocks and releases tags correctly.
- Compare the next 48 hours of conversions with orders or leads in your own system.
- Check that values and currencies are passed.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Purchase happens on a third-party checkout | Use server-side events from the checkout platform or post-purchase webhooks |
| Phone sales | Call tracking and offline imports with call IDs |
| App plus web | Align events across Firebase or MMPs and web tags; avoid double counting |
| Low volume of final conversions | Optimise on a well-correlated earlier event (qualified lead) with care |
| Strict consent markets with low opt-in | Advanced Consent Mode and modelled conversions where lawful; set expectations |

## Handoffs to related skills
- Overall account review: `paid-media-audit`
- First-party audiences: `audience-first-party-data`
- Reporting: `paid-media-reporting`
- Channel bidding: `google-search-ads`, `performance-max-shopping`, `meta-ads`

## Worked example
A lead-generation firm in financial services optimised Google and Meta for form fills. Sales said most leads were unqualified. Tracking showed Google Ads counting form fills twice (two tags), Meta pixel only (no CAPI, event match quality poor) and no offline imports. The fix: one form conversion per platform, Meta CAPI with deduplication, Consent Mode v2 with advanced mode for UK users, and weekly offline imports of qualified and closed outcomes with stage values. Bidding switched to qualified-lead value. Form volume fell, but qualified leads and closed revenue per pound rose within two months.

## Output format
```
# Tracking review: <business>, <date>
## Conversion inventory and issues by platform
## Consent Mode status by market
## Server-side and deduplication status
## Values and offline imports
## Tracking plan (table)
## Test results and monitoring setup
```

## Common mistakes
- Two primary conversions for the same action.
- Server-side events without deduplication.
- Consent defaults set to granted before the banner.
- Optimising lead campaigns on raw form fills.
- No monitoring after site releases.

## Questions to ask before you recommend changes
- Which conversions drive bidding today on each platform?
- Which markets require consent, and what does the CMP send?
- Where is the source of truth for orders and leads?

## Self-check before you answer
- Is each conversion counted once per platform?
- Is Consent Mode correct for consent-required markets?
- Are server events deduplicated and consented?
- Are values and offline outcomes passed for bidding?

## Official documentation
- Google consent mode: https://support.google.com/google-ads/answer/10000067
- Google enhanced conversions: https://support.google.com/google-ads/answer/9888656
- Meta Conversions API: https://developers.facebook.com/docs/marketing-api/conversions-api
- TikTok Events API: https://business-api.tiktok.com/portal/docs
- LinkedIn Conversions API: https://learn.microsoft.com/en-us/linkedin/marketing/conversions/conversions-overview

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/conversion-tracking-capi/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
