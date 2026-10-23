# Marketing Skills for AI Agents — the full SKILL.md library

[![172 skills](https://img.shields.io/badge/skills-172-0b7285)](#all-skills)
[![Format: Agent Skills](https://img.shields.io/badge/format-SKILL.md-5f3dc4)](https://agentskills.io/specification)
[![Works with Claude Code, Codex & Claude.ai](https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Codex%20%7C%20Claude.ai-1c7ed6)](#install)
[![Licence: CC BY 4.0](https://img.shields.io/badge/licence-CC%20BY%204.0-2b8a3e)](https://creativecommons.org/licenses/by/4.0/)

The complete library of free **marketing [Agent Skills](https://agentskills.io/specification)** (`SKILL.md`) for
**Claude, Claude Code, OpenAI Codex** and any agent that reads the standard. Each skill is one Markdown file that
gives your agent a senior practitioner's workflow — when to use it, the inputs to ask for, a numbered process,
decision rules, an output template and sources — loaded only when a task needs it.

By [**Afeez Adebayo**](https://afeezadebayo.com) · [Browse online](https://afeezadebayo.com/skills-md/marketing/) · [LinkedIn](https://www.linkedin.com/in/afeez-adebayo/) · [X](https://x.com/za_icon) · [Newsletter](https://afeezadebayo.com/newsletter/)

> **This repo is the hub monorepo** — all 172 skills live here, one folder per skill, grouped by category
> (`category/skill-name/SKILL.md`), matching the layout used by `anthropics/skills`.
> Each category is also mirrored as its own standalone repo below, for anyone who only wants one set.

## Skill categories

13 categories, 172 skills, each a self-contained `category/skill-name/SKILL.md` folder in this repo.

| Category | Skills | Folder | Standalone repo |
|---|---|---|---|
| Technical SEO | 16 | [`technical-seo/`](technical-seo) | [technical-seo-skills](https://github.com/afeezadebayo/technical-seo-skills) |
| Content & On-Page SEO | 13 | [`content-seo/`](content-seo) | [content-seo-skills](https://github.com/afeezadebayo/content-seo-skills) |
| AEO & GEO (AI Search) | 13 | [`aeo-geo/`](aeo-geo) | [aeo-geo-skills](https://github.com/afeezadebayo/aeo-geo-skills) |
| International SEO | 13 | [`international-seo/`](international-seo) | [international-seo-skills](https://github.com/afeezadebayo/international-seo-skills) |
| CRM & Lifecycle | 13 | [`crm-lifecycle/`](crm-lifecycle) | [crm-lifecycle-skills](https://github.com/afeezadebayo/crm-lifecycle-skills) |
| Performance Marketing | 13 | [`performance-marketing/`](performance-marketing) | [performance-marketing-skills](https://github.com/afeezadebayo/performance-marketing-skills) |
| Growth Marketing | 13 | [`growth-marketing/`](growth-marketing) | [growth-marketing-skills](https://github.com/afeezadebayo/growth-marketing-skills) |
| Product-Led Growth | 13 | [`product-led-growth/`](product-led-growth) | [product-led-growth-skills](https://github.com/afeezadebayo/product-led-growth-skills) |
| Conversion Rate Optimisation | 13 | [`conversion-rate-optimization/`](conversion-rate-optimization) | [conversion-rate-optimization-skills](https://github.com/afeezadebayo/conversion-rate-optimization-skills) |
| Product Marketing & GTM | 13 | [`product-marketing/`](product-marketing) | [product-marketing-skills](https://github.com/afeezadebayo/product-marketing-skills) |
| Content, Copy & PR | 13 | [`content-copy-pr/`](content-copy-pr) | [content-copy-pr-skills](https://github.com/afeezadebayo/content-copy-pr-skills) |
| Social Media | 13 | [`social-media/`](social-media) | [social-media-skills](https://github.com/afeezadebayo/social-media-skills) |
| GTM Engineering | 13 | [`gtm-engineering/`](gtm-engineering) | [gtm-engineering-skills](https://github.com/afeezadebayo/gtm-engineering-skills) |

Use this hub if you want everything in one clone, or install category repos individually if you only need one or two sets.

## Install

**Pick a format for your use:**

| You want to… | Use | How |
|---|---|---|
| Run skills in **Claude Code / Codex** | this hub, or one category repo | `git clone` it, copy a `category/skill-name` folder into `~/.claude/skills/` or `~/.agents/skills/` |
| Upload to **Claude.ai / Desktop** | a single skill folder | zip the `skill-name/` folder → **Settings → Capabilities → Skills → Upload** |
| **Bulk-load** a Project / custom GPT / knowledge base | several skill folders at once | upload the `SKILL.md` files directly, or browse bundles on the [library page](https://afeezadebayo.com/skills-md/marketing/) |
| Just **read / browse** | this repo | open any `category/skill-name/SKILL.md` below |

```bash
# Example: install the XML sitemaps skill in Claude Code
git clone https://github.com/afeezadebayo/marketing-skills.git
cp -r marketing-skills/technical-seo/xml-sitemaps ~/.claude/skills/

# Or from the standalone category repo
git clone https://github.com/afeezadebayo/technical-seo-skills.git
cp -r technical-seo-skills/xml-sitemaps ~/.claude/skills/
```

Then start a new session and ask your agent which skills it can use. Code execution must be enabled for skills in the Claude apps.

## How these skills work

Agents use **progressive disclosure**: they read each skill's `name` and `description` (~100 tokens) at the start of a
session, and load the full `SKILL.md` only when your request matches. Install the sets you use; a smaller, relevant set
helps the agent pick the right skill.

## All skills

### [technical-seo](technical-seo) — 16 skills
- technical-seo-audit: Technical SEO Audit
- crawlability-indexation-audit: Crawlability and Indexation Audit
- robots-directives: Robots.txt and Robots Directives
- xml-sitemaps: XML Sitemaps
- canonicalization: Canonicalization and Duplicate Content
- redirects-status-codes: Redirects and HTTP Status Codes
- site-migration: Site Migration SEO
- core-web-vitals: Core Web Vitals and Page Experience
- javascript-seo: JavaScript SEO and Rendering
- structured-data: Structured Data and Schema Markup
- internal-linking: Internal Linking and Site Architecture
- log-file-analysis: Log File Analysis for SEO
- faceted-navigation-parameters: Faceted Navigation and URL Parameters
- hreflang-implementation: hreflang Implementation and Debugging
- image-seo: Image SEO
- international-technical-seo: International Technical SEO

### [content-seo](content-seo) — 13 skills
- content-seo-audit: Content SEO Audit
- keyword-research: Keyword Research
- search-intent-serp-analysis: Search Intent and SERP Analysis
- topical-map: Topical Maps and Content Clusters
- content-brief: SEO Content Briefs
- seo-content-writing: SEO Content Writing
- title-tags-meta-descriptions: Title Tags and Meta Descriptions
- on-page-seo: On-Page SEO Optimisation
- eeat-content-quality: E-E-A-T and Content Quality
- content-refresh: Content Refresh and Decay Recovery
- keyword-cannibalisation: Keyword Cannibalisation
- content-pruning: Content Pruning and Consolidation
- internal-linking: Internal Linking for Content SEO

### [aeo-geo](aeo-geo) — 13 skills
- ai-search-visibility-audit: AI Search Visibility Audit
- ai-visibility-tracking: AI Visibility Tracking and Reporting
- query-fan-out-mapping: Query Fan-Out and Prompt Research
- answer-ready-content: Answer-Ready Content for AI Search
- ai-overviews-ai-mode: Google AI Overviews and AI Mode
- chatgpt-search-visibility: ChatGPT Search Visibility
- answer-engine-platforms: Perplexity, Copilot, Claude and Gemini Visibility
- entity-optimisation: Entity Optimisation for AI Search
- ai-citation-earning: Earning Citations and Mentions for AI Answers
- ai-crawler-access: AI Crawler Access and Technical Readiness
- brand-accuracy-ai-answers: Brand Accuracy in AI Answers
- agent-readiness: Agent Readiness for AI Browsers and Assistants
- ai-commerce-product-visibility: Product Visibility in AI Shopping and Commerce

### [international-seo](international-seo) — 13 skills
- international-seo-audit: International SEO Audit
- international-market-selection: International Market Selection and Prioritisation
- international-site-structure: International Site Structure: ccTLDs, Subfolders and Subdomains
- hreflang-implementation: hreflang Implementation and Debugging
- localisation-translation: Localisation and Translation Workflows for SEO
- multilingual-keyword-research: Multilingual Keyword Research
- geo-language-targeting: Country and Language Targeting Signals
- international-technical-seo: International Technical SEO
- local-search-engines: Local Search Engines: Baidu, Yandex, Naver and Seznam
- international-content-strategy: International Content Strategy
- international-link-building: International Link Building and Digital PR
- international-expansion-migration: International Expansion and Site Migrations
- international-seo-reporting: International SEO Reporting by Market

### [crm-lifecycle](crm-lifecycle) — 13 skills
- lifecycle-marketing-audit: Lifecycle Marketing Audit
- customer-journey-mapping: Customer Journey Mapping for Lifecycle
- lifecycle-segmentation: Lifecycle Segmentation and Engagement Tiers
- crm-data-hygiene: CRM Data Hygiene and Enrichment
- lead-scoring-routing: Lead Scoring and Routing
- onboarding-activation: Onboarding and Activation Sequences
- retention-churn-prevention: Retention and Churn Prevention
- win-back-reactivation: Win-Back and Reactivation Campaigns
- email-deliverability: Email Deliverability and Inbox Placement
- lifecycle-email-copy-design: Lifecycle Email Copy and Design
- sms-whatsapp-lifecycle: SMS and WhatsApp Lifecycle Messaging
- lifecycle-experimentation: Lifecycle Experimentation and Holdout Testing
- lifecycle-reporting-attribution: Lifecycle Reporting and Attribution

### [performance-marketing](performance-marketing) — 13 skills
- paid-media-audit: Paid Media Audit
- media-planning-budgeting: Media Planning and Budget Allocation
- conversion-tracking-capi: Conversion Tracking, Consent Mode and Conversions API
- incrementality-testing: Incrementality Testing: Lift and Geo Experiments
- marketing-mix-modelling: Marketing Mix Modelling
- google-search-ads: Google Search Ads and AI Max
- performance-max-shopping: Performance Max and Shopping
- meta-ads: Meta Ads (Facebook and Instagram)
- paid-social-tiktok-linkedin: TikTok, LinkedIn and Other Paid Social
- ad-creative-testing: Ad Creative Strategy and Testing
- landing-page-cro: Landing Pages and Conversion Rate Optimisation for Paid Traffic
- audience-first-party-data: Audiences and First-Party Data for Paid Media
- paid-media-reporting: Paid Media Reporting and Attribution

### [growth-marketing](growth-marketing) — 13 skills
- growth-audit: Growth Audit
- north-star-metric-tree: North Star Metric and Metric Tree
- growth-model: Growth Model and Forecasting
- growth-experiment-backlog: Growth Experiment Backlog and Cadence
- experiment-design: Experiment Design for Growth
- experiment-readout: Experiment Readouts and Analysis
- acquisition-channel-testing: Acquisition Channel Testing
- growth-loops: Growth Loops
- referral-programmes: Referral Programmes
- funnel-analysis: Funnel Analysis
- cohort-retention-analysis: Cohort Retention Analysis
- tracking-plan: Tracking Plan and Event Taxonomy
- growth-reporting: Growth Reporting and Attribution

### [product-led-growth](product-led-growth) — 13 skills
- plg-audit: Product-Led Growth Audit
- plg-strategy: Product-Led Growth Strategy
- free-model-design: Free Model Design: Freemium, Free Trials and Reverse Trials
- in-product-onboarding: In-Product Onboarding
- feature-adoption: Feature Adoption
- product-qualified-leads: Product-Qualified Leads
- product-led-sales: Product-Led Sales
- in-app-upgrade-prompts: In-App Upgrade Prompts and Paywalls
- team-expansion-invites: Team Expansion and Invites
- in-app-messaging: In-App Messaging
- templates-integrations-growth: Templates, Integrations and Marketplace Growth
- product-education: Product Education and Academy
- plg-metrics: PLG Metrics and Reporting

### [conversion-rate-optimization](conversion-rate-optimization) — 13 skills
- cro-audit: CRO Audit
- conversion-research: Conversion Research Methods
- landing-page-optimisation: Landing Page and Homepage Optimisation
- form-optimisation: Form Optimisation
- pricing-page-optimisation: Pricing Page Optimisation
- checkout-optimisation: Checkout and Cart Optimisation
- signup-flow-optimisation: Sign-Up Flow and Onboarding Conversion
- popups-onsite-messaging: Popups and On-Site Messaging
- social-proof-trust: Social Proof and Trust Signals
- conversion-copywriting: Conversion Copywriting and Value Proposition Tests
- mobile-conversion: Mobile Conversion Optimisation
- cro-test-planning: CRO Test Planning and Prioritisation
- cro-reporting: CRO Programme Reporting

### [product-marketing](product-marketing) — 13 skills
- product-marketing-audit: Product Marketing Audit
- positioning: Positioning
- messaging-framework: Messaging Framework
- ideal-customer-profile: Ideal Customer Profile and Personas
- customer-research-interviews: Customer Research and Jobs-to-Be-Done Interviews
- competitive-intelligence: Competitive Intelligence and Battlecards
- win-loss-analysis: Win-Loss Analysis
- go-to-market-plan: Go-to-Market Plan
- product-launch: Product Launches
- pricing-packaging: Pricing and Packaging
- sales-enablement: Sales Enablement
- case-studies-customer-proof: Case Studies and Customer Proof
- partner-marketing: Partner Marketing and Co-Marketing

### [content-copy-pr](content-copy-pr) — 13 skills
- content-marketing-audit: Content Marketing Audit
- content-strategy: Content Strategy
- editorial-operations: Editorial Operations and Content Calendar
- brand-voice-guide: Brand Voice and Style Guide
- marketing-copywriting: Marketing Copywriting
- editing-proofreading: Editing and Proofreading
- ai-writing-cleanup: AI Writing Cleanup: Removing AI-Sounding Phrasing
- newsletter-strategy: Newsletter Strategy
- thought-leadership: Thought Leadership
- original-research-reports: Original Research Reports
- digital-pr: Digital PR and Media Relations
- content-repurposing: Content Repurposing and Distribution
- content-pr-measurement: Content and PR Measurement

### [social-media](social-media) — 13 skills
- social-media-audit: Social Media Audit
- social-media-strategy: Social Media Strategy
- linkedin-organic: LinkedIn Organic Growth
- x-twitter-organic: X (Twitter) Organic Growth
- instagram-organic: Instagram Organic Growth
- tiktok-organic: TikTok Organic Growth
- short-video-scripts: Short Video Scripts
- youtube-seo-growth: YouTube SEO and Channel Growth
- social-content-calendar: Social Media Content Calendar
- community-building: Community Building and Management
- social-listening: Social Listening and Reputation Monitoring
- creator-employee-advocacy: Creator Partnerships and Employee Advocacy
- social-media-reporting: Social Media Reporting

### [gtm-engineering](gtm-engineering) — 13 skills
- gtm-engineering-audit: GTM Engineering Audit
- clay-table-design: Clay Table Design
- enrichment-waterfalls: Enrichment Waterfalls
- icp-account-scoring: ICP and Account Scoring
- signal-based-outbound: Signal-Based Outbound
- ai-copy-columns: AI Copy Columns
- data-deduplication-normalisation: Data Deduplication and Normalisation
- crm-sync-routing: CRM Sync and Routing
- outbound-infrastructure: Outbound Infrastructure and Deliverability
- gtm-workflow-qa: GTM Workflow QA
- gtm-cost-control: GTM Cost Control
- gtm-workflow-documentation: GTM Workflow Documentation
- gtm-reporting: GTM Reporting

## Adapt them

Fork or copy any skill. Keep the `name`, add your own tools, thresholds and house style to the `description`, and keep
the credit line. If you publish an adapted version, link back to the source so readers find updates.

## Licence

Released under [**CC BY 4.0**](https://creativecommons.org/licenses/by/4.0/). Use, share and adapt — including
commercially — with credit to Afeez Adebayo and a link to the source page in each file.

<sub>Keywords: marketing SKILL.md, Agent Skills, Claude skills, Claude Code skills, Codex skills, AI agent skills,
SEO skills, AEO GEO skills, lifecycle marketing, performance marketing, growth marketing, product-led growth, CRO,
product marketing, content marketing, social media, GTM engineering — free and open under CC BY 4.0.</sub>
