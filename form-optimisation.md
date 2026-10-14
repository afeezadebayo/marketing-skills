---
name: form-optimisation
description: "Improve sign-up, lead, quote, contact and application forms: field-level analytics, field justification, ordering and multi-step design, labels, input types and autocomplete, flexible formats, inline validation and specific errors, privacy reassurance, mobile and accessibility fixes and changes judged on completion and qualified leads. Use whenever someone asks about form conversion, form abandonment, too many form fields, multi-step forms, form validation errors, lead form quality or improving a sign-up or quote form."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/conversion-rate-optimization/form-optimisation/
  category: marketing
  subcategory: conversion-rate-optimization
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-10"
---

# Form Optimisation

Forms are where intent turns into action: sign-ups, demo requests, quotes, applications, checkouts. They are also where many visitors give up. Too many fields, unclear labels, aggressive validation, surprise requirements and slow mobile keyboards each add friction. Small improvements to a form that thousands of people start every month can add more conversions than any new campaign.

This skill audits and improves forms using field analytics, usability principles and research: what to ask, in what order, with which inputs and messages, balancing completion rate with lead quality.

## Operating principles
1. **Ask only what you need now.** Every field must earn its place; collect the rest later.
2. **Make errors hard and recovery easy.** Clear labels, helpful formats, inline validation and kind messages.
3. **Design for mobile first.** Correct keyboard types, autofill, large tap targets.
4. **Balance volume and quality.** For lead forms, judge changes on qualified leads, not just submissions.
5. **Measure at field level.** Know which fields cause hesitation, errors and abandonment.

## Common friction points
| Friction | Fix |
|---|---|
| Too many fields | Remove, defer to later steps or progressive profiling |
| Unclear labels or placeholder-only labels | Visible labels above fields; examples as hint text |
| Strict formats (phone, postcode, dates) | Accept common formats; normalise on the server |
| Errors shown only after submit | Inline validation after the field is completed |
| Vague error messages | Say what is wrong and how to fix it |
| Password rules revealed late | Show requirements up front; allow show password |
| Required phone number without reason | Make optional or explain why it's needed |
| No autofill support | Correct autocomplete attributes |
| Wrong mobile keyboard | Input types for email, tel, number |
| CAPTCHA puzzles | Invisible bot protection where possible |

## When to use, and when not to
Use it for sign-up, lead, demo, quote, contact, application and checkout forms with high abandonment or low quality, and before launching new forms.

Don't use it for full checkout redesigns (`checkout-optimisation`) or onboarding after sign-up (`signup-flow-optimisation`).

## Inputs to ask for, in one message
1. Form URL, purpose and what happens after submission.
2. Form starts, completions and field-level analytics if available.
3. Which fields are used downstream (by sales, onboarding, billing) and why.
4. Lead quality data for lead forms (qualification rate by source and field answers).
5. Recordings or user tests of the form.
6. Legal or compliance requirements (consent, data protection).

## Workflow

### Step 1. Measure
Starts versus completions; time to complete; field-level drop-off, corrections and errors.

### Step 2. Justify every field
For each field: who uses it, for what, and could it be collected later? Remove or defer what isn't needed now.

### Step 3. Order and group
Start with easy questions, group related fields, use multi-step forms for longer flows with a progress indicator.

### Step 4. Improve inputs
Labels, hints, input types, autocomplete attributes, sensible defaults, address lookup where helpful.

### Step 5. Improve validation and errors
Inline validation, accepting common formats, specific error messages that keep entered data.

### Step 6. Reduce anxiety
Privacy reassurance near email and phone fields, what happens next, expected response times.

### Step 7. Check mobile and accessibility
Tap targets, keyboard types, focus order, labels for screen readers, error announcements.

### Step 8. Test and measure
Completion rate and, for lead forms, qualified lead rate; run tests where traffic allows.

## Field justification table
```
| Field | Used by | Purpose | Needed now? | Alternative |
| Company size | Sales | Routing and qualification | Yes | Enrich from domain |
| Phone | Sales | Call booking | No | Optional, or ask after booking |
| Job title | Marketing | Personalisation | No | Ask during onboarding |
```

## Multi-step form guidelines
- First step asks the easiest, least sensitive questions.
- Show progress (step 1 of 3).
- Save progress so users can return.
- Put qualifying questions where they help routing, not as a wall at the start.

## Error message examples
| Poor | Better |
|---|---|
| Invalid input | Enter an email address like name@company.com |
| Phone number invalid | Enter your phone number with or without spaces, for example 07700 900123 |
| Password does not meet requirements | Use at least 8 characters, including a number |
| Error | We could not reach the server. Your answers are saved; try again |
Good messages say what happened, how to fix it and keep what the user already typed.

## Autocomplete attributes worth setting
| Field | Attribute |
|---|---|
| Full name | name |
| Email | email |
| Phone | tel |
| Address lines | address-line1, address-line2 |
| Postcode | postal-code |
| Card number (checkout) | cc-number |
Correct attributes let browsers and password managers fill forms in seconds, which matters most on mobile.

## Field-level metrics
| Metric | What it shows |
|---|---|
| Field drop-off | The last field people touched before leaving |
| Time in field | Hesitation or confusion |
| Corrections and refills | Unclear formats or labels |
| Error rate | Validation that is too strict or unclear |
| Blank optional fields | Fields people see no value in |

## Lead quality guardrail
When removing qualifying fields from lead forms, track the share of submissions that sales accepts or that become opportunities. If quality falls, replace the field with enrichment from the email domain or ask the question on the thank-you page or in the first call instead.

## Consent and privacy
Show consent options clearly and unticked where the law requires, link to the privacy notice near personal data fields and explain briefly how contact details will be used. Clear explanations reduce anxiety and abandonment.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Sales wants many qualifying fields | Use enrichment and fewer, better questions; test quality impact |
| Regulated forms (finance, health) | Keep required fields, improve explanations and layout |
| High spam | Invisible bot checks, honeypots and server validation rather than puzzles |
| International users | Flexible name, address and phone formats |
| Very long applications | Multi-step with save and resume |

## Handoffs to related skills
- Overall audit: `cro-audit`
- Research on hesitation: `conversion-research`
- Checkout forms: `checkout-optimisation`
- Sign-up flows: `signup-flow-optimisation`
- Mobile issues: `mobile-conversion`
- Lead quality and scoring: the CRM and Lifecycle `lead-scoring-routing` skill

## Worked example
A home insurance broker's quote form had 14 fields on one page, a strict phone format and errors shown only on submit. Field analytics showed most abandonment at phone and date of birth. The redesign started with postcode and property type, moved personal details to step two with a progress bar, accepted any common phone format, added inline validation and a line explaining why date of birth was needed. Completion rose substantially, and qualified quote rates held steady because the key qualifying fields remained.

## Output format
```
# Form review: <form>, <date>
## Funnel and field-level analytics
## Field justification table
## Recommended structure (steps, order)
## Input, validation and error improvements
## Mobile and accessibility fixes
## Hypotheses and test plan
```

## Common mistakes
- Asking for data nobody uses.
- Placeholder text instead of labels.
- Rejecting valid input formats.
- Errors that clear the whole form.
- Judging lead forms only on submission volume.

## Questions to ask before you change the form
- Who uses each field, and when?
- Where do users hesitate or make errors?
- How is lead quality measured?

## Self-check before you answer
- Is every field justified?
- Are validation and errors helpful and inline?
- Is the form mobile-friendly and accessible?
- Are changes judged on the right quality metric?

## Further reading
- Baymard Institute form usability research: https://baymard.com/research
- W3C Web Accessibility Initiative forms tutorial: https://www.w3.org/WAI/tutorials/forms/
- MDN autocomplete attribute reference: https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/conversion-rate-optimization/form-optimisation/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
