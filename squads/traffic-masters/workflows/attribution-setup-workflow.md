# Attribution Setup Workflow
> **Type**: Workflow
> **Duration**: 3-5 business days
> **Agents involved**: pixel-specialist, performance-analyst, traffic-chief

## Trigger
New account setup, attribution model review, or data discrepancy investigation.

## Steps
1. Pixel Audit → Agent: pixel-specialist → Framework: Pixel Health Check → Output: All platform pixels verified firing correctly with event match quality scores
2. CAPI Implementation → Agent: pixel-specialist → Framework: Server-Side Setup → Output: Conversions API configured for Meta, Google Enhanced Conversions enabled
3. UTM Framework → Agent: pixel-specialist → Framework: UTM Taxonomy → Output: Standardized UTM parameters: source, medium, campaign, content, term
4. Attribution Model Selection → Agent: performance-analyst → Framework: Model Comparison → Output: Recommended model (last-click, data-driven, position-based) with rationale
5. Cross-Platform Reconciliation → Agent: performance-analyst → Framework: Data Reconciliation → Output: Mapping document showing how platform data maps to GA4 and CRM
6. Incrementality Baseline → Agent: performance-analyst → Framework: Geo-Split or Holdout → Output: Incrementality test design for key channels
7. Dashboard Setup → Agent: performance-analyst → Framework: Multi-Touch View → Output: Attribution dashboard showing all models side by side
8. Documentation → Agent: pixel-specialist → Framework: Attribution Playbook → Output: Complete attribution documentation for the account

## Quality Gates
- [ ] All pixels firing with correct parameters and values
- [ ] CAPI event match quality above 6.0 (Meta)
- [ ] UTM parameters consistent across all campaigns
- [ ] GA4 attribution model configured and validated
- [ ] Platform-reported vs GA4-reported conversions reconciled
- [ ] Incrementality test plan documented (even if not yet executed)
- [ ] Team trained on reading multi-touch attribution data

## Output
Complete attribution framework with documentation.
Reconciliation map between platforms.
Attribution dashboard accessible to all team members.
Incrementality test plan for future execution.

## Notes
- No single attribution model is "correct" — use multiple as lenses
- Platform self-attribution always over-reports; GA4 under-reports
- The truth is usually between platform data and GA4 data
- Review attribution setup quarterly as platforms change their models
- iOS 14+ and cookie deprecation make server-side tracking essential

> **Quality Gates Reference**: See [Quality Gates Guide](../docs/quality-gates-guide.md) for gate definitions and override policy.
