# Account Structure Review

> **Type**: Task
> **Category**: review
> **Agents**: Ads Analyst
> **Frameworks**: Account Architecture Framework, Campaign Hierarchy Best Practices
> **Checklists**: account-structure-checklist
> **Output template**: templates/structure-assessment.md

## ROUTING (from config.yaml)

> **Config key**: `routing.account-structure-review`
> **Agents**: [ads-analyst](../../agents/ads-analyst.md)
> **Frameworks**: `account-structure-meta`, `account-structure-google`
> **Checklists**: `account-audit-quality`
> **Templates**: `reports/audit-report-template`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Review the advertising account structure across all platforms to ensure campaigns are properly organized, audiences are not overlapping, naming conventions are consistent, and the architecture supports both performance and reporting clarity.

## Inputs
- Current account structure across all platforms
- Campaign naming convention documentation
- Audience targeting details per campaign and ad set
- Budget allocation across campaigns
- Reporting requirements and dashboard structure
- Platform-specific structural best practices

## Steps
1. Map the current account structure: campaigns, ad sets, ads hierarchy per platform
2. Evaluate campaign segmentation logic: is the split by objective, funnel stage, audience, or product logical
3. Check for audience overlap between ad sets and campaigns using platform overlap tools
4. Review naming conventions: are they consistent, descriptive, and supporting automated reporting
5. Assess budget distribution: does the structure allow proper budget flow to winners
6. Evaluate CBO vs ABO decisions: are they appropriate for each campaign's needs
7. Check for campaign consolidation opportunities: fragmented campaigns diluting learning
8. Review ad group structure in Google: are keywords properly grouped by theme and intent
9. Verify exclusion logic: are converters excluded from prospecting, are windows properly separated
10. Assess structural support for reporting: can performance be sliced by the dimensions leadership needs
11. Identify structural inefficiencies that are limiting platform optimization algorithms
12. Document recommended structural changes with migration plan if needed

## Output
Structure assessment containing: current structure map, overlap analysis, naming convention audit, consolidation opportunities, structural inefficiencies, recommended changes with rationale, and migration plan if restructuring is needed.

## Quality Gate
- Account structure checklist confirms all platforms and structural elements reviewed
- Audience overlap analysis completed with specific overlap percentages documented
- Ads Analyst confirms recommendations will not disrupt current learning phase campaigns

## Duration
2-4 hours per platform; 1-2 hours for documentation and migration planning
