---
name: audience-first-party-data
description: "Build first-party audiences for Google, Meta, TikTok, LinkedIn and Microsoft: legal basis and consent checks, customer and lead segments, Customer Match and Custom Audiences with automated syncs, existing-customer exclusions and new-customer goals, value-based lookalikes and audience signals, match rate improvements and data governance. Use whenever someone asks about customer match, custom audiences, lookalike audiences, excluding existing customers, first-party data for ads, audience signals for PMax or Advantage+, or ABM account lists."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/audience-first-party-data/
  category: marketing
  subcategory: performance-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Audiences and First-Party Data for Paid Media

As platforms automate targeting, the most valuable audience inputs are the ones only you have: your customers, your leads, their value and their behaviour. Customer lists tell platforms who to exclude, who to find more of and who is worth more. Used well, first-party data improves acquisition efficiency and stops you paying to reach people who already buy. Used carelessly, it breaks privacy rules and trust.

This skill builds a first-party audience strategy for Google, Meta, TikTok, LinkedIn and Microsoft: consented data collection, customer match and custom audiences, exclusions, lookalikes and value-based seeds, audience signals for automated campaigns and governance.

## Operating principles
1. **Consent and transparency first.** Use customer data for advertising only where your privacy notice and legal basis allow it.
2. **Exclude before you include.** Stopping spend on existing customers (for acquisition goals) is often the fastest win.
3. **Seed with value.** Lookalikes and signals built from high-value customers beat lists of everyone.
4. **Keep lists fresh.** Automate syncs from your CRM or commerce platform.
5. **Audiences are signals, not walls.** In automated campaigns, lists guide the system; creative and goals still decide delivery.

## Audience types and uses
| Audience | Source | Use |
|---|---|---|
| All customers | CRM or commerce platform | Exclude from acquisition; separate reporting |
| High-value customers | Top spend or LTV segment | Lookalike and signal seeds; value-based bidding inputs |
| Recent purchasers | Last 30 to 90 days | Exclude from promotions; cross-sell where relevant |
| Lapsed customers | No purchase in the normal cycle | Win-back campaigns (where consent and law allow) |
| Leads and pipeline stages | CRM | Exclude closed customers; target open opportunities in B2B |
| Site and app visitors | Pixels and SDKs | Retargeting (test incrementality) |
| Engaged video viewers | Platform data | Mid-funnel sequencing |
| Target accounts (B2B) | ABM lists | LinkedIn and Google account targeting |

## When to use, and when not to
Use it when campaigns spend on existing customers, when lookalikes underperform, when setting up customer match for the first time, before Black Friday or peak, and when moving to new-customer goals.

Don't use it to fix conversion tracking (`conversion-tracking-capi`) or lifecycle messaging (the CRM and Lifecycle skills).

## Inputs to ask for, in one message
1. CRM or commerce platform and customer data fields available (email, phone, value, dates).
2. Privacy notice and consent records for advertising use.
3. Current audiences in each platform and how they are refreshed.
4. Campaign goals: new customers, revenue, leads, retention.
5. Customer value data (LTV, order history) for value-based seeds.

## Workflow

### Step 1. Check legal basis
Confirm the privacy notice covers advertising use and that consent where required is recorded. Exclude people who opted out.

### Step 2. Build core segments
All customers, high-value customers, recent buyers, lapsed customers, leads by stage.

### Step 3. Upload and sync
Customer Match (Google), Custom Audiences (Meta), TikTok and LinkedIn matched audiences; hashed identifiers; automated daily or weekly syncs through native integrations or a CDP.

### Step 4. Apply exclusions
Exclude existing customers from acquisition campaigns or use new-customer goals and budget caps; exclude recent purchasers from discount campaigns.

### Step 5. Build lookalikes and signals
Seed lookalikes and audience signals with high-value customers; test seed size and value weighting.

### Step 6. Pass values
Value-based lookalikes where platforms support them; value rules or new-customer values in bidding.

### Step 7. Measure
New-customer share, CAC from your own data, match rates and audience sizes.

### Step 8. Govern
Document sources, refresh schedules, owners and retention; remove data on request.

## Match rate tips
- Upload email and phone (E.164 format) together where consented.
- Normalise data (lowercase emails, trimmed spaces) before hashing or let the platform hash.
- Include first name, last name, country and postcode where platforms accept them.
- Expect lower match rates for B2B work emails on consumer platforms.

## Seed quality experiment
| Seed | Size | Expectation |
|---|---|---|
| All customers | Large | Broad reach, average quality |
| Repeat customers | Medium | Better quality |
| Top 20% by 12-month value | Smaller | Highest quality, may limit scale |
| High-value with value weighting (where supported) | Varies | Balances scale and quality |
Test two or three seeds in parallel and judge on new-customer CAC and 90-day value, not just first-order CPA.

## Sync options
| Method | Pros | Cons |
|---|---|---|
| Native platform integrations (Shopify, HubSpot, Klaviyo) | Easy, automatic | Limited segment logic |
| CDP (Segment, RudderStack, Hightouch) | One definition across platforms | Cost and setup |
| Manual CSV uploads | No tools needed | Goes stale; error-prone |
Aim for daily syncs for customer exclusions; weekly is acceptable for lookalike seeds.

## Peak season preparation
- Refresh all customer lists two weeks before peak.
- Create a recent-purchasers exclusion for discount campaigns.
- Build lapsed-customer audiences for win-back offers (where lawful).
- Check match rates and audience sizes meet platform minimums.
- Agree new versus returning customer goals for the peak period.

## Governance checklist
- Source system and definition for each audience.
- Refresh schedule and owner.
- Consent basis and exclusions for opt-outs.
- Retention period and deletion process.
- Record of which platforms receive which data.

## Exclusion setup by platform
| Platform | How to exclude or cap existing customers |
|---|---|
| Google Ads (PMax, Search) | Customer Match lists with new-customer acquisition goal, or audience exclusions where supported |
| Meta (Advantage+) | Existing customer definitions and budget cap for existing customers |
| TikTok | Custom audience exclusions in ad groups |
| LinkedIn | Matched audience exclusions for customers and employees |
Check each platform's current settings; options change frequently.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Small customer list | Seed with broader valuable groups (repeat buyers) and accept lower precision |
| Strict consent market | Use only consented records; rely more on contextual and broad targeting |
| B2B on consumer platforms | Use LinkedIn for account targeting; consumer platforms for retargeting |
| Existing customers drive most conversions | Separate goals and reporting; test whether those ads are incremental |
| Data in many systems | Use a CDP or warehouse sync to keep one definition per audience |

## Handoffs to related skills
- Tracking and values: `conversion-tracking-capi`
- PMax new-customer goals: `performance-max-shopping`
- Meta Advantage+ customer settings: `meta-ads`
- LinkedIn account targeting: `paid-social-tiktok-linkedin`
- Data hygiene and consent records: the CRM and Lifecycle `crm-data-hygiene` skill

## Worked example
A fashion retailer found that a large share of Meta and PMax conversions came from existing customers. Customer lists hadn't been refreshed in months, and lookalikes were seeded from all past buyers. A daily sync from the commerce platform fed fresh customer lists, existing customers were capped in Advantage+ and excluded from PMax acquisition goals, and lookalikes were reseeded from the top 20% by 12-month value. New-customer share rose and new-customer CAC fell, while a separate retention campaign served existing customers with appropriate offers.

## Output format
```
# First-party audience plan: <business>, <date>
## Legal basis and consent check
## Core segments (definition, size, refresh)
## Platform uploads and sync method
## Exclusions and new-customer settings
## Lookalikes and signals (seeds, value weighting)
## Measurement and governance
```

## Common mistakes
- Using customer data without a legal basis for advertising.
- Stale lists that never refresh.
- Seeding lookalikes from everyone instead of valuable customers.
- Paying acquisition prices for existing customers.
- Treating audience lists as hard targeting in automated campaigns.

## Questions to ask before you build
- Does your privacy notice cover advertising use of customer data?
- Which customers are most valuable, and can you identify them?
- Do campaigns need new customers or total revenue?

## Self-check before you answer
- Is the legal basis confirmed and opt-outs excluded?
- Are customer lists synced automatically and fresh?
- Are exclusions and new-customer goals set for acquisition?
- Are seeds value-based?

## Official documentation
- Google Customer Match: https://support.google.com/google-ads/answer/6379332
- Meta Business Help Centre (Custom Audiences): https://www.facebook.com/business/help
- LinkedIn Marketing Solutions help (Matched Audiences): https://www.linkedin.com/help/lms
- UK ICO guidance on direct marketing and advertising technologies: https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/performance-marketing/audience-first-party-data/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
