# Scaling and Stability Loop
> **Type**: Workflow
> **Duration**: Ongoing (weekly cycles)
> **Agents involved**: media-buyer, performance-analyst, traffic-chief, scale-optimizer

## Trigger
Campaign achieves stable CPA/ROAS for 7+ consecutive days with 50+ conversions.

## Steps
1. Stability Validation → Agent: performance-analyst → Framework: Coefficient of Variation → Output: Stability score confirming CPA variance below 20% over 7 days
2. Scale Readiness Check → Agent: scale-optimizer → Framework: Mandalia Scale Criteria → Output: Green light with recommended scale increment (15-20% budget increase)
3. Incremental Scale → Agent: media-buyer → Framework: Gradual Budget Increase → Output: Budget increased, timestamp logged
4. 48h Monitor → Agent: performance-analyst → Framework: GECO-ANA → Output: Performance delta report comparing pre/post scale metrics
5. Stabilize or Rollback → Agent: media-buyer → Framework: Decision Matrix → Output: If CPA within 15% of target, hold; if above, rollback to prior budget
6. Horizontal Scale → Agent: scale-optimizer → Framework: Audience Expansion → Output: New ad sets with lookalikes, interest expansion, or geo expansion
7. Document Learnings → Agent: performance-analyst → Framework: Scale Log → Output: Entry documenting what worked, what did not, and current ceiling

## Quality Gates
- [ ] 7-day stability confirmed before any scale action
- [ ] Budget increase never exceeds 20% per increment
- [ ] Minimum 48h between scale actions
- [ ] CPA monitored at ad set level, not just campaign
- [ ] Creative frequency below 3.0 across scaled audiences
- [ ] No audience overlap above 25% with new expansions
- [ ] Learning phase not re-triggered unnecessarily

## Output
Documented scaling trajectory with performance at each increment.
Identified scaling ceiling and recommended next strategies.
Updated budget forecast based on proven scale capacity.

## Scaling Methods (Priority Order)
1. Vertical: Budget increase on winning ad sets (15-20% increments)
2. Horizontal: Duplicate winners into new audiences
3. Geographic: Expand to new regions/states
4. Platform: Replicate winning angles on new platforms
5. Funnel: Add retargeting layers to capture more conversions

## Notes
- CBO campaigns are more resilient to budget scaling than ABO
- Monday and Tuesday are safest days to scale (full week of data ahead)
- Never scale during platform instability or holiday anomalies
- Sobral rule: if it breaks at scale, the creative was carrying the campaign

> **Quality Gates Reference**: See [Quality Gates Guide](../docs/quality-gates-guide.md) for gate definitions and override policy.
