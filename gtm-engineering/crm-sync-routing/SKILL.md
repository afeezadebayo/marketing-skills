---
name: crm-sync-routing
description: "Sync GTM tables to CRMs and sequencers safely: field mapping with direction and overwrite rules, lookups before create, protected rep and system fields, ownership and routing by territory, tier and capacity, enrolment and suppression rules, source stamping, error handling and weekly monitoring. Use whenever someone connects Clay or another GTM tool to HubSpot, Salesforce or a sequencer, sees duplicates or overwritten CRM data, needs account routing rules or wants to stop sequencing people already in deals."
license: CC-BY-4.0
metadata:
  author: Afeez Adebayo
  author_url: https://afeezadebayo.com
  author_linkedin: https://www.linkedin.com/in/afeez-adebayo/
  author_x: https://x.com/za_icon
  source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/crm-sync-routing/
  category: marketing
  subcategory: gtm-engineering
  version: "1.0.0"
  created: "2026-10-10"
  updated: "2026-10-13"
---

# CRM Sync and Routing

The last step of a GTM workflow is where the most damage happens. Enriched data overwrites what reps typed, duplicate records appear, accounts land with the wrong owner, contacts are added to sequences while already talking to sales, and nobody can trace where a record came from. A careful sync turns good table work into pipeline; a careless one erodes trust in the CRM.

This skill designs how GTM tables sync to CRMs (HubSpot, Salesforce or similar) and sequencers: field mapping, create-versus-update logic, field ownership and overwrite rules, deduplication lookups, account and contact ownership, routing by territory, tier and capacity, sequence enrolment rules, suppression, source tracking, error handling and monitoring.

## Operating principles
1. **Look up before you create.** Every push checks for existing accounts and contacts first.
2. **Never overwrite human data.** Rep-entered and system-critical fields are protected.
3. **One owner per account.** Routing rules decide ownership before outreach starts.
4. **Do not sequence active conversations.** Suppress anyone in an open deal, recent conversation or opt-out.
5. **Trace every record.** Source, workflow, date and version are stamped on each record.

## Field mapping table
```
| Table column | CRM object.field | Direction | Overwrite rule | Required |
| in_domain | Company.domain | Table -> CRM | Only if empty | Yes |
| en_email | Contact.email | Table -> CRM | Only if empty | Yes |
| sc_tier | Company.gtm_tier | Table -> CRM | Always update | Yes |
| sc_fit_score | Company.fit_score | Table -> CRM | Always update | No |
| title | Contact.job_title | Table -> CRM | Only if empty or older than 90 days | No |
| owner | Company.owner | CRM -> Table | Never from table | Yes |
| src_workflow | Contact.lead_source_detail | Table -> CRM | Set on create only | Yes |
```

## Field ownership
| Type | Examples | Rule |
|---|---|---|
| System fields | IDs, created dates, lifecycle stage | CRM owns; never written by the table |
| Rep-owned fields | Notes, next steps, owner, deal stage | Never overwritten |
| Enrichment fields | Employees, industry, tech stack | Updated on schedule with source and date |
| Score fields | Fit, timing, tier | Always updated by the scoring workflow |
| Source fields | Workflow, list, date | Set once on create |

## When to use, and when not to
Use it when connecting Clay or another tool to a CRM or sequencer, when CRM data gets overwritten or duplicated, when routing is unclear, or before scaling automated pushes.

Don't use it for full CRM implementation or lifecycle design (the CRM and Lifecycle skills), though it should follow their definitions.

## Inputs
- CRM objects, fields and permissions.
- Ownership and territory rules.
- Sequencer and its enrolment options.
- Suppression lists: customers, open deals, opt-outs, competitors.
- The table spec and QA results.

## Workflow

### Step 1. Map fields
Table columns to CRM fields with direction, overwrite rules and requirements.

### Step 2. Define create versus update
Look up companies by domain and contacts by email (then LinkedIn URL); update if found, create only if not.

### Step 3. Protect fields
Set overwrite rules and test them on a sandbox or a small batch.

### Step 4. Set ownership and routing
Existing owner wins; otherwise route by territory, segment, tier and rep capacity; round-robin within a team.

### Step 5. Define enrolment rules
Only QA-passed, tier-appropriate contacts with valid emails, no open deals, no recent activity and no opt-outs.

### Step 6. Stamp the source
Workflow name, table, version and date on create.

### Step 7. Handle errors
Failed pushes go to an error list with reasons; retry rules; alert the owner.

### Step 8. Monitor
Weekly report on records created, updated, failed, duplicates found and routing exceptions.

## Routing rules example
```
1. If the company has an owner in the CRM -> keep owner.
2. If tier A and region UK -> UK enterprise team (round-robin by capacity).
3. If tier A and region West Africa -> Lagos team.
4. If tier B -> SDR pool, round-robin.
5. If tier C -> nurture sequence, no owner.
6. Tier D -> not pushed.
```

## Suppression checks
| Check | Source | Action |
|---|---|---|
| Existing customer | CRM lifecycle stage | Do not sequence; notify account owner if a signal fired |
| Open deal | Deal pipeline | Do not sequence; send signal to the deal owner |
| Contacted in last 30 to 90 days | Activity history | Hold |
| Unsubscribed or opted out | CRM and sequencer | Never contact |
| Competitor or partner | Lists | Exclude |

## Signals for existing customers and deals
When a signal fires for a customer or an account with an open deal, do not sequence; instead create a task or alert for the owner with the signal and a suggested action, such as an expansion conversation after a funding round. This turns GTM data into account management value without annoying active buyers.

## Testing a sync
Before going live, push 20 to 50 tagged records, check every mapped field in the CRM, confirm protected fields were untouched, check owners and sequence enrolment, then delete or untag the test records. Repeat after any mapping change. Keep a rollback plan, such as a saved export of affected records, for bulk updates.

Document every mapping change with the date and reason.

## Monitoring report example
```
Week 42: created 640 | updated 1,120 | failed 18 (missing owner region) | duplicates blocked 210 | routing exceptions 6
```
Investigate any rise in failures or duplicates the same week.

Agree mapping and routing changes with sales operations before releasing them.

## Edge cases and judgement calls
| Situation | What to do |
|---|---|
| Contact exists under a different company | Check for job change; create new association, keep history |
| Several contacts per account | Limit per account; sequence by persona and priority |
| Account owned by an inactive rep | Route by rules and notify sales operations |
| API limits | Batch pushes; schedule off-peak |
| Sandbox not available | Test with a tagged small batch and roll back plan |
| Regional data rules | Store and route data according to local requirements |

## Handoffs to related skills
- Deduplication before push: `data-deduplication-normalisation`
- Tiers used in routing: `icp-account-scoring`
- QA before push: `gtm-workflow-qa`
- Documentation of mappings: `gtm-workflow-documentation`
- Lead routing in depth: the CRM and Lifecycle `lead-scoring-routing` skill
- CRM hygiene: the CRM and Lifecycle `crm-data-hygiene` skill

## Worked example
A team pushed Clay contacts straight into HubSpot. Within a month, 900 duplicate contacts appeared, rep notes were overwritten by enrichment, and 40 contacts in open deals received cold sequences. The redesign added domain and email lookups, a mapping table with overwrite rules, protected rep-owned fields, routing that kept existing owners and assigned new accounts by region and tier, suppression for customers, open deals and recent activity, and source stamps on every record. A 50-record test batch passed. Duplicates stopped, reps stopped complaining about lost notes and no active deals were sequenced again.

## Common mistakes
- Creating records without lookups.
- Overwriting rep-entered fields.
- Sequencing people in open deals or recent conversations.
- No source stamps, so nobody knows where data came from.
- Ignoring failed pushes.

## Output format
```
1. Field mapping with overwrite rules
2. Create-versus-update logic
3. Ownership and routing rules
4. Enrolment and suppression rules
5. Source stamping
6. Error handling and monitoring report
```

## Self-check before you answer
- Does every push look up existing records first?
- Are rep-owned and system fields protected?
- Are suppression rules applied before enrolment?
- Is every record stamped with its source?

---
Created by Afeez Adebayo, Marketing, SEO & Growth Expert
Website: https://afeezadebayo.com
LinkedIn: https://www.linkedin.com/in/afeez-adebayo/
X: https://x.com/za_icon
Source: https://afeezadebayo.com/skills-md/marketing/gtm-engineering/crm-sync-routing/

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). You may copy, share and adapt this skill, including for commercial use, as long as you credit Afeez Adebayo and link to the source URL above. Keep this notice in any copy or adapted version.
