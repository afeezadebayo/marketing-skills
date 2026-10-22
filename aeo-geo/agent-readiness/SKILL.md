---
name: agent-readiness
description: "Prepare a site for AI agents that browse and act for people: audit key tasks with real browser agents, fix the accessibility tree, labels, semantic HTML and flows agents rely on, keep prices and policies machine-clear, tune bot protection for user-directed agents, and assess agent commerce protocols such as Google's Universal Commerce Protocol, OpenAI and Stripe's Agentic Commerce Protocol and MCP. Use whenever someone mentions AI agents, agentic browsing, ChatGPT agent, browser agents, agent-friendly websites, agentic commerce, UCP, ACP, MCP for websites, or whether assistants can complete tasks on their site."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/aeo-geo/agent-readiness/
  category: marketing
  subcategory: aeo-geo
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Agent Readiness for AI Browsers and Assistants

AI agents don't just read pages; they act on them. Browser agents from OpenAI, Google, Anthropic, Perplexity and others can open a site, compare plans, fill in a form, book a demo or start a checkout for a person. Google describes how such agents work: they may analyse screenshots, inspect the DOM and interpret the accessibility tree. [Confirmed, Google Search Central] A site that confuses a screen reader usually confuses an agent too.

This skill audits whether agents can understand and complete the key tasks on a site, and prepares for the protocols that let agents transact directly.

## How agents meet your site
| Layer | What the agent uses | What helps |
|---|---|---|
| Visual | Screenshots of the rendered page | Clear layout, visible labels, no overlapping pop-ups |
| Structure | DOM and accessibility tree | Semantic HTML, labelled controls, logical headings, ARIA used correctly |
| Data | Text, tables, structured data, feeds | Facts in text, consistent prices, product and organisation data |
| Actions | Links, buttons, forms, checkout | Predictable flows, clear errors, no traps |
| Protocols | APIs and standards such as UCP, ACP and MCP | Machine interfaces for search, cart and checkout |

## Operating principles
1. **Accessibility is agent readiness.** Labelled inputs, real buttons and logical focus order serve people and agents.
2. **Tasks, not pages.** Audit the jobs that matter: compare plans, check availability, book, buy, contact, cancel.
3. **Facts in text.** Prices, specs, policies and availability belong in HTML text, not only in images or scripts.
4. **Friction where it protects, not everywhere.** Keep fraud controls, but avoid blanket challenges that stop legitimate, user-directed agents from browsing public pages.
5. **Watch the standards.** Agent protocols are young; adopt through your platform where possible rather than custom builds.

## When to use, and when not to
Use it for e-commerce, SaaS sign-up and pricing flows, booking and lead-generation sites, and any business where an assistant could complete the task for a buyer.

Don't use it for crawler policy (`ai-crawler-access`) or product feeds and AI shopping surfaces (`ai-commerce-product-visibility`), though they overlap.

## Inputs to ask for, in one message
1. The five to ten most valuable tasks on the site.
2. Key templates: pricing, product, booking, forms, checkout, account.
3. The platform (Shopify, WooCommerce, custom) and any bot protection.
4. Accessibility audits or known issues.
5. Whether you sell through feeds, marketplaces or agent checkout already.

## Workflow

### Step 1. List the tasks
For each, define start page, steps, success state and what an agent needs to know (price, availability, terms).

### Step 2. Run an accessibility pass
Check headings, landmarks, labels, button semantics, focus order, contrast and error messages with automated tools and a screen reader. Fix issues on task paths first.

### Step 3. Test with agents
Give one or two browser agents each task in plain words ("find the cheapest plan with SSO and start a trial"). Record where they fail: hidden prices, unlabeled fields, modal traps, ambiguous buttons, CAPTCHAs.

### Step 4. Make facts machine-clear
Put plan names, prices, limits and policies in consistent HTML text and tables; mirror them in structured data where it applies; keep them identical across pages and feeds.

### Step 5. Simplify flows
Fewer steps, clear labels ("Start free trial", not "Go"), inline errors, no forced account creation before showing prices, cookie banners that don't cover controls.

### Step 6. Review bot protection
Tune rules so public browsing by user-directed agents works while abusive automation is still blocked; protect sensitive actions with confirmation rather than blanket blocks.

### Step 7. Assess protocols
| Protocol | What it is | Status |
|---|---|---|
| Universal Commerce Protocol (UCP) | Open standard for agent commerce from discovery to checkout and post-purchase, announced by Google with Shopify, Etsy, Wayfair, Target, Walmart and others on 11 January 2026; REST, A2A and MCP bindings; merchants stay merchant of record | Live in Google's AI Mode and Gemini for eligible US merchants; expanding [Confirmed, Google] |
| Agentic Commerce Protocol (ACP) | OpenAI and Stripe standard powering checkout in ChatGPT, launched September 2025 | Live for participating merchants [Confirmed, OpenAI/Stripe] |
| Model Context Protocol (MCP) | Open protocol for connecting AI applications to tools and data | Widely adopted for tools; useful for exposing product, booking or support functions |

For most merchants, the practical route is through their commerce platform's integrations.

## Agent readiness checklist
- [ ] Key facts (price, plans, availability, policies) in HTML text
- [ ] Forms have visible labels and clear errors
- [ ] Buttons and links are real elements with descriptive text
- [ ] No pop-ups that block content without a clear close control
- [ ] Task flows work without forced sign-in before key information
- [ ] Bot rules allow public browsing by legitimate agents
- [ ] Structured data and feeds match the page
- [ ] Platform agent-commerce options reviewed (UCP, ACP)

## Worked example
A software company asked two browser agents to "find a plan with SSO for 50 users and book a demo". Both failed: plan limits were in images, the SSO add-on price appeared only in a tooltip, and the demo form's company-size field was an unlabeled custom dropdown. The team moved plan details into an HTML table, added the add-on price to the table, rebuilt the dropdown as a native select with a label and removed a newsletter pop-up on the pricing page. Both agents then completed the task; human conversion on the pricing page rose slightly as well.

## Output format
```
# Agent readiness review: <site>, <date>
## Tasks tested (agent, result, failure point)
## Accessibility findings on task paths
## Fact clarity issues (where facts are hidden or inconsistent)
## Flow and bot-protection changes
## Protocol assessment (UCP, ACP, MCP: relevant or not, route)
## Prioritised fixes with owners
```

## Task test script
Give each agent the same plain request and record the result:
```
Task: [plain request, e.g. find the cheapest plan with SSO for 50 users and start a trial]
Start URL: [homepage]
Agent: [name, version, date]
Result: completed / failed / partial
Steps taken: [list]
Failure point: [page, element, reason]
Time taken: [minutes]
```

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Checkout requires human verification (3-D Secure, ID checks) | Keep it; agents should hand control back to the person |
| Prices depend on location or login | Show a clear default price and explain how it changes |
| Marketplace or reseller channels | Make sure product facts match across channels agents may use |
| Accessibility fixes conflict with design | Accessible patterns win on task paths; designers can style them |
| Agents abuse forms (spam) | Use rate limits and server-side validation rather than blocking all automation |

## Handoffs to related skills
- Product data and checkout protocols: `ai-commerce-product-visibility`
- Bot rules: `ai-crawler-access`
- Server-rendered facts: the Technical SEO `javascript-seo` skill
- Speed: the Technical SEO `core-web-vitals` skill
- Clear fact pages: `answer-ready-content`

## Quality bar: what an excellent review includes
- Real tasks tested with real agents, with failure points recorded.
- Accessibility fixes prioritised on task paths.
- Protocol claims labelled with status and source.
- Fixes that help people as much as agents.

## Common mistakes
- Treating agents as a future problem while customers already use them.
- Prices in images or behind interactions.
- Custom controls without labels or keyboard support.
- Blanket bot blocking that also stops user-directed agents.
- Building custom agent integrations the platform already provides.

## Questions to ask before you recommend changes
- Which tasks would a buyer delegate to an assistant?
- What does the platform already support for agent commerce?
- Where must friction stay for fraud or compliance?

## Self-check before you answer
- Did I test real tasks with real agents?
- Are accessibility fixes prioritised on task paths?
- Are protocol claims labelled with status and source?
- Do fixes help humans as much as agents?

## Official documentation
- Google: generative AI features in Search, site owner guide (agentic experiences): https://developers.google.com/search/docs/fundamentals/ai-optimization-guide
- Agent-friendly website best practices (web.dev): https://web.dev/articles/ai-agent-site-ux
- Universal Commerce Protocol: https://ucp.dev/
- Model Context Protocol: https://modelcontextprotocol.io/
- WCAG 2.2: https://www.w3.org/TR/WCAG22/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/aeo-geo/agent-readiness/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
