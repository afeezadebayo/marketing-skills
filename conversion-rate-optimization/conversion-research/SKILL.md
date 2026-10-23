---
name: conversion-research
description: "Plan and run conversion research that produces strong hypotheses: funnel and segment analysis, heatmaps, session recordings, on-page polls, exit and post-purchase surveys, user testing, interviews, support and review mining, form analytics and expert review, with privacy safeguards, triangulation and synthesis into prioritised hypotheses. Use whenever someone asks about conversion research, heatmaps, session recordings, on-site surveys, user testing, why visitors don't convert, research before A/B testing or where test ideas should come from."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/conversion-rate-optimization/conversion-research/
  category: marketing
  subcategory: conversion-rate-optimization
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Conversion Research Methods

Most failed A/B tests fail because the idea behind them was a guess. Conversion research replaces guesses with evidence about where visitors struggle and why. Quantitative data (analytics, funnels, heatmaps) shows what happens; qualitative research (session recordings, surveys, user tests, interviews, support tickets) explains why. Teams that do both find stronger hypotheses, win more tests and avoid wasting traffic on changes that were never going to matter.

This skill plans and runs conversion research: choosing methods for the question, collecting data ethically, analysing it and turning findings into prioritised hypotheses.

## Operating principles
1. **Start with a question.** "Why do mobile visitors abandon checkout?" beats "Let's look at heatmaps."
2. **Combine what and why.** Numbers locate problems; people explain them.
3. **Talk to the right people.** Visitors who didn't convert, new customers and lost leads reveal friction that loyal customers forget.
4. **Respect privacy.** Mask personal data in recordings, follow consent rules and keep data only as long as needed.
5. **End with hypotheses.** Research that doesn't change the test plan or the page wasn't finished.

## Research methods
| Method | Answers | Effort | Watch out for |
|---|---|---|---|
| Funnel and segment analysis | Where and for whom drop-off happens | Low | Broken tracking |
| Heatmaps (click, scroll) | What people click and how far they scroll | Low | Easy to over-read; segment by device |
| Session recordings | How people struggle in real sessions | Medium | Time-consuming; watch with a question in mind |
| On-page polls | Why visitors hesitate at a specific step | Low | Keep to one question; avoid leading wording |
| Exit or post-purchase surveys | What nearly stopped buyers; why others left | Low | Sample bias |
| User testing (moderated or unmoderated) | Where tasks fail and why | Medium | Small samples show problems, not frequencies |
| Customer interviews | Motivations, anxieties, decision criteria | Medium | Recall bias |
| Support tickets, chat logs, reviews | Recurring confusion and objections | Low | Skewed to problems |
| Form analytics | Which fields cause errors or abandonment | Low | Needs field-level tracking |
| Expert heuristic review | Usability and persuasion issues | Low | Opinion; confirm with data |

## When to use, and when not to
Use it before building a test roadmap, when tests keep losing, when a step leaks badly with no obvious cause, before redesigns and when entering new segments.

Don't use it to analyse completed experiments (the Growth Marketing `experiment-readout` skill) or for product usability research beyond conversion journeys.

## Inputs to ask for, in one message
1. The research question and the conversion step involved.
2. Analytics access and funnel data by segment.
3. Tools available: heatmaps and recordings (for example Hotjar, Microsoft Clarity, FullStory), survey tools, user testing platforms.
4. Access to customers or visitors for surveys and interviews.
5. Consent and privacy requirements in your markets.

## Workflow

### Step 1. Frame the question
Tie it to a funnel step and metric.

### Step 2. Locate the problem quantitatively
Funnel drop-offs by device, source, new versus returning and country; form field analytics; page speed by template.

### Step 3. Choose qualitative methods
Recordings and polls at the leaking step; user tests for task failures; surveys for motivations and objections.

### Step 4. Collect
Set sample targets (for example 30 to 50 recordings at the step, 100 or more poll responses, five to eight user tests per segment).

### Step 5. Analyse
Tag recordings and responses with themes; count frequency; note severity; pull quotes and clips.

### Step 6. Triangulate
A finding supported by two or more methods is stronger than one from a single source.

### Step 7. Write hypotheses
Evidence, change, audience, metric.

### Step 8. Prioritise and share
Score by impact, confidence and ease; share a short readout with clips and quotes.

## Survey questions that work
| Placement | Question |
|---|---|
| Exit intent on pricing page | "What, if anything, is stopping you from choosing a plan today?" |
| Checkout abandonment | "What made you leave checkout?" (with options plus "other") |
| Post-purchase | "What nearly stopped you from buying?" |
| Post-purchase | "What made you choose us over other options?" |
| Lead form thank-you | "What were you hoping to find today?" |
One question at a time, open text where possible, and no leading wording.

## Watching recordings efficiently
- Filter to sessions that reached the leaking step and didn't convert.
- Watch with one question in mind and tag what you see (rage clicks, errors, hesitation, back-and-forth).
- Stop when new sessions stop showing new patterns, often after 20 to 40.
- Record timestamps for clips to share.

## User test task example
```
Scenario: You run a 10-person design agency and want a tool to track client projects.
Task 1: Find out how much it would cost for your team.
Task 2: Decide which plan fits and start a trial.
Ask them to think aloud. Note where they hesitate, what they misunderstand and what they say they'd need to know.
```

## Research synthesis template
```
| Theme | Evidence (method, count) | Severity | Quote or clip | Hypothesis | Metric |
```

## Research sprint plan (one week)
| Day | Activity |
|---|---|
| 1 | Funnel and segment analysis; choose the leaking step |
| 2 | Launch on-page poll; watch 20 to 30 recordings |
| 3 | Run five user tests on the step |
| 4 | Review support tickets, chat logs and reviews for the same step |
| 5 | Synthesise themes, write hypotheses and score them |
A short sprint like this produces a test roadmap grounded in evidence within days rather than months.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Low traffic | Rely more on user tests, interviews and expert review |
| Strict privacy rules | Mask inputs, sample sessions, get consent for recordings where required |
| B2B with few buyers | Interview recent buyers and lost leads; shadow sales calls |
| Conflicting signals | Segment; the conflict often reveals two audiences |
| Stakeholders want quick answers | Run a one-week sprint: funnel data, 30 recordings, one poll, five user tests |

## Handoffs to related skills
- Overall audit: `cro-audit`
- Test prioritisation and roadmap: `cro-test-planning`
- Page-specific fixes: `landing-page-optimisation`, `form-optimisation`, `checkout-optimisation`, `pricing-page-optimisation`
- Copy from customer language: `conversion-copywriting`
- Customer interviews in depth: the Product Marketing `customer-research-interviews` skill

## Worked example
A SaaS company's pricing page had many visits and few trial starts. Heatmaps showed visitors scrolling to the comparison table and stopping; recordings showed repeated hovering over plan limits; an exit poll found many visitors unsure which plan suited a team of their size. Five user tests confirmed confusion about what counted as a user. Hypotheses: add a team-size selector that recommends a plan, and rewrite limits in plain language with examples. A test of the recommendation selector raised trial starts from the pricing page.

## Output format
```
# Conversion research readout: <question>, <date>
## Quantitative findings (where, for whom)
## Qualitative findings (why), with clips and quotes
## Triangulated themes
## Hypotheses (prioritised)
## Next steps
```

## Common mistakes
- Collecting data without a question.
- Reading heatmaps without segmenting.
- Leading survey questions.
- Treating five user tests as statistics.
- Research that never becomes hypotheses.

## Questions to ask before you research
- Which step and metric is the research about?
- Which methods can you run with your traffic and tools?
- What privacy rules apply to recordings and surveys?

## Self-check before you answer
- Is the research framed by a question and step?
- Are quantitative and qualitative methods combined?
- Are privacy and consent handled?
- Do findings end as prioritised hypotheses?

## Further reading
- Nielsen Norman Group on usability testing: https://www.nngroup.com/articles/usability-testing-101/
- Microsoft Clarity documentation: https://learn.microsoft.com/en-us/clarity/
- CXL ResearchXL framework: https://cxl.com/blog/

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/conversion-rate-optimization/conversion-research/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
