# Attribution Quality
> **Type**: Quality Gate
> **Domain**: Measurement & Analytics
> **Reviewed by**: Analytics Lead

## Purpose
Ensures attribution methodology is sound, documented, and reconciled across platforms. Without reliable attribution, optimization decisions are based on flawed data.

## Checklist

### Attribution Window Documentation
- [ ] Click-through attribution window is defined for each platform
- [ ] View-through attribution window is defined for each platform
- [ ] Window settings are documented with rationale for each choice
- [ ] Windows are consistent with the typical sales cycle length
- [ ] Changes to attribution windows are logged with dates and reasons

### Model Selection
- [ ] Attribution model is selected (last-click, first-click, data-driven, linear, etc.)
- [ ] Rationale for model selection is documented
- [ ] Model aligns with the business sales cycle and funnel complexity
- [ ] Team understands the implications and limitations of the chosen model
- [ ] Model selection is reviewed quarterly or when strategy changes

### Cross-Platform Reconciliation
- [ ] Total conversions are compared across all ad platforms
- [ ] Platform-reported conversions are compared against CRM or backend data
- [ ] Revenue figures from ad platforms are reconciled with actual revenue
- [ ] Discrepancies between platforms are identified and explained
- [ ] A single source of truth is designated for final reporting

### Sanity Checks
- [ ] Sum of platform-attributed conversions does not exceed total actual conversions by more than 20%
- [ ] No single platform claims credit for more conversions than actually occurred
- [ ] Blended ROAS or CPA is calculated and compared to platform-specific metrics
- [ ] Trends in attribution data align with known business events
- [ ] Anomalies in attribution data are investigated within 48 hours

### Limitations Documentation
- [ ] Known blind spots in attribution are documented (dark social, word of mouth)
- [ ] iOS privacy restrictions and their impact are acknowledged
- [ ] Cookie deprecation implications are noted and mitigation planned
- [ ] View-through attribution inflation risks are documented
- [ ] Team is trained on attribution limitations to avoid overconfidence

### Incrementality Planning
- [ ] Incrementality testing is planned or scheduled for key channels
- [ ] Holdout test methodology is defined (geo-lift, conversion lift, PSA tests)
- [ ] Budget is allocated for incrementality experiments
- [ ] Historical incrementality results are documented and referenced
- [ ] Incrementality findings are used to calibrate platform-reported data

## Pass/Fail Criteria
All checklist items must pass. Attribution quality directly impacts all optimization and budget decisions and cannot be compromised.

## If Failed
Flag specific attribution gaps. Convene analytics and media buying teams to align on fixes. Do not make significant budget reallocation decisions until attribution quality is restored.

## Related
- `tracking-plan-quality.md`
- `pixel-and-capi-quality.md`
- `reporting-quality.md`
- `cross-platform-consistency-quality.md`
