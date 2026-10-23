---
name: ai-copy-columns
description: "Design AI copy columns for outbound in Clay or similar tools: one job per column, clean short inputs, prompts with rules, examples and fallbacks, gating to qualified tiers, a five-part scoring rubric, QA for placeholders and invented facts, prompt rotation and reply-rate monitoring by version. Use whenever someone writes AI personalisation prompts, AI openers or subject lines in Clay, gets generic or invented AI copy, wants better cold email personalisation at scale or needs to test and score AI-written outbound lines."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/ai-copy-columns/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-13"
---

# AI Copy Columns

AI-written personalisation can lift reply rates when it says something specific and true about the prospect. It damages results and reputation when it produces flattering filler ("I love what you're doing at Acme"), invents facts, repeats the same structure across thousands of emails, or leaves placeholders behind. The model only knows what the row gives it, so most bad AI copy comes from weak inputs and vague prompts rather than from the model.

This skill designs AI copy columns in Clay or similar tools: choosing what to personalise, feeding the right inputs, writing prompts with rules and examples, constraining length and style, preventing invented facts, handling missing data, testing and scoring outputs, and integrating copy into sequences that still read as written by a person.

## Operating principles
1. **Inputs decide quality.** The prompt can only use facts present in the row.
2. **Specific and relevant.** Mention something real and connect it to the prospect's likely problem.
3. **No invented facts.** If the data is missing, use a safe fallback, not a guess.
4. **Short and plain.** One or two sentences that sound like a person, not a brochure.
5. **Test before scale.** Review samples by segment and score them against a rubric.

## What to personalise
| Element | Good inputs | Example output |
|---|---|---|
| Opener | Signal, role, recent event | "You're hiring three SDRs this quarter; ramp time is usually where pipeline slips." |
| Relevance line | Industry, use case, pain point | "Payments teams often lose a day each month reconciling payouts by hand." |
| Proof point | Matching case study by segment | "A UK lender cut reconciliation from 5 days to 1 with us." |
| Subject line | Topic of the opener | "SDR ramp at Acme" |
| Call to action | Tier and offer | "Worth a 15-minute look next week?" |

## When to use, and when not to
Use it for outbound openers, relevance lines, subject lines, LinkedIn notes, account research summaries and call prep notes.

Don't use it to write whole emails from nothing at volume, to fake familiarity, or for regulated claims that need approval.

## Inputs
- The fields available per row (signals, role, industry, company facts, website summary).
- The offer, value proposition and proof points by segment.
- Tone and style rules, banned phrases and English variant.
- Examples of good and bad lines.
- The sequence the copy will sit in.

## Workflow

### Step 1. Decide the job of each column
One column, one output: opener, relevance line, subject line or proof point.

### Step 2. Prepare inputs
Clean, short fields: a signal summary, the role, the industry, a one-line company description. Avoid feeding whole web pages into copy prompts.

### Step 3. Write the prompt
Role, task, inputs, rules, length, style, banned phrases, fallback behaviour and two or three examples.

### Step 4. Add a fallback
If key inputs are empty, return a segment-level line or a blank flagged for review rather than inventing.

### Step 5. Gate the column
Run only on qualified tiers with required inputs present.

### Step 6. Test on samples
Generate 20 to 50 outputs across segments; score them; refine the prompt.

### Step 7. Add QA checks
Length, placeholders, banned phrases, company and signal references and an AI judgement check for invented facts.

### Step 8. Monitor results
Reply rates by prompt version and segment; rotate or retire weak prompts.

## Prompt template
```
You write the first line of a cold email for <offer>.
Inputs:
- First name: {first_name}
- Role: {title}
- Company: {company_name}
- Signal: {signal_summary}
- Industry: {industry}
Rules:
- One sentence, under 25 words, British English.
- Mention the signal or the company's situation, then link it to <problem>.
- Use only facts in the inputs. Never invent numbers, news or names.
- No flattery, no "I hope this finds you well", no exclamation marks, no em dashes.
- If the signal is empty, write a line about a common <industry> problem instead.
Good example: "You're opening in Kenya next quarter; local payouts are usually the first thing that breaks."
Bad example: "I love what you're building at Acme!"
Return only the sentence.
```

## Scoring rubric
| Criterion | 0 | 1 | 2 |
|---|---|---|---|
| Specific | Generic | Somewhat specific | Clearly about this company or person |
| True | Invented or wrong | Unclear | Fully supported by inputs |
| Relevant | Unrelated to offer | Loosely related | Links to a problem we solve |
| Natural | Sounds like AI or marketing | Mixed | Sounds like a person |
| Rules | Breaks rules | Minor issues | Follows all rules |
Ship prompts that average 8 or more out of 10 on samples.

## Research columns versus copy columns
Separate research from writing. A research column summarises a website, job post or news item into two or three plain facts; a copy column then writes from those facts. This keeps copy prompts short, makes facts easy to check in QA and lets the same research feed several copy columns, subject lines and rep call notes.

## Avoiding AI tells
Watch for patterns readers recognise as machine-written: flattery openers, "I noticed" and "I came across", triplets of adjectives, em dashes, exclamation marks and perfectly parallel sentences in every email. Add these to the banned list, vary sentence length and let some lines be plain and short. Read ten outputs in a row; if they sound alike, the prompt needs variety.

## Versioning prompts
Name prompts with a version and date, record which rows used which version and compare reply rates by version. Change one thing at a time so improvements can be traced.

Have a person read a random sample of sent lines each week, even after QA, to catch drift.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Thin data for a segment | Use a segment-level relevance line; personalise less |
| Several languages | Separate prompts per language; native review |
| Regulated industries | Approved claims only; no performance promises |
| Same structure in every email | Rotate two or three prompt variants; vary length |
| Sensitive signals (layoffs) | Skip or use neutral, respectful language |
| Model outputs vary by run | Lower creativity settings; keep examples tight |

## Handoffs to related skills
- Signals feeding inputs: `signal-based-outbound`
- Table gating: `clay-table-design`
- QA before sending: `gtm-workflow-qa`
- Copywriting principles: the Content, Copy and PR `marketing-copywriting` skill
- Removing AI tells: the Content, Copy and PR `ai-writing-cleanup` skill
- Results by prompt: `gtm-reporting`

## Worked example
A team's AI opener column used a vague prompt with the whole company website as input and produced lines such as "Impressive growth at Acme!" across thousands of rows, with 4% mentioning news that did not exist. The rebuild fed a short signal summary, role and industry, added rules, a fallback and two examples, gated the column to tier A and B and scored 50 samples per segment. After two prompt revisions the average score rose from 5 to 8.6, invented facts disappeared in QA and positive reply rate roughly doubled over the next month.

## Common mistakes
- Feeding long, noisy inputs.
- No rule against invented facts.
- No fallback for missing data.
- Flattery instead of relevance.
- Scaling before scoring samples.

## Output format
```
1. Column purpose and inputs
2. Prompt with rules, examples and fallback
3. Run conditions
4. Sample outputs with rubric scores
5. QA checks
6. Monitoring plan by prompt version
```

## Self-check before you answer
- Does the prompt use only facts present in the row?
- Is there a fallback for missing inputs?
- Were samples scored before scaling?
- Are QA checks in place for placeholders and invented facts?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/ai-copy-columns/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
