---
name: growth-loops
description: "Identify, design and strengthen growth loops where each user brings more: collaboration and viral loops, referral, user-generated and company-generated content loops, paid and sales loops and product output loops, with loop maps, viral coefficient, content conversion and cycle time, the weakest step, consented mechanics and experiments on each loop step. Use whenever someone asks about growth loops, viral growth, viral coefficient, network effects, user-generated content growth, growth beyond paid ads, or why growth is linear with spend."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/growth-loops/
  category: marketing
  subcategory: growth-marketing
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Growth Loops

Funnels describe a one-way journey: people come in at the top, some convert at the bottom, and you pour more in to grow. Loops describe a system where the output of one cycle becomes the input of the next: users create content that ranks and brings new users; users invite colleagues who become users who invite more; sales fund ads that bring customers whose revenue funds more ads. Companies with strong loops grow faster and spend less per customer as they scale.

This skill identifies, designs, measures and strengthens growth loops: viral and collaboration loops, user-generated content loops, paid loops, sales loops and product-led loops.

## Operating principles
1. **Loops compound; funnels don't.** Prioritise mechanisms where each new user brings in more.
2. **One or two primary loops.** Most successful companies are driven by a small number of loops.
3. **Measure each step.** A loop is only as strong as its weakest conversion.
4. **Speed matters.** Cycle time (how long one turn of the loop takes) changes growth as much as conversion.
5. **Loops must fit the product.** Forced sharing or invites that don't help users backfire.

## Common loop types
| Loop | How it works | Example |
|---|---|---|
| Collaboration (viral) | Using the product requires or benefits from inviting others | Shared documents, team chat, scheduling links |
| Referral (incentivised) | Users invite others for a reward | Credit for both referrer and friend |
| User-generated content (UGC) | Users create content that attracts new users via search or social | Reviews, Q&A, templates, public profiles |
| Company-generated content | Content attracts users who convert, revenue funds more content | SEO content engine |
| Paid loop | Revenue from customers funds acquisition of more customers | Payback-driven paid acquisition |
| Sales loop | Revenue funds salespeople who bring more revenue | Sales-led B2B |
| Product output loop | Product output carries branding to new audiences | "Made with" badges, shared reports, email signatures |

## When to use, and when not to
Use it when growth is linear with spend, when designing a new product's growth engine, when referral or sharing features underperform, and when planning long-term growth strategy.

Don't use it for a one-off acquisition test (`acquisition-channel-testing`) or a referral reward programme in detail (`referral-programmes`).

## Inputs to ask for, in one message
1. Product, users and how value is created and shared.
2. Current acquisition sources with volumes.
3. Data on invites, shares, content created, public pages and their conversion.
4. Cycle times: how long from sign-up to inviting or creating content.
5. Revenue and payback data for paid loops.

## Workflow

### Step 1. Map current loops
Draw how users currently arrive and whether any of them generate new users. Quantify each step with data.

### Step 2. Calculate loop strength
For viral loops: invites sent per user × invite conversion rate = new users per user per cycle (the viral coefficient, K). For content loops: content created per user × visits per content × visit-to-user conversion.

### Step 3. Measure cycle time
Time from a user joining to their first invite, share or content creation, and from that to the new user joining.

### Step 4. Find the weakest step
Which step has the lowest conversion or longest delay? That's where to work.

### Step 5. Design improvements
Make sharing part of getting value (not a pop-up), shorten time to first share, improve the experience for invited users, make public content indexable and useful.

### Step 6. Test
Experiment on loop steps with metrics for each step and for retention of new users.

### Step 7. Monitor
Track loop metrics weekly alongside the north star.

## Loop metrics
| Metric | Definition |
|---|---|
| Viral coefficient (K) | New users generated per existing user per cycle |
| Cycle time | Average time for one loop turn |
| Invite rate | Share of users sending at least one invite |
| Invite conversion | Share of invites that become active users |
| Content conversion | New users per piece of user content |
| Loop share of acquisition | Share of new users arriving through loops |
K below 1 still helps: it amplifies other channels. Even K = 0.3 means every 100 users acquired bring 43 over time (100 × (0.3 + 0.09 + ...)).

## Loop map template
```
New user signs up
  -> reaches first value (activation rate __%, median __ days)
  -> creates shareable output / invites / content (rate __%, median __ days)
  -> exposure to new people (views or invites per user __)
  -> new person signs up (conversion __%)
  -> back to start
Loop strength (K) = invites or exposures per user x conversion
Cycle time = days from sign-up to new user's sign-up
```

## Improving each step
| Step | Typical problem | Improvement |
|---|---|---|
| Activation before sharing | Users share before seeing value | Prompt sharing after first value |
| Share or invite rate | Sharing is an afterthought | Build sharing into the core task |
| Exposure | Shared output lacks context | Clear branding and a reason to try |
| Invitee conversion | Generic landing experience | Personalised invite page showing who invited them and why |
| New user activation | Invitees drop off | Shortened onboarding for invited users |

## Content loops and search
User-generated content loops depend on pages being indexable, useful and unique. Thin, duplicate or low-quality UGC pages can hurt search visibility. Set quality thresholds (minimum content, moderation) before pages are indexed, and use internal links from strong pages to new ones.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Solo-use product | Look for output loops (sharing results) or content loops instead of invites |
| B2B with gatekeepers | Focus on in-company spread (team invites) rather than consumer-style virality |
| UGC quality risk | Moderation and quality thresholds before pages are indexed |
| Privacy-sensitive products | Sharing must be opt-in and clear about what is visible |
| Spammy invite flows | Never auto-send invites from address books without explicit consent |

## Handoffs to related skills
- Referral rewards: `referral-programmes`
- Loop contributions in forecasts: `growth-model`
- Experiments on loop steps: `experiment-design`
- SEO for UGC and content loops: the Content SEO and Technical SEO skills
- Tracking invites and shares: `tracking-plan`

## Worked example
A scheduling tool grew mainly through paid search. Mapping showed every booking page displayed the brand, and 4% of people who booked through someone's page later signed up. Cycle time was long because new users waited weeks before sharing their link. Improvements: prompt link sharing right after setup with ready-made email signature snippets, improve the "powered by" message on booking pages with a one-click sign-up, and optimise the invitee sign-up flow. The share of sign-ups from the booking-page loop rose from 12% to 27% over two quarters, reducing blended CAC.

## Output format
```
# Growth loops review: <company>, <date>
## Loop map (current) with step conversion
## Loop strength (K, content conversion) and cycle time
## Weakest step and diagnosis
## Improvement ideas and experiments
## Loop metrics dashboard
```



## Common mistakes
- Adding share buttons and calling it a loop.
- Ignoring cycle time.
- Poor experience for invited users.
- Incentives that attract low-quality users.
- Spammy or non-consented invite mechanics.

## Questions to ask before you design
- Does using the product naturally involve other people or produce shareable output?
- Where do new users come from today, beyond paid channels?
- How long does it take a new user to bring another?

## Self-check before you answer
- Are loops mapped with real conversion data?
- Are K and cycle time calculated?
- Is the weakest step identified and tested?
- Are mechanics consented and valuable to users?

## Further reading
- Reforge, growth loops essays: https://www.reforge.com/blog
- Andrew Chen, The Cold Start Problem (2021)

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/growth-marketing/growth-loops/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
