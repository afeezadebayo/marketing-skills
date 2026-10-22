---
name: ai-commerce-product-visibility
description: "Get products shortlisted, priced correctly and purchasable in AI shopping answers across Google AI Mode, ChatGPT, Copilot and Perplexity: shopping prompt tests, Merchant Center and feed quality, shopper-intent attributes, page, markup and feed alignment, reviews and editorial comparisons, and agent checkout through the Universal Commerce Protocol, the Agentic Commerce Protocol and platform integrations. Use whenever someone asks about AI shopping, ChatGPT shopping, products in AI Mode, product feeds for AI, Merchant Center for AI answers, agentic checkout, UCP or ACP for retailers, or why their products aren't recommended by AI assistants."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/aeo-geo/ai-commerce-product-visibility/
  category: marketing
  subcategory: aeo-geo
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Product Visibility in AI Shopping and Commerce

Shoppers now ask assistants to shortlist products: "best waterproof running shoes under £120 for wide feet". The answer draws on product data from feeds, merchant pages, reviews and editorial comparisons, and increasingly lets the shopper buy without leaving the assistant. Microsoft describes three data pipes behind AI shopping visibility: crawled web data, product feeds and APIs, and live website data agents see. [Microsoft Advertising, A guide to AEO and GEO, 2026]

This skill audits and improves how products appear in AI shopping answers across Google, ChatGPT, Copilot and Perplexity, from feed quality to agent checkout readiness.

## The three data pipes
| Pipe | What it is | Main tools |
|---|---|---|
| Crawled data | Product, category and review pages engines index | Product structured data, server-rendered pages, reviews |
| Feeds and APIs | Structured catalogue data pushed to platforms | Google Merchant Center, Microsoft Merchant Center, platform catalogues, ChatGPT merchant programmes |
| Live site data | What an agent sees and does on the site | Clear product pages, accurate stock and price, working checkout, agent protocols |

Google states that Merchant Center feeds and Google Business Profile help products and services appear in AI responses and other Search results. [Confirmed]

## Operating principles
1. **One truth for every product fact.** Price, stock, variants, shipping and returns must match across page, markup and feeds.
2. **Attributes answer shopper intent.** AI answers match long, specific requests; complete attributes (size range, material, use case, compatibility) decide inclusion.
3. **Reviews and editorial mentions count.** Shortlists draw on verified reviews and independent comparisons. [Consensus]
4. **Agent checkout is arriving through platforms.** Use your commerce platform's support for UCP or ACP rather than custom builds.
5. **Measure by product group.** Track which products appear for which shopping prompts and engines.

## When to use, and when not to
Use it for retailers, DTC brands, marketplaces and software sold self-serve, when products are missing from AI shopping answers, when assistants quote wrong prices, and when evaluating agent checkout.

Don't use it for general product page SEO alone (use the Content and Technical SEO skills) or for non-commerce entity work (`entity-optimisation`).

## Inputs to ask for, in one message
1. Catalogue size, platform and feed setup (Merchant Center accounts, other channels).
2. Feed diagnostics and disapprovals.
3. Sample product URLs per category and their structured data.
4. Review volume and platforms.
5. Shopping prompts customers use, by category and market.
6. Whether agent checkout (UCP, ACP or platform features) is enabled or planned.

## Workflow

### Step 1. Run shopping prompts
For top categories, run specific shopping prompts in Google AI Mode, ChatGPT, Copilot and Perplexity. Record which products and retailers appear, prices shown and sources cited.

### Step 2. Audit feed quality
Check titles (brand, type, key attribute), descriptions, GTINs, product categories, variants, images, price and availability freshness, shipping and returns. Fix disapprovals and warnings.

### Step 3. Enrich attributes
Add the attributes shoppers use in prompts: size and fit, materials, use cases, compatibility, certifications, sustainability claims with evidence. Keep them consistent across feed and page.

### Step 4. Align pages and markup
Product pages show the same facts in text; Product, Offer, shipping and return markup match; variants use `ProductGroup` where supported; prices and stock are in server-rendered HTML.

### Step 5. Strengthen reviews and comparisons
Invite verified buyers to review; respond to reviews; give editors of cited comparisons accurate specs and samples.

### Step 6. Evaluate agent commerce
| Option | Where | Route |
|---|---|---|
| Universal Commerce Protocol (UCP) | Google AI Mode and Gemini checkout for eligible merchants; announced 11 January 2026 with Shopify, Etsy, Wayfair, Target and Walmart | Merchant Center and supported platforms; waitlist where required [Confirmed, Google] |
| Agentic Commerce Protocol (ACP) | ChatGPT checkout, launched September 2025 with Stripe | Merchant application and supported platforms [Confirmed, OpenAI/Stripe] |
| Platform integrations | Shopify and others connecting merchants to several AI surfaces | Platform settings |

### Step 7. Measure
Track product appearance rate per prompt and engine, price accuracy, AI referral sessions and conversions by product group.

## Feed attribute checklist
- [ ] Title: brand + product type + key attribute + variant
- [ ] GTIN or MPN where available
- [ ] Accurate, current price and availability
- [ ] Variants with size, colour and material
- [ ] High-quality images, including in use
- [ ] Shipping cost and speed, return policy
- [ ] Use-case and compatibility attributes
- [ ] Same facts on page, in markup and in feed

## Worked example
An outdoor retailer's waterproof jackets rarely appeared in AI shopping answers despite strong reviews. Feed titles lacked the waterproof rating and fit, 30% of products had no GTIN, and prices on the page loaded by script after a currency check. The team rebuilt titles to include rating and fit, added GTINs and use-case attributes, rendered prices on the server, and added return-policy markup. Over the next two months, the jackets appeared in AI Mode and ChatGPT answers for 5 of 8 tracked prompts, with correct prices.

## Output format
```
# AI commerce visibility review: <brand>, <categories>, <date>
## Prompt results (engine x prompt: products shown, ours?, price accuracy, sources)
## Feed audit (issues, counts, fixes)
## Attribute enrichment plan
## Page and markup alignment
## Reviews and comparison plan
## Agent commerce assessment (UCP, ACP, platform)
## Measurement plan
```

## Shopping prompt library by category
| Category | Example prompts to test |
|---|---|
| Apparel | "waterproof running jacket for women under £150", "best rain jacket for cycling commutes" |
| Electronics | "noise cancelling headphones for flights under $200", "laptop for video editing with 32GB RAM" |
| Home | "quiet dishwasher for open-plan kitchen", "sofa bed for small flat" |
| Beauty | "fragrance-free moisturiser for sensitive skin" |
| B2B software | "invoicing software for agencies with multi-currency" |
Adapt with your products' real attributes and price points.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Prices vary by region or currency | Feed and page should show the correct local price; avoid script-only currency switching |
| Large catalogue with weak data | Fix top sellers and top categories first; template the rest |
| Products sold mainly through marketplaces | Make sure marketplace listings are accurate; agents may buy there |
| Sustainability or performance claims | Back each claim with a certification or test; unverified claims can mislead and break rules |
| Out-of-stock items still recommended | Keep availability current in feeds and pages, updated as often as stock changes |

## Handoffs to related skills
- Agent flows and protocols: `agent-readiness`
- Reviews and comparisons: `ai-citation-earning`
- Wrong prices in answers: `brand-accuracy-ai-answers`
- Product markup: the Technical SEO `structured-data` skill
- Filter URLs: the Technical SEO `faceted-navigation-parameters` skill

## Quality bar: what an excellent review includes
- Real shopping prompts tested across engines.
- Feed, page and markup facts consistent.
- Attributes enriched for the prompts shoppers use.
- Protocol options assessed through the merchant's platform.

## Common mistakes
- Feeds and pages showing different prices or stock.
- Generic titles without the attributes shoppers ask about.
- Prices loaded only by JavaScript.
- Unverified sustainability or performance claims.
- Building custom agent checkout before checking platform support.

## Questions to ask before you recommend changes
- Which categories matter most for revenue and margin?
- Who owns the feed, and how often does it update?
- Does the platform support UCP, ACP or other agent checkout?

## Self-check before you answer
- Did I test real shopping prompts across engines?
- Are feed, page and markup facts consistent?
- Are protocol details labelled with source and status?
- Is measurement set by product group?

## Official documentation
- Google: generative AI features in Search, site owner guide (ecommerce details): https://developers.google.com/search/docs/fundamentals/ai-optimization-guide
- Share product data with Google: https://developers.google.com/search/docs/specialty/ecommerce/share-your-product-data-with-google
- Merchant listing structured data: https://developers.google.com/search/docs/appearance/structured-data/merchant-listing
- Universal Commerce Protocol: https://ucp.dev/
- Google Merchant Center: https://merchants.google.com/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/aeo-geo/ai-commerce-product-visibility/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
