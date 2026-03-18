# Account Audit (30-60-90 Day)

> **Type**: Task
> **Category**: reporting
> **Agents**: Ads Analyst, Traffic Chief, Aslam
> **Frameworks**: Account Audit Framework, 30-60-90 Day Improvement Plan
> **Checklists**: account-audit-checklist
> **Output template**: templates/audit-report-plan.md

## ROUTING (from config.yaml)

> **Config key**: `routing.account-audit-30-60-90`
> **Agents**: [ads-analyst](../../agents/ads-analyst.md), [traffic-chief](../../agents/traffic-chief.md), [kasim-aslam](../../agents/kasim-aslam.md)
> **Frameworks**: `burns-sgp-30-60-90`, `account-structure-meta`, `account-structure-google`
> **Checklists**: `account-audit-quality`, `burns/burns-ncac-mpi-metrics-audit`
> **Templates**: `reports/audit-report-template`, `plans/30-60-90-growth-plan`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Conduct a comprehensive account audit evaluating campaign structure, targeting, creative, bidding, tracking, and overall strategy to identify improvement opportunities and build a prioritized 30-60-90 day action plan.

## Inputs
- Full access to all ad platform accounts
- Historical performance data: minimum 90 days preferred
- Current campaign structure and settings documentation
- Tracking setup documentation
- Business goals and KPI targets
- Previous audit reports (if available)

## Steps
1. Audit account structure: campaign organization, naming conventions, segmentation logic
2. Review campaign settings: objectives, bidding strategies, budget allocation, scheduling
3. Analyze audience targeting: overlap, saturation, relevance, exclusion gaps
4. Evaluate creative performance: winner/loser ratio, diversity, refresh cadence, fatigue levels
5. Audit keyword strategy (Google): match types, negative keywords, search query relevance
6. Review tracking setup: pixel health, event accuracy, attribution settings
7. Assess landing page alignment: message match, load speed, mobile experience
8. Analyze budget efficiency: spend distribution vs performance, wasted spend identification
9. Check for common mistakes: audience overlap, creative fatigue, missing exclusions, wrong objectives
10. Score each audit area on a 1-5 scale with specific findings and evidence
11. Prioritize improvements by impact and effort using ICE scoring
12. Build the 30-60-90 day plan: quick wins (30d), structural fixes (60d), strategic improvements (90d)

## Output
Audit report and plan containing: audit scorecard, detailed findings per area, prioritized improvement list, 30-day quick wins, 60-day structural fixes, 90-day strategic improvements, expected impact projections, and resource requirements.

## Quality Gate
- Account audit checklist confirms all audit areas covered with evidence
- All findings supported by specific data or examples from the account
- Traffic Chief and Aslam validate prioritization and feasibility of the improvement plan

## Duration
6-10 hours for full audit; 2-3 hours for plan development and documentation
