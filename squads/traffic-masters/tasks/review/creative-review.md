# Creative Review

> **Type**: Task
> **Category**: review
> **Agents**: Creative Analyst
> **Frameworks**: Creative Evaluation Framework, Performance-Creative Correlation
> **Checklists**: creative-review-checklist
> **Output template**: templates/creative-feedback.md

## ROUTING (from config.yaml)

> **Config key**: `routing.creative-review`
> **Agents**: [creative-analyst](../../agents/creative-analyst.md)
> **Frameworks**: `burns-kaizen-kreative`, `creative-iteration-loop`
> **Checklists**: `creative-fatigue-quality`, `creative/angle-coverage-quality`
> **Templates**: `reports/creative-analysis-report`
> **Registry**: `data/registries/creatives-registry`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Review creative assets for strategic alignment, brand consistency, platform compliance, and performance potential before deployment, and evaluate live creatives for ongoing performance and optimization opportunities.

## Inputs
- New creative assets awaiting approval for deployment
- Live creative performance data: CTR, hook rate, hold rate, conversion rate, CPA
- Brand guidelines and compliance requirements
- Creative strategy with approved angles and messaging
- Platform-specific best practices and policy requirements
- Swipe file for competitive context

## Steps
1. Review new creatives for brand guideline compliance: visual identity, tone, messaging
2. Check new creatives against platform advertising policies for potential rejections
3. Validate message alignment: does the creative deliver the intended angle and hook
4. Assess creative quality: visual clarity, audio quality, text readability, mobile optimization
5. Verify CTA clarity: is the next step obvious and compelling
6. Check offer presentation: is the offer clearly communicated with proper proof elements
7. Review live creative performance data: rank by primary KPI with sufficient data
8. Identify creatives showing fatigue signals: declining CTR, rising frequency, dropping conversion rate
9. Flag creatives ready for retirement or refresh
10. Identify high-potential creatives that could benefit from iteration or variant testing
11. Provide specific, actionable feedback for each creative reviewed
12. Update the creative performance tracker with review findings

## Output
Creative feedback document containing: new creative approval status with notes, live creative performance rankings, fatigue alerts, retirement recommendations, iteration opportunities, specific feedback per creative, and performance tracker update.

## Quality Gate
- Creative review checklist confirms all pending and live creatives evaluated
- Feedback is specific and actionable, not vague or subjective
- Creative Analyst confirms no policy-risk creatives are approved for launch

## Duration
1-2 hours depending on creative volume; recurring weekly
