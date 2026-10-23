---
name: gtm-workflow-documentation
description: "Document GTM engineering workflows so others can run and debug them: workflow specs, data dictionaries with meaning, source, run condition and cost, flow diagrams, runbooks for common failures, access lists without secrets, change logs, handovers and quarterly reviews. Use whenever someone needs to document Clay or GTM workflows, write a data dictionary or runbook, hand over GTM systems before leaving, onboard a new GTM engineer or require documentation from an agency."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/gtm-workflow-documentation/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-13"
---

# GTM Workflow Documentation

GTM systems often live in one person's head. When that person is on holiday or leaves, nobody knows why a table filters out certain countries, which provider is used for phones, what a column called "final_v3" does or how to restart a failed sync. Undocumented workflows break silently and cannot be improved, audited or handed over.

This skill documents GTM engineering work so others can run, debug and change it: a workflow spec, a data dictionary, diagrams of the flow, runbooks for routine runs and failures, change logs, ownership and access lists, and handover documents, kept short, current and stored where the team works.

## Operating principles
1. **Document for the next person.** Assume a capable newcomer with no context.
2. **Spec before build, update after change.** Documentation is part of the workflow, not an afterthought.
3. **Short and structured.** Templates beat long prose.
4. **One home.** All GTM docs live in one shared space, linked from each table.
5. **Owned and dated.** Every document has an owner and last-reviewed date.

## Document set
| Document | Purpose |
|---|---|
| Workflow spec | What the workflow does, inputs, outputs, rules, owner |
| Data dictionary | Every column and CRM field: meaning, source, format, cost |
| Flow diagram | Steps from source to CRM and sequencer |
| Runbook | How to run, monitor and fix the workflow |
| Change log | What changed, when, why and by whom |
| Access list | Tools, accounts, API keys (stored in a password manager), who has access |
| Handover | Status, open issues and contacts when ownership changes |

## When to use, and when not to
Use it when building a new workflow, after major changes, before someone leaves or goes on leave, during audits and when onboarding new GTM team members.

Don't use it to store secrets in documents; keys and passwords belong in a password manager.

## Inputs
- Access to the tables, integrations and CRM mappings.
- The builder's knowledge (interview or recorded walkthrough).
- QA specs and recent results.
- Costs and owners.

## Workflow

### Step 1. Write or update the spec
Purpose, trigger or schedule, inputs, outputs, ICP and exclusion rules, volumes, budget, owner, related tables.

### Step 2. Build the data dictionary
For each column: name, stage, meaning, source, type, format, run condition, cost, used by.

### Step 3. Draw the flow
A simple diagram from sources through enrichment, scoring, signals, copy, QA, CRM and sequencer, with failure points marked.

### Step 4. Write the runbook
How to start a run, what to check, normal results, common errors and fixes, who to escalate to.

### Step 5. Record access
Tools, integrations and who owns each account; where credentials are stored.

### Step 6. Start a change log
Every change with date, reason, person and QA result.

### Step 7. Store and link
One shared folder or wiki; link the spec from the table description.

### Step 8. Review
Quarterly, or after any major change; test the runbook with someone new.

## Workflow spec template
```
Workflow: <name> | Owner: <name> | Status: active | Last reviewed: <date>
Purpose: <one sentence>
Trigger or schedule: <daily 7am / on new signal / manual>
Inputs: <sources>
Rules: <ICP, exclusions, tiers>
Steps: <enrich, score, signals, copy, QA, push>
Outputs: <CRM objects, sequences, exports>
Volumes and budget: <rows per run, credits per month>
QA: <spec link, thresholds>
Dependencies: <other tables, providers, integrations>
```

## Data dictionary example
```
| Column | Meaning | Source | Format | Run condition | Cost |
| en_email | Verified work email | Waterfall: B, A, C + verifier | lowercase email | q_icp_ok and empty | 1 to 3 credits |
| sc_tier | Account tier | Formula from fit and timing | A/B/C/D | always | 0 |
| ai_opener | First line of email | AI prompt v4 | 1 sentence, <25 words | tier A/B and email valid | AI cost |
```

## Runbook template
```
How to run: <steps>
What good looks like: <match rate, QA pass rate, rows pushed>
Common problems:
- Match rate drops below 65% -> check provider status; rerun benchmark
- QA fail rate above 2% -> read QA report; fix causing step
- CRM push failures -> check error list; missing owner region
Escalation: <name, channel>
```

## Flow diagram example
```
Sources (Clay search, CRM exports, signals)
  -> Qualify (country, size, exclusions)
  -> Enrich (contacts, email waterfall, verification)
  -> Score (fit, timing, tier)
  -> Write (AI opener for tiers A and B)
  -> QA (spec checks, go or no-go)
  -> CRM (lookup, update or create, owner routing)
  -> Sequencer (enrol by tier, suppression)
Failure points: provider outages, AI column order, CRM API limits
```

## Handover template
```
Workflows owned: <list with status>
Running now: <schedules and next runs>
Open issues: <issue, impact, next step>
Recent changes: <link to change log>
Key contacts: <sales ops, data vendors, agency>
Budgets: <credits per month, renewal dates>
First-week checklist for the new owner: <steps>
```

## Change log format
```
| Date | Workflow | Change | Reason | By | QA result |
| 14 Oct | outbound-fintech | Reordered UK email waterfall | Benchmark: B cheaper per valid email | AA | Pass 0.9% |
```

## Using an AI agent
The agent can generate a first-draft data dictionary from a table export, turn a recorded walkthrough transcript into a runbook, draw a text flow diagram, keep the change log updated after each edit and flag documentation older than the last change. The owner checks accuracy, especially rules and costs.

Review documents quarterly and test the runbook with someone new.

## Minimum documentation for small teams
If time is short, keep three things for every active workflow: a one-paragraph spec, a column list with run conditions and a runbook of the three most common failures. These cover most handover risk.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Builder leaving next week | Record walkthroughs; write handover first, details after |
| Dozens of undocumented tables | Document active ones; archive the rest |
| Fast-changing workflows | Keep spec and change log; update dictionary monthly |
| Several builders | Shared templates and naming; peer review of changes |
| Agency-built workflows | Require documentation in the contract |
| Sensitive data rules | Document lawful basis and retention per source |

## Handoffs to related skills
- Table design and naming: `clay-table-design`
- QA specs: `gtm-workflow-qa`
- Audit: `gtm-engineering-audit`
- Process documents in general: the Workplace Writing `sops-process-docs` skill

## Worked example
A GTM engineer was leaving with 14 active workflows and no documentation. In two weeks the skill produced a spec and data dictionary for each active workflow from recorded walkthroughs, a flow diagram for the main outbound system, runbooks with the five most common failures, an access list pointing to the password manager and a change log template. Thirty-one unused tables were archived. The new owner ran every workflow in her first week, fixed a failed CRM sync using the runbook and made her first change through the change log with QA.

## Common mistakes
- Documentation written once and never updated.
- Long prose nobody reads.
- Secrets pasted into docs.
- No runbook for failures.
- Docs stored away from where work happens.

## Output format
```
1. Workflow spec
2. Data dictionary
3. Flow diagram (text or image)
4. Runbook
5. Access list
6. Change log
7. Handover notes if needed
```

## Self-check before you answer
- Could a newcomer run and debug the workflow from these documents?
- Does every column have a meaning, source and run condition?
- Are secrets kept out of the documents?
- Is there an owner and review date?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/gtm-workflow-documentation/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
