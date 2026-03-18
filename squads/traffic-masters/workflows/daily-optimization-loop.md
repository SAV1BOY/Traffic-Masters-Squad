# Daily Optimization Loop
> **Type**: Workflow
> **Duration**: 30-60 minutes daily
> **Agents involved**: media-buyer, performance-analyst

## Trigger
Every business day at 09:00 local time, or when anomaly alerts fire.

## Steps
1. Data Pull → Agent: performance-analyst → Framework: GECO-ANA → Output: Daily performance dashboard refresh with key metrics
2. Anomaly Detection → Agent: performance-analyst → Framework: Statistical Thresholds → Output: Flagged metrics outside normal range (CPL +20%, ROAS -15%, CTR drop >25%)
3. Root Cause Diagnosis → Agent: media-buyer → Framework: Sobral Diagnostic Tree → Output: Identified cause (creative fatigue, audience saturation, bid competition, external factor)
4. Action Decision → Agent: media-buyer → Framework: Mandalia Decision Matrix → Output: Specific action (pause, scale, adjust bid, swap creative, expand audience)
5. Implementation → Agent: media-buyer → Framework: Platform SOP → Output: Changes applied in ad platform with notes
6. Documentation → Agent: media-buyer → Framework: Change Log → Output: Entry in optimization log with action, rationale, expected outcome
7. End-of-Day Review → Agent: performance-analyst → Framework: Delta Analysis → Output: Impact of changes made, comparison to prior day

## Quality Gates
- [ ] All active accounts checked
- [ ] Anomalies diagnosed with root cause
- [ ] No action taken without documented rationale
- [ ] Budget pacing within 5% of target
- [ ] Creative frequency checked (cap at 3.0 for cold)
- [ ] Spend vs. conversion volume reconciled

## Output
Updated optimization log with daily actions and rationale.
Dashboard reflecting current state of all active campaigns.

## Escalation Rules
- If CPA exceeds 2x target for 48h → escalate to traffic-chief
- If spend pacing is 20% under → check delivery and escalate
- If platform flags policy violation → pause immediately and notify compliance

## Notes
- Weekend performance is reviewed Monday morning with 3-day lookback
- Never optimize on less than 50 conversions or 48h of data for CBO campaigns
- Log format: Date | Account | Action | Rationale | Expected Impact

> **Quality Gates Reference**: See [Quality Gates Guide](../docs/quality-gates-guide.md) for gate definitions and override policy.
