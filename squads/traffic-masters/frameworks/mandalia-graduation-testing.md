# Graduation Testing

> **Author**: Depesh Mandalia
> **Domain**: Creative Testing and Scaling Pipeline
> **Used by agents**: media-buyer, performance-analyst, strategy-orchestrator
> **Checklists**: testing-launch-checklist, graduation-review-checklist

## Overview

Graduation Testing is Depesh Mandalia's systematic pipeline for moving ad concepts from initial test to full-scale deployment. It prevents two common failures: scaling unproven concepts too fast (wasting budget) and killing potential winners too early (missing opportunities). Every concept must earn its way through phases — no skipping, no exceptions.

## When to Use

- Launching new creative concepts, audiences, or offers
- Establishing a repeatable testing process for an account
- When ad performance is inconsistent due to lack of testing discipline
- Building a pipeline of proven winners ready for scaling
- Training media buyers on structured testing methodology

## The Framework

### Sandbox Phase (Exploration)
1. **Budget**: $5-20 per day per ad set
2. **Duration**: 3-7 days minimum
3. **Purpose**: Test many concepts cheaply to find signals
4. **Setup**: Multiple ad sets with distinct creative concepts
5. **Optimization**: Optimize for the lowest-funnel event you can still get data on
6. **Volume**: Run 5-10+ concepts simultaneously
7. **Metrics to watch**: CTR, CPC, engagement rate, early conversion signals
8. **Graduation criteria**: Meets or exceeds benchmark CTR and CPC for 3+ consecutive days

### Phase 1 (Validation)
1. **Budget**: 2-3x Sandbox budget ($15-60 per day)
2. **Duration**: 7-14 days
3. **Purpose**: Validate that Sandbox winners perform with more budget and time
4. **Setup**: Only graduated Sandbox winners move here
5. **Optimization**: Optimize for conversion events (purchase, lead, ATC)
6. **Volume**: 3-5 concepts from Sandbox
7. **Metrics to watch**: CPA, ROAS, conversion rate, cost per result
8. **Graduation criteria**: Profitable CPA/ROAS sustained for 7+ days

### Phase 2 (Proving)
1. **Budget**: Scale budget based on Phase 1 performance ($50-200+ per day)
2. **Duration**: 14-30 days
3. **Purpose**: Prove the concept works at higher spend and broader audiences
4. **Setup**: Phase 1 winners with expanded targeting
5. **Optimization**: Optimize for primary business KPI
6. **Volume**: 2-3 proven concepts
7. **Metrics to watch**: CPA at scale, frequency, audience saturation, ROAS stability
8. **Graduation criteria**: Stable or improving CPA at 3x+ Phase 1 budget for 14+ days

### Graduation (Scaling Deployment)
1. Move proven winners to main scaling campaigns
2. Apply scaling recipes (V-Scale, H-Scale, M-Scale, Nitro)
3. Continue monitoring for fatigue and saturation
4. Feed learnings back into new Sandbox tests

### Pipeline Management
- Always have concepts in every phase simultaneously
- Sandbox should never be empty — continuous testing feeds the pipeline
- Track graduation rates to measure creative quality over time

## Key Concepts

- **Never skip phases**: A concept that looks great in Sandbox may fail at Phase 1 budget
- **Never scale losers**: Hope is not a strategy. If it does not graduate, it dies.
- **Volume in Sandbox, quality in Phase 2**: Cast a wide net early, narrow ruthlessly
- **Learning phase respect**: Give each phase enough time and budget to exit learning phase
- **Pipeline continuity**: The biggest scaling bottleneck is usually a dry creative pipeline

## Decision Rules

- IF a Sandbox concept does not meet CTR/CPC benchmarks in 3 days THEN cut it
- IF a Sandbox concept is borderline THEN extend to 7 days maximum before deciding
- IF a Phase 1 concept has high CPA for 5+ days THEN demote back or cut
- IF a Phase 2 concept shows rising CPA with rising frequency THEN audience saturation — pause and test new audiences
- IF graduation rate is below 10% THEN creative quality is the bottleneck — revisit avatar and messaging
- IF graduation rate is above 30% THEN you may not be testing boldly enough — try riskier angles

## Common Mistakes

- Scaling directly from Sandbox to full budget (skipping validation)
- Running too few Sandbox concepts (low volume = low chance of finding winners)
- Cutting Sandbox concepts after 1 day (insufficient data)
- Emotional attachment to concepts that do not graduate
- Not maintaining a continuous Sandbox pipeline (feast-or-famine creative supply)
- Using the same benchmarks for every niche (adjust for industry and funnel stage)

## Integration

- Depends on: mandalia-3n-ads-formula (concepts entering Sandbox should follow 3N)
- Feeds into: mandalia-scaling-recipes (graduated winners are scaled using recipes)
- Feeds into: mandalia-punisher-method (non-graduates are punished and cut)
- Connects to: mandalia-ac4 (test results diagnose which AC4 lever needs work)

## Output

- A live testing pipeline with concepts tracked across all phases
- Graduation status for each concept (Sandbox / Phase 1 / Phase 2 / Graduated / Cut)
- Benchmark metrics for each phase (CTR, CPC, CPA, ROAS thresholds)
- Weekly pipeline health report: concepts in each phase, graduation rate, pipeline velocity
