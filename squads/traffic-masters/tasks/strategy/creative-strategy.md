# Creative Strategy

> **Type**: Task
> **Category**: strategy
> **Agents**: Ad Midas, Creative Analyst, Burns
> **Frameworks**: Kaizen Kreative, Creative Diversity Matrix
> **Checklists**: creative-strategy-checklist
> **Output template**: templates/creative-strategy.md

## ROUTING (from config.yaml)

> **Config key**: `routing.creative-strategy`
> **Agents**: [ad-midas](../../agents/ad-midas.md), [creative-analyst](../../agents/creative-analyst.md), [ralph-burns](../../agents/ralph-burns.md)
> **Frameworks**: `burns-kaizen-kreative`, `creative-testing-framework`, `creative-angle-matrix`, `pittman-ad-grid-7-steps`
> **Checklists**: `creative-brief-quality`, `burns/burns-creative-lab-deep-dive`, `creative/angle-coverage-quality`
> **Templates**: `briefs/creative-brief`, `plans/creative-production-plan`
> **Registry**: `data/registries/creatives-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Plan the creative approach for all campaigns including angle prioritization, format selection, creative backlog development, production pipeline design, and testing methodology to ensure a continuous supply of high-performing ad creatives.

## Inputs
- Hook and angle bank from research
- Swipe file with competitor analysis
- ICP and avatar document
- Platform-specific creative requirements
- Budget available for creative production
- Brand guidelines and asset library

## Steps
1. Define the creative diversity matrix: angles x formats x hooks x audiences
2. Prioritize top angles based on avatar research and competitive gap analysis
3. Select initial creative formats per platform: static, video, carousel, UGC, motion graphics
4. Build the creative backlog with specific briefs for each angle-format combination
5. Design the production pipeline: briefing, scripting, production, review, iteration
6. Establish the testing methodology: variable isolation, sample size, winner criteria
7. Set creative volume targets: number of new creatives per week/sprint
8. Define the creative review process and approval workflow
9. Plan the creative refresh cadence based on expected fatigue timelines
10. Establish performance benchmarks: CTR, hook rate, hold rate, conversion rate by format
11. Document the Kaizen Kreative iteration process for scaling winners

## Output
Creative strategy document containing: creative diversity matrix, prioritized angle list, format selection rationale, production pipeline design, testing methodology, volume and cadence targets, review workflow, and performance benchmarks.

## Quality Gate
- Creative strategy checklist confirms all elements of the Kaizen Kreative framework addressed
- Burns validates creative volume supports projected spend levels
- Ad Midas approves angle prioritization and format selections

## Duration
3-4 hours for strategy development; 1-2 hours for documentation
