---
name: cro-audit
description: "Audit a website or app conversion journey end to end: tracking, segmented funnels and sized drop-offs, landing, product, pricing, sign-up and checkout templates, forms, trust and social proof, mobile and speed, qualitative evidence from recordings, surveys and user tests, and findings written as hypotheses, separated into fixes, tests and research and prioritised. Use whenever someone asks for a CRO audit, conversion rate optimisation review, why the website doesn't convert, falling conversion rates, where visitors drop off, or what to test first."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/conversion-rate-optimization/cro-audit/
  category: marketing
  subcategory: conversion-rate-optimization
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# CRO Audit

Conversion rate optimisation (CRO) is often treated as a list of tweaks: change the button colour, add a testimonial, shorten the form. Those changes sometimes help, but without understanding why visitors don't convert, most of them are guesses. A CRO audit builds that understanding first: where in the journey visitors drop off, for whom, and why, using analytics, behaviour data and research. Every finding ends as a hypothesis with a metric, not an opinion.

This skill audits a website or app's conversion journey end to end: tracking, funnels, key templates (landing, product, pricing, sign-up, checkout), forms, trust, mobile experience, speed and the research behind them. It returns a prioritised list of hypotheses and hands each to a specialist skill. It is the entry point for the Conversion Rate Optimization set.

## Operating principles
1. **Data and research before opinions.** Find where and why people drop off before proposing changes.
2. **Every finding becomes a hypothesis.** "Because [evidence], changing [thing] for [audience] will improve [metric]."
3. **Optimise for business outcomes.** Revenue, qualified leads and retained customers, not clicks.
4. **Segment everything.** Device, traffic source, new versus returning and country often explain more than averages.
5. **Fix broken things first.** Bugs, slow pages and tracking errors are wins that need no test.

## Audit areas
| Area | What to check | Typical finding |
|---|---|---|
| 1. Tracking | Conversion events, funnel steps, revenue, consent | Purchases double-counted; form submits not tracked |
| 2. Funnel performance | Step conversion by device, source, segment | Mobile checkout converts at half the desktop rate |
| 3. Landing pages | Message match, clarity, proof, calls to action | Ads promise one thing, page shows another |
| 4. Product or feature pages | Information, images, reviews, objections | Missing sizing, delivery or compatibility details |
| 5. Pricing page | Plan clarity, recommended plan, FAQs | Visitors can't tell which plan fits |
| 6. Forms and sign-up | Fields, errors, friction, social sign-in | Twelve fields where four would do |
| 7. Checkout and cart | Costs, guest checkout, payment options, errors | Delivery cost revealed only at the last step |
| 8. Trust and social proof | Reviews, guarantees, security, brand signals | No reviews near the decision point |
| 9. Mobile and speed | Layout, tap targets, load time, Core Web Vitals | Slow mobile pages; buttons too small |
| 10. Research and testing practice | Surveys, recordings, interviews, test log | No research; tests chosen by opinion |

## When to use, and when not to
Use it when conversion rates fall, before redesigns, when traffic grows but sales don't, when starting a CRO programme and when paid media costs rise because pages convert poorly.

Don't use it for traffic acquisition problems (the SEO and Performance Marketing skills) or for analysing a single test result (the Growth Marketing `experiment-readout` skill).

## Inputs to ask for, in one message
1. Business model, primary conversions (purchase, sign-up, demo, lead) and their value.
2. Analytics access or exports: funnels, conversion by page, device, source and segment for 90 days.
3. Key URLs: home, landing pages, product, pricing, sign-up, checkout.
4. Any heatmaps, session recordings, surveys, user tests or past test results.
5. Page speed data and Core Web Vitals.
6. Traffic volume per key page, to judge what can be tested.

## Workflow

### Step 1. Verify tracking
Confirm each conversion and funnel step fires once with correct values, on every device. Fix tracking before analysing.

### Step 2. Map the funnel
From entry to conversion, with conversion and drop-off at each step, segmented by device, source and new versus returning.

### Step 3. Find the biggest leaks
Size each drop-off by lost conversions and value. Focus on high-traffic, high-value steps.

### Step 4. Review key templates
Walk through each template as a first-time visitor on mobile and desktop. Note friction, confusion, missing information and weak proof.

### Step 5. Gather qualitative evidence
Session recordings at leaking steps, on-page surveys ("What's stopping you today?"), support tickets, reviews and short user tests.

### Step 6. Check speed and mobile
Field data by template; tap targets, layout shifts, keyboard types on forms.

### Step 7. Write hypotheses
For each issue, a hypothesis with evidence, change, audience and metric.

### Step 8. Prioritise
Score by impact, confidence and ease; separate quick fixes (bugs, clear errors) from tests.

### Step 9. Plan
Fix list, test roadmap and research plan, each with owners.

## Hypothesis template
```
Because we saw [evidence: data, recordings, survey quotes],
we believe [change]
for [audience/segment]
will [increase/decrease] [primary metric],
measured by [method] over [duration].
```

## Fix, test or research?
| Situation | Action |
|---|---|
| Clear bug or error (broken button, JavaScript error, wrong price) | Fix now, no test needed |
| Strong evidence and low risk | Implement and monitor |
| Plausible idea with uncertain impact and enough traffic | A/B test |
| Low traffic page | Implement bigger changes with before-and-after monitoring, or research more |
| Unclear cause | Research first (recordings, surveys, user tests) |

## Audit scorecard
| Area | Score 0-3 | Key findings | Evidence | Next step |
|---|---|---|---|---|
Scores: 0 broken or missing, 1 weak, 2 solid, 3 strong and tested.

## Quick wins checklist
- Broken links, buttons or forms on key templates.
- JavaScript errors in checkout or sign-up.
- Missing or wrong prices, delivery costs or stock information.
- Slow mobile pages on high-traffic templates.
- Form fields that reject valid input (postcodes, phone formats, names with accents).

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Low traffic site | Focus on research and fixing obvious friction; test only big changes |
| B2B with long cycles | Optimise for qualified leads and pipeline, not raw form fills |
| Many traffic sources with different intent | Audit landing pages per source |
| App plus website | Map the journey across both; check handoffs |
| Regulated industries | Keep required disclosures while simplifying presentation |

## Handoffs to specialist skills
- Research methods: `conversion-research`
- Landing pages: `landing-page-optimisation`
- Forms: `form-optimisation`
- Pricing page: `pricing-page-optimisation`
- Checkout: `checkout-optimisation`
- Sign-up and onboarding: `signup-flow-optimisation`
- Popups: `popups-onsite-messaging`
- Social proof: `social-proof-trust`
- Copy tests: `conversion-copywriting`
- Mobile: `mobile-conversion`
- Test planning: `cro-test-planning`
- Reporting: `cro-reporting`
- Experiment analysis: the Growth Marketing `experiment-readout` skill

## Worked example
An online furniture retailer's conversion rate fell over a year while traffic grew. Tracking was fine, but funnel analysis showed mobile visitors added to cart at similar rates to desktop and then abandoned checkout far more often. Recordings showed delivery charges appearing only at the final step and a postcode field that rejected valid formats. A one-question exit survey confirmed surprise costs. Quick fixes repaired the postcode validation; tests showed delivery costs on product pages and added express payment options. Mobile checkout completion rose substantially, and overall revenue per visitor improved.

## Output format
```
# CRO audit: <site>, <date>
## Summary (biggest leak, quick wins, first tests)
## Tracking check
## Funnel with segmented drop-offs and sizing
## Template findings
## Qualitative evidence
## Scorecard
## Hypotheses (prioritised) and fix list
## Test roadmap and research plan
```

## Common mistakes
- Testing opinions without research.
- Optimising for clicks instead of revenue or qualified leads.
- Ignoring mobile and segment differences.
- Testing on pages without enough traffic.
- Leaving obvious bugs unfixed while running tests.

## Questions to ask before you recommend changes
- Which conversion matters most, and what is it worth?
- Where do the most valuable visitors drop off?
- How much traffic does each key page get each week?

## Self-check before you answer
- Is tracking verified before analysis?
- Are drop-offs segmented and sized?
- Is every finding written as a hypothesis with evidence and a metric?
- Are fixes, tests and research separated and prioritised?

## Further reading
- Baymard Institute UX research: https://baymard.com/research
- Nielsen Norman Group articles: https://www.nngroup.com/articles/
- CXL conversion optimisation guides: https://cxl.com/blog/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/conversion-rate-optimization/cro-audit/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
