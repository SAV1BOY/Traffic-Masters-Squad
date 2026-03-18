# Platform Updates Monitoring

> **Type**: Task
> **Category**: operations
> **Agents**: Ads Analyst
> **Frameworks**: Platform Intelligence Framework, Change Management Protocol
> **Checklists**: platform-monitoring-checklist
> **Output template**: templates/platform-update-log.md

## ROUTING

> **Agents**: traffic-chief, ads-analyst
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Monitor advertising platform changes including algorithm updates, new features, policy changes, and deprecations to proactively adapt campaigns and squad procedures before changes impact performance.

## Inputs
- Platform official blogs and announcement channels: Meta Business Blog, Google Ads Blog, TikTok for Business, LinkedIn Marketing Blog
- Platform release notes and changelog feeds
- Industry news sources and analyst commentary
- Platform beta program access (if enrolled)
- Squad's current platform usage and feature dependencies
- Historical platform changes and their measured impact

## Steps
1. Check official platform blogs and announcement channels for new updates
2. Review platform dashboards for new features, UI changes, or notification banners
3. Monitor industry news sources for reported algorithm changes or beta features
4. Categorize each update: new feature, algorithm change, policy update, deprecation, UI change
5. Assess impact level for each update: high (requires immediate action), medium (requires planning), low (informational)
6. Identify which current campaigns or workflows are affected by each update
7. Document required actions: settings changes, strategy adjustments, checklist updates
8. Test new features in a controlled environment before broad adoption
9. Brief relevant squad agents on updates that affect their work
10. Update checklists and SOPs to reflect platform changes
11. Log the update with date, description, impact assessment, and actions taken
12. Share a periodic platform update summary with the full squad

## Output
Platform update log containing: update inventory with categorization, impact assessments, required actions, feature test results, SOP update notes, and periodic summary for squad distribution.

## Quality Gate
- Platform monitoring checklist confirms all platforms checked on schedule
- High-impact updates communicated to affected agents within 24 hours
- Ads Analyst validates impact assessments are accurate and actions are appropriate

## Duration
30-60 minutes weekly for monitoring; additional time for high-impact changes
