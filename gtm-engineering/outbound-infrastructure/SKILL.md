---
name: outbound-infrastructure
description: "Set up and run cold outbound infrastructure: secondary domains, mailboxes, SPF, DKIM and DMARC, warm-up, capacity planning and moderate per-mailbox limits, verified lists, deliverable plain-text copy, Google and Yahoo sender requirements, health thresholds for bounces and complaints and an incident response plan. Use whenever someone sets up cold email infrastructure, buys sending domains, configures SPF, DKIM or DMARC, scales outbound volume, sees emails landing in spam, has rising bounces or wants to protect their main domain."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/outbound-infrastructure/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-13"
---

# Outbound Infrastructure and Deliverability

The best list and copy fail if emails land in spam. Since February 2024, Google and Yahoo require bulk senders to authenticate their domains with SPF, DKIM and DMARC, offer easy unsubscribes for marketing mail and keep spam complaint rates low, with Google guidance to stay below 0.3% and ideally under 0.1%. [Confirmed, Google and Yahoo sender requirements 2024] Cold outbound adds more risk: new domains, high volumes, unverified emails and repetitive copy all damage reputation, and recovering a burned domain takes weeks.

This skill sets up and runs outbound sending infrastructure: secondary domains, mailboxes, DNS authentication, warm-up, sending limits, list hygiene, copy and link practices, monitoring of bounces, complaints and placement, and a response plan when deliverability drops. It protects the main company domain at all times.

## Operating principles
1. **Protect the main domain.** Cold outbound runs on separate, similar domains.
2. **Authenticate everything.** SPF, DKIM and DMARC on every sending domain.
3. **Start slow, stay moderate.** Warm up new mailboxes and keep daily volumes per mailbox low.
4. **Clean lists only.** Verified emails, low bounce rates, no purchased spam traps.
5. **Monitor and react fast.** Bounces, complaints and reply rates are early warnings.

## Setup checklist
| Item | Detail |
|---|---|
| Secondary domains | Variants of the brand (for example getacme.com, acmehq.com), redirecting to the main site |
| Mailboxes | A few per domain, real names, profile photos and signatures |
| SPF | One record listing the sending service |
| DKIM | Enabled in the email provider, 2048-bit keys where possible |
| DMARC | Start at p=none with reports, move to quarantine or reject when stable |
| Custom tracking domain | If using link or open tracking |
| MX records | So replies arrive |
| Unsubscribe or opt-out | Clear way to stop emails; honour immediately |
| Business address | Where required by local law |

## Volume guidance
Many outbound teams keep each mailbox to tens of cold emails a day (often 30 to 50) after warm-up, and spread volume across several mailboxes and domains rather than pushing one hard. [Reported, common practitioner guidance] Treat these as starting points and adjust to results.

## When to use, and when not to
Use it when starting outbound, adding volume, after reply rates drop suddenly, when bounces or complaints rise, or when changing sending tools.

Don't use it for newsletters and marketing email to opted-in lists (the CRM and Lifecycle `email-deliverability` skill covers those) or to work around consent and anti-spam laws.

## Inputs
- Main domain, brand and email provider (Google Workspace, Microsoft 365 or other).
- Sequencer and sending tool.
- Planned monthly volume and number of reps.
- Current bounce, complaint and reply rates.
- Target countries and their email marketing rules.

## Workflow

### Step 1. Plan capacity
Monthly target sends divided by safe per-mailbox daily volume and working days gives the number of mailboxes; spread them across domains.

### Step 2. Buy and configure domains
Similar to the brand, redirecting to the main website; set DNS records.

### Step 3. Create mailboxes
Real sender names, signatures and photos; connect to the sequencer.

### Step 4. Authenticate
SPF, DKIM and DMARC; test with DNS and mail-tester tools.

### Step 5. Warm up
Two to four weeks of gradually increasing volume and engagement before cold sending.

### Step 6. Set sending rules
Daily limits per mailbox, random gaps between sends, sending windows in the recipient's time zone, stop on reply.

### Step 7. Protect list quality
Only verified emails; exclude invalid and, by policy, catch-all addresses; remove bounced contacts immediately.

### Step 8. Write deliverable copy
Plain text, few or no links in the first email, no images or attachments, varied wording, clear opt-out.

### Step 9. Monitor
Daily bounce and reply rates per mailbox; weekly placement tests; Google Postmaster Tools for domain reputation where volumes allow.

### Step 10. Respond to problems
Pause affected mailboxes, find the cause (list, copy, volume, authentication), fix and resume slowly.

## Health thresholds
| Metric | Healthy | Act |
|---|---|---|
| Bounce rate | Under 2% | Above 3%: pause and clean list |
| Spam complaint rate | Under 0.1% | Approaching 0.3%: pause and review |
| Positive reply rate | Stable or rising | Sudden drop: check placement |
| Inbox placement tests | Mostly inbox | Spam placement: reduce volume, review copy and authentication |

## Capacity example
Target: 6,000 cold emails a month across 20 working days = 300 a day. At about 30 a day per warmed mailbox, that needs 10 mailboxes; spread across three or four secondary domains with two or three mailboxes each, plus one or two spare warmed mailboxes to rotate in if any need to rest.

## Warm-up schedule example
| Week | Daily sends per mailbox | Notes |
|---|---|---|
| 1 | Warm-up only | Engagement-based warm-up tool or real conversations |
| 2 | 5 to 10 cold plus warm-up | Best-fit, verified contacts only |
| 3 | 15 to 20 cold plus warm-up | Watch bounces and replies daily |
| 4 | 25 to 30 cold plus warm-up | Hold here until metrics are stable |
Keep warm-up running in the background while sending.

## Copy practices that protect placement
- Plain text with a short signature; no images or attachments in first emails.
- At most one link, ideally none, in the first email.
- Vary wording across sequences; avoid identical text sent thousands of times.
- Avoid spam-trigger styles such as all caps, excessive punctuation and heavy sales language.
- Include a simple way to opt out and honour it immediately.

## Legal basics
Rules differ by country: some allow B2B cold email with a clear opt-out, others require consent or extra disclosures. Check the rules for each target country with qualified advice, keep suppression lists permanent and record the source of every contact.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Main domain already used for cold email | Move cold sending to secondary domains; monitor the main domain |
| Burned domain | Stop sending, let it rest, focus on new warmed domains |
| Microsoft-heavy recipients | Test placement on Outlook separately |
| Many countries | Check local consent and disclosure rules |
| Rapid scaling request | Add mailboxes and domains gradually, not volume per mailbox |
| Shared IPs on sending tools | Prefer providers with good reputation; monitor |

## Handoffs to related skills
- Verified emails: `enrichment-waterfalls`
- Copy quality: `ai-copy-columns`
- QA before sending: `gtm-workflow-qa`
- Costs of domains and mailboxes: `gtm-cost-control`
- Marketing email deliverability: the CRM and Lifecycle `email-deliverability` skill
- Email security: the Email and Inbox `email-security` skill

## Worked example
A team sent 400 cold emails a day from its main domain with no DMARC and saw replies fall and customer emails start landing in spam. The fix moved cold outbound to three secondary domains with nine mailboxes, set SPF, DKIM and DMARC, warmed up for three weeks, capped each mailbox at a moderate daily volume, verified every email, removed links from first emails and monitored bounces daily. Customer email placement recovered after the main domain stopped cold sending, bounces fell below 2% and positive replies returned to earlier levels.

## Common mistakes
- Cold emailing from the main domain.
- Skipping DMARC or warm-up.
- High volume from few mailboxes.
- Unverified lists and ignoring bounces.
- Link-heavy, templated first emails.

## Output format
```
1. Capacity plan (domains, mailboxes, volumes)
2. DNS and authentication checklist
3. Warm-up schedule
4. Sending rules
5. Copy and list hygiene rules
6. Monitoring dashboard and thresholds
7. Incident response steps
```

## Self-check before you answer
- Is the main domain protected from cold sending?
- Are SPF, DKIM and DMARC set on every sending domain?
- Are volumes per mailbox moderate after warm-up?
- Are bounces and complaints monitored with clear thresholds?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/outbound-infrastructure/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
