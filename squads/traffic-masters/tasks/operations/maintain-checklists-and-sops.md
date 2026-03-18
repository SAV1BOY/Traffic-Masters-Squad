# Maintain Checklists and SOPs

> **Type**: Task
> **Category**: operations
> **Agents**: Traffic Chief
> **Frameworks**: Continuous Improvement Framework, SOP Management
> **Checklists**: sop-maintenance-checklist
> **Output template**: templates/sop-update-log.md

## ROUTING

> **Agents**: traffic-chief, ads-analyst
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Keep all squad checklists and standard operating procedures current by reviewing them against actual workflows, incorporating lessons learned, updating for platform changes, and ensuring new team members can execute effectively.

## Inputs
- Current checklist and SOP inventory
- Feedback from squad agents on checklist accuracy and completeness
- Platform updates that affect existing procedures
- Lessons learned from recent campaigns and incidents
- New tasks or workflows that need documentation
- Industry best practice updates

## Steps
1. Inventory all existing checklists and SOPs with last-updated dates
2. Identify outdated documents: any checklist not updated in the past 90 days
3. Collect feedback from agents who use each checklist: what is missing, wrong, or unclear
4. Review platform change logs for updates that affect existing procedures
5. Incorporate lessons learned from recent campaign reviews and post-mortems
6. Update checklist items: add missing steps, remove obsolete ones, clarify ambiguous language
7. Create new checklists for any undocumented but recurring workflows
8. Validate updated checklists by having an agent walk through them on a real task
9. Version control all changes: document what changed and why
10. Distribute updated documents to all relevant agents
11. Archive deprecated checklists with notes on why they were retired
12. Set the next review cycle date (quarterly recommended)

## Output
SOP update log containing: inventory of all checklists with status, changes made with rationale, new checklists created, deprecated items, validation results, and next review schedule.

## Quality Gate
- SOP maintenance checklist confirms all documents reviewed within the cycle
- Updated checklists validated by at least one agent through actual use
- Traffic Chief approves all changes before distribution

## Duration
4-8 hours quarterly for full review cycle; 1-2 hours for individual updates as needed
