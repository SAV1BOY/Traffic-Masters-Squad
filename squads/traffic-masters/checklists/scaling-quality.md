# Scaling Quality
> **Type**: Quality Gate
> **Domain**: Growth & Optimization
> **Reviewed by**: Media Buyer

## Purpose
Ensures campaigns are scaled methodically with proper guardrails and rollback triggers. Premature or aggressive scaling destroys performance and wastes budget.

## Checklist

### Baseline Stability
- [ ] Campaign has been stable for a minimum of 7 consecutive days
- [ ] CPA or ROAS has been within acceptable range for the full stability period
- [ ] Daily conversion volume is consistent without erratic spikes or drops
- [ ] Campaign has exited the platform learning phase
- [ ] No major external factors (seasonality, promotions) are skewing baseline data

### Scaling Method Selection
- [ ] Scaling method is selected and documented (Vertical, Horizontal, or Mixed)
- [ ] Vertical scaling: increasing budget on existing winning ad sets
- [ ] Horizontal scaling: duplicating winners into new audiences or campaigns
- [ ] Mixed scaling: combining both approaches with clear rationale
- [ ] Method selection considers platform algorithm behavior and learning phase impact

### Increment Rules
- [ ] Budget increases follow a maximum 20% increment per change
- [ ] Minimum 48-72 hours between budget increases to allow stabilization
- [ ] Each increment is logged with date, amount, and resulting performance
- [ ] Larger increments (above 20%) require documented justification and approval
- [ ] Increments are planned in a scaling roadmap with projected spend levels

### Guardrails
- [ ] Maximum CPA or minimum ROAS threshold is defined for the scaling phase
- [ ] Daily spend limits are set at the campaign level as a ceiling
- [ ] Frequency caps are monitored to prevent audience fatigue during scale
- [ ] Audience overlap is checked between scaled campaigns and existing ones
- [ ] Performance is monitored daily during active scaling periods

### Rollback Triggers
- [ ] CPA increase threshold for rollback is defined (e.g., 30% above target for 48 hours)
- [ ] ROAS decrease threshold for rollback is defined
- [ ] Rollback process is documented (reduce budget to last stable level)
- [ ] Rollback is executed within 24 hours of trigger being met
- [ ] Post-rollback analysis is conducted to understand what went wrong

### Creative Backlog
- [ ] Sufficient creative variants are ready to support scaled delivery
- [ ] Minimum of 3-5 fresh creatives are in the pipeline for rotation
- [ ] Creative refresh schedule is accelerated to match higher spend levels
- [ ] Ad fatigue indicators are monitored more frequently during scaling
- [ ] New angles and hooks are being tested alongside scaling efforts

## Pass/Fail Criteria
All six sections must pass before scaling begins. Scaling without stable baselines or adequate creative backlog is prohibited.

## If Failed
Maintain current spend levels. Address the failing items before attempting to scale. If already mid-scale and failing, execute rollback to last stable configuration.

## Related
- `budget-pacing-quality.md`
- `creative-fatigue-quality.md`
- `experiment-design-quality.md`
