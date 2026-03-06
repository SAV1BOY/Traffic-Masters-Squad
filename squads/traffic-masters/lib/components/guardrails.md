# Guardrails Component

## Purpose
Define performance boundaries that trigger alerts or automatic actions.

## Guardrail Types

### Hard Guardrails (Auto-Pause)
- CPA exceeds 2x target for 3 consecutive days
- Daily spend exceeds 150% of daily budget
- Account policy violation detected
- Frequency exceeds 5.0 in 7 days

### Soft Guardrails (Alert & Review)
- CPA exceeds 1.3x target for 2 days
- CTR drops 25% below 7-day average
- ROAS drops below minimum threshold
- Budget pacing off by more than 15%

### Strategic Guardrails (Monthly Review)
- Platform concentration >70% on single platform
- Prospecting:Retargeting ratio outside 60-80:20-40 range
- New creative launch rate below 3/week
- Test velocity below 2 experiments/week

## Component Fields
- `guardrail_id`: Unique identifier
- `type`: hard | soft | strategic
- `metric`: Which metric is being guarded
- `threshold`: The boundary value
- `direction`: above | below
- `window`: Time period for evaluation
- `action`: What happens when triggered
- `escalation`: Who gets notified
- `override_allowed`: boolean

## Implementation
1. Set guardrails during campaign setup
2. Monitor daily (automated where possible)
3. Log all guardrail triggers in decisions log
4. Review and adjust thresholds monthly
