---
name: signal-based-outbound
description: "Run outbound on buying signals: signals chosen from past wins, precise definitions and sources, strength and freshness decay, a play library matching signals to people, angles and calls to action, detection workflows, relevant non-creepy openers, routing within 48 hours and measurement by signal. Use whenever someone wants trigger-based or signal-based outbound, intent data plays, to reach accounts after funding, hiring or leadership changes, to follow champions to new companies or to decide which signals are worth tracking in Clay."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/signal-based-outbound/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-13"
---

# Signal-Based Outbound

Cold outreach to a static list ignores timing. The same message lands very differently on a company that just raised funding, hired a new head of growth, launched in a new market or started using a competitor's tool. Signal-based outbound watches for these events and reaches the right people soon after, with a message that refers to the event and why it matters. Done badly, it becomes creepy ("I saw you visited our pricing page three times"), spammy (every job post triggers a sequence) or stale (signals acted on weeks too late).

This skill designs signal-based outbound: choosing signals that predict buying, sourcing and detecting them, scoring strength and freshness, matching signals to plays and messages, timing and routing, writing relevant openers, avoiding over-reach, and measuring which signals produce meetings and revenue.

## Operating principles
1. **Signals must predict buying.** Use events that preceded past deals, not everything that can be tracked.
2. **Fresh beats many.** Act within days, not weeks; signals expire.
3. **Relevance, not surveillance.** Refer to public, professional events; never make people feel watched.
4. **One signal, one play.** Each signal has a matching message, audience and action.
5. **Measure by signal.** Keep the ones that produce meetings; drop the rest.

## Signal types
| Type | Examples | Source |
|---|---|---|
| Hiring | Job posts for roles your product supports | Job boards, careers pages |
| People moves | New leader in a buying role, a champion changes company | LinkedIn and people data |
| Funding and finance | New funding round, acquisition, IPO filing | News, funding databases |
| Expansion | New market, new office, new product line | News, press releases, websites |
| Technology | Adopted or dropped a tool, competitor tech detected | Technographic providers |
| Engagement (first party) | Pricing page visits, trial sign-ups, webinar attendance | Website analytics, product data |
| Content and social | Leader posts about a problem you solve | LinkedIn, podcasts |
| Compliance or events | New regulation affecting their sector | Regulators, industry news |

## When to use, and when not to
Use it to prioritise outbound, build trigger-based workflows, time outreach to existing target accounts, re-engage closed-lost deals and follow champions to new companies.

Don't use it for broad awareness campaigns or to justify contacting people outside your ICP just because a signal fired.

## Inputs
- ICP and scoring model.
- Past won deals and the events that preceded them.
- Available data sources and tools.
- Sales capacity and channels (email, LinkedIn, phone).
- Privacy and compliance rules for first-party data.

## Workflow

### Step 1. Find predictive signals
Review the 30 to 50 most recent wins: what happened at the account in the 90 days before first contact? Rank signals by how often they appear and how strongly they relate to deal size.

### Step 2. Define each signal precisely
What counts, how it is detected, which fields prove it, how long it stays valid.

### Step 3. Score strength and freshness
Points for strength; decay over time (for example full points for 14 days, half to 45 days, none after 90).

### Step 4. Design plays
For each signal: who to contact, the angle, the channel, the timing and the call to action.

### Step 5. Build detection workflows
Scheduled or triggered tables that check sources, deduplicate events, enrich contacts and score.

### Step 6. Write signal-aware openers
Reference the event plainly and connect it to a problem you solve; see `ai-copy-columns`.

### Step 7. Route and time
Tier A signals to reps within 48 hours; others to automated sequences or nurture.

### Step 8. Measure and prune
Track positive reply rate, meetings and pipeline by signal; keep the top performers.

## Play library
| Signal | Who | Angle | Call to action |
|---|---|---|---|
| Hiring a head of growth | New leader, CEO | Teams building growth functions often first need X | Share a 30-day plan template |
| Raised Series A or B | CEO, COO, finance lead | Scaling after funding usually strains Y | Short call on how peers handled it |
| Champion moved company | The champion | Bring a proven result to the new team | Catch-up call |
| Launched in a new country | Country lead, ops | Local payments, compliance or hiring needs | Relevant case study |
| Competitor tool dropped | Tool owner | What they likely need next | Comparison guide |
| Pricing page visits (first party) | Account owner | Offer help, not surveillance | Answer questions or book a demo |

## Opener examples
| Weak | Better |
|---|---|
| "Congrats on the funding!" | "After a Series A, finance teams usually rebuild month-end; we help payments companies close in two days." |
| "I saw you visited our pricing page." | "If you're comparing options for X, here's a short guide on what to check." |
| "Noticed you're hiring!" | "You're hiring three SDRs; ramp time is usually where pipeline slips, and that's what we fix." |

## Freshness and decay
```
Days since signal | Strength multiplier
0 to 14           | 1.0
15 to 45          | 0.5
46 to 90          | 0.2
90+               | 0 (expired)
```

## Multi-channel timing
For tier A signals, combine channels over a short window: a relevant email within 48 hours, a LinkedIn connection or comment within the same week and, for the best-fit accounts, a call from the account owner. Space touches over two to three weeks and stop as soon as someone replies or opts out.

Log every signal, play and outcome in the CRM so future win analysis can update which signals matter.

Review the play library every quarter, retiring plays that no longer produce meetings and adding new ones from recent wins.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Too many signals firing | Raise thresholds; combine with fit tier |
| First-party visit data | Use carefully and within privacy law; refer to the topic, not the tracking |
| Sensitive events (layoffs, crises) | Avoid or approach with great care |
| Same account, several signals | Combine into one stronger play; avoid multiple sequences |
| Signal source unreliable | Verify before acting; note the source in the record |
| Competitor customers | Respect contracts and timing; lead with value |

## Handoffs to related skills
- Scoring and tiers: `icp-account-scoring`
- Table and trigger design: `clay-table-design`
- Personalised copy: `ai-copy-columns`
- Routing to reps: `crm-sync-routing`
- Sending safely: `outbound-infrastructure`
- Results by signal: `gtm-reporting`

## Worked example
A lifecycle-marketing platform reviewed 40 recent wins and found most followed one of three events: a new head of growth, a Series A or B round, or a move away from a legacy email tool. It built three daily detection tables, scored signals with decay, wrote one play and opener per signal and routed tier A accounts to reps within 48 hours. Generic job-post triggers were dropped after a month because they produced replies but no meetings. Positive reply rates on signal-based sequences were about three times those of static lists, and most new pipeline came from the funding and new-leader plays.

## Common mistakes
- Tracking every possible signal.
- Acting weeks after the event.
- Creepy references to tracking data.
- Generic congratulations with no relevance.
- Not measuring results by signal.

## Output format
```
1. Predictive signals from win analysis
2. Signal definitions, sources and expiry
3. Scoring and decay rules
4. Play library with openers
5. Detection and routing workflow
6. Measurement plan by signal
```

## Self-check before you answer
- Are signals chosen from evidence of past wins?
- Do signals decay and expire?
- Does each signal have a play and a relevant, non-creepy opener?
- Are results measured by signal?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/signal-based-outbound/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
