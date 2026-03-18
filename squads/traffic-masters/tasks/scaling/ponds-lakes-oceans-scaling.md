# Ponds, Lakes, Oceans Scaling

> **Type**: Task
> **Category**: scaling
> **Agents**: Kusmich, Scale Optimizer
> **Frameworks**: Kusmich Ponds-Lakes-Oceans, Pixel Maturity Model
> **Checklists**: ponds-lakes-oceans-checklist
> **Output template**: templates/stage-progression-plan.md

## ROUTING (from config.yaml)

> **Config key**: `routing.ponds-lakes-oceans-scaling`
> **Agents**: [nicholas-kusmich](../../agents/nicholas-kusmich.md), [scale-optimizer](../../agents/scale-optimizer.md)
> **Frameworks**: `kusmich-ponds-lakes-oceans`, `scaling-playbook`
> **Checklists**: `scaling-quality`, `kusmich/kusmich-ponds-lakes-oceans-scaling`
> **Templates**: `plans/scaling-plan-template`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Scale campaigns through the Ponds, Lakes, Oceans framework by progressively expanding audience size and budget as the pixel matures and accumulates conversion data, ensuring each stage builds on validated performance from the previous one.

## Inputs
- Current pixel maturity level: conversion volume and data quality
- Campaign performance history with audience size progression
- Scaling strategy with stage definitions
- Available audience segments by size tier
- Budget capacity for each scaling stage
- Platform optimization recommendations based on conversion volume

## Steps
1. Assess current pixel maturity: total conversions, weekly conversion volume, data recency
2. Define Ponds stage (small, targeted audiences, low budget):
   - Target warm audiences and tight interest stacks (10K-500K audience size)
   - Budget: $20-100/day per ad set
   - Goal: accumulate 50+ conversions for pixel learning
3. Define Lakes stage (medium audiences, moderate budget):
   - Expand to broader interests and lookalike audiences (500K-5M audience size)
   - Budget: $100-500/day per ad set
   - Goal: validate CPA at scale with 100+ weekly conversions
4. Define Oceans stage (broad audiences, high budget):
   - Target broad or open audiences leveraging pixel intelligence (5M+ audience size)
   - Budget: $500+/day per ad set
   - Goal: maximize volume at target efficiency with mature pixel
5. Set graduation criteria for each stage transition
6. Plan the audience progression path with specific audiences per stage
7. Adjust bid strategies per stage: manual at Ponds, automated at Oceans
8. Monitor pixel optimization events: ensure the right event has sufficient data
9. Plan creative volume increases to match audience expansion
10. Document current stage and progression timeline

## Output
Stage progression plan containing: current stage assessment, stage definitions with audience and budget parameters, graduation criteria, audience progression path, bid strategy per stage, creative requirements, and projected timeline.

## Quality Gate
- Ponds lakes oceans checklist confirms stage definitions and graduation criteria are clear
- Pixel data volume sufficient for current stage requirements
- Kusmich validates audience progression logic follows framework principles

## Duration
2-3 hours for initial assessment and planning; ongoing weekly reviews of 30-60 minutes
