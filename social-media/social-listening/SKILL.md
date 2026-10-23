---
name: social-listening
description: "Set up social listening that leads to action: goals for care, product insight, competitors, category trends, content ideas, advocates and risk, precise queries with exclusions, sources from social and Reddit to reviews, news and AI answers, alerts and crisis signals, human theme analysis, routing to owners and reporting on share of voice and sentiment. Use whenever someone asks about social listening, brand monitoring, tracking mentions, online reputation, sentiment analysis, competitor monitoring on social, spotting a social media crisis or finding content ideas from conversations."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/social-media/social-listening/
  category: marketing
  subcategory: social-media
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Social Listening and Reputation Monitoring

Most conversations about a brand happen away from its own profiles: in replies to other people, forums, review sites, Reddit threads, TikTok comments, news articles and private groups that surface publicly. Social listening tracks those conversations to spot complaints early, find content ideas, understand sentiment, learn what customers say about competitors, discover advocates and creators and detect crises before they grow. Monitoring that only counts mentions misses the point; listening means turning what people say into action.

This skill sets up social listening: goals, queries, sources, alerts, sentiment and theme analysis, competitor and category tracking, crisis signals, routing to the right teams and reporting.

## Operating principles
1. **Listen with a purpose.** Each query should serve a goal: care, product insight, content, competitors or risk.
2. **Good queries beat big tools.** Precise keywords, exclusions and languages decide data quality.
3. **Read, don't just count.** Sentiment scores are rough; real insight comes from reading samples.
4. **Route insights to owners.** Support, product, sales, PR and content each get what they can act on.
5. **Respect privacy and platform rules.** Use public data and approved tools; don't track individuals inappropriately.

## Listening goals and queries
| Goal | What to track | Example query terms |
|---|---|---|
| Customer care | Brand mentions with problems | brand name + "not working", "refund", "cancel" |
| Product insight | Feature requests, complaints, praise | brand + "wish", "would love", "missing" |
| Competitors | Competitor mentions and switching talk | competitor names + "alternative", "switching from" |
| Category trends | Topics and questions in your space | category terms, problem phrases |
| Content ideas | Questions people ask | "how do I" + topic |
| Creators and advocates | People recommending you | brand + "recommend", "love" |
| Risk and crisis | Spikes, negative themes, influential critics | brand + "scam", "lawsuit", "boycott", sudden volume changes |

## Sources
| Source | Notes |
|---|---|
| X, Instagram, TikTok, Facebook, LinkedIn, YouTube | Coverage varies by tool and platform access |
| Reddit and forums | Rich, candid discussions |
| Review sites (G2, Trustpilot, app stores, Google reviews) | Product and service feedback |
| News and blogs | Coverage and reputation |
| Podcasts and video transcripts | Growing source where tools support it |
| AI answer engines | Check how assistants describe your brand (see AEO & GEO skills) |

## When to use, and when not to
Use it to catch complaints and crises early, inform content and product decisions, track competitors, measure share of voice and find advocates.

Don't use it to monitor private individuals inappropriately, or as a replacement for direct customer research (the Product Marketing `customer-research-interviews` skill).

## Inputs to ask for, in one message
1. Goals for listening.
2. Brand names, product names, common misspellings, handles and executives.
3. Competitors and category terms.
4. Languages and markets.
5. Tools available (social listening platforms, native alerts, review monitoring).
6. Teams that will act on insights.

## Workflow

### Step 1. Set goals
One to three primary uses at first.

### Step 2. Build queries
Brand terms, misspellings, product names, competitor and category terms; exclusions to remove noise (for example common words that share the brand name).

### Step 3. Choose sources and tools
Match to where the audience talks; check platform coverage limits.

### Step 4. Set alerts
Volume spikes, negative keywords, influential accounts and crisis terms, routed to owners.

### Step 5. Review regularly
Daily for care and risk; weekly for themes and content ideas; monthly for trends and competitors.

### Step 6. Analyse themes
Read samples, tag themes, track sentiment trends with human checks.

### Step 7. Route and act
Support handles complaints; product gets feature themes; content gets questions; PR gets reputation issues; sales gets switching signals.

### Step 8. Report
Share of voice, sentiment trends, top themes, actions taken and outcomes.

## Crisis signals
- Sudden spike in mentions or negative sentiment.
- Influential accounts or journalists posting critically.
- The same complaint repeated by many people.
- Mentions of safety, legal or ethical issues.
- Hashtags or campaigns targeting the brand.
Agree escalation thresholds and owners in advance.

## Query example
```
("Acme Meals" OR "AcmeMeals" OR "acme meal kit" OR @acmemeals)
AND NOT ("acme corporation" OR "acme anvil")
Languages: English
Markets: UK, Ireland
```
Test queries on a sample of results and refine exclusions until most matches are relevant.

## Weekly listening report
| Section | Content |
|---|---|
| Volume and sentiment trend | Mentions this week versus last, with notable spikes |
| Top themes | Three to five themes with example posts |
| Care issues | Complaints found and resolved |
| Product and content insights | Requests, questions and ideas routed |
| Competitors | Share of voice and notable conversations |
| Risks | Anything to watch or escalate |

## Share of voice
Share of voice compares your mentions with competitors' in the same sources and period. Track it alongside sentiment, because a spike in negative mentions also raises share of voice.

## Finding advocates and creators
Filter mentions for positive recommendations and for people with engaged audiences in your niche. Thank them, invite them into the community or advocacy programmes and consider creator partnerships.

## Tool selection
Compare platform coverage, languages, historical data, alerting, sentiment accuracy, integration with support tools and price. Many teams combine a listening platform with native platform search, review alerts and manual checks of key communities.

## Crisis response steps
1. Confirm the facts internally before responding.
2. Pause scheduled posts that could seem insensitive.
3. Acknowledge publicly with what you know and what you're doing.
4. Route individual cases to support privately.
5. Update regularly until resolved, then review what happened.

Refine queries monthly as products, competitors and slang change.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Brand name is a common word | Use exclusions and combine with product or category terms |
| Small brand with few mentions | Focus on category and competitor listening |
| Several languages | Native speakers review samples; tools may misread sentiment |
| Sarcasm and slang | Human review; don't trust automated sentiment alone |
| Limited budget | Native alerts, Google Alerts, review site notifications and manual Reddit searches |

## Handoffs to related skills
- Community responses: `community-building`
- Reporting: `social-media-reporting`
- Creators and advocates: `creator-employee-advocacy`
- Competitive intelligence: the Product Marketing `competitive-intelligence` skill
- PR and reputation: the Content, Copy and PR `digital-pr` skill
- Brand accuracy in AI answers: the AEO & GEO `brand-accuracy-ai-answers` skill

## Worked example
A meal-kit company only watched its own comments. Listening queries for the brand, misspellings and "meal kit" plus complaint terms revealed a growing Reddit thread about late deliveries in one region, many TikTok videos praising a specific recipe and frequent comparisons with a competitor on price. Support contacted affected customers and logistics fixed a courier issue; content created a series around the popular recipe; product marketing updated pricing comparisons. Negative mentions about delivery fell, and the recipe series became a top performer.

## Output format
```
# Social listening plan: <brand>, <date>
## Goals
## Queries and exclusions
## Sources and tools
## Alerts and escalation
## Review cadence and owners
## Reporting template
```

## Common mistakes
- Counting mentions without reading them.
- Noisy queries full of irrelevant results.
- Trusting automated sentiment blindly.
- Insights that never reach product, support or content.
- No crisis thresholds.

## Questions to ask before you listen
- What decisions will listening inform?
- Which terms, misspellings and competitors matter?
- Who acts on each type of insight?

## Self-check before you answer
- Do queries serve clear goals with exclusions?
- Are alerts and escalation defined?
- Are themes read by humans, not just scored?
- Are insights routed to owners and acted on?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/social-media/social-listening/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
