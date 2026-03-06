# Urgency Scale

## Purpose
Calibrate urgency level in communications based on situation severity.

## Scale Levels

### Level 1 — Informational (No Urgency)
- **Situation:** Routine updates, positive performance, general info
- **Tone:** Calm, factual, scheduled delivery
- **Timing:** Regular report cadence
- **Example:** "Weekly update: All metrics within target range."

### Level 2 — Advisory (Low Urgency)
- **Situation:** Trends to watch, minor deviations, opportunities
- **Tone:** Proactive, suggesting attention
- **Timing:** Next business day
- **Example:** "CTR trending down 10% this week. Monitoring — may need creative refresh."

### Level 3 — Action Needed (Moderate Urgency)
- **Situation:** Guardrails approached, budget pacing off, performance declining
- **Tone:** Direct, solution-oriented, time-sensitive
- **Timing:** Same day
- **Example:** "CPA exceeded 1.3x guardrail today. Recommend pausing underperforming ad sets. Awaiting approval."

### Level 4 — Alert (High Urgency)
- **Situation:** Guardrails breached, significant overspend, rapid performance decline
- **Tone:** Urgent, concise, immediate action language
- **Timing:** Within 1 hour
- **Example:** "ALERT: Daily spend pacing at 180% of budget. Pausing campaigns pending review."

### Level 5 — Critical (Emergency)
- **Situation:** Account suspension, policy violation, tracking failure, major error
- **Tone:** Emergency protocol, immediate escalation
- **Timing:** Immediate
- **Example:** "CRITICAL: Ad account restricted due to policy violation. All ads paused. Submitting appeal now."

## Response Protocol by Level

| Level | Action | Notify | Channel |
|-------|--------|--------|---------|
| 1 | Log | Team | Async (Slack/email) |
| 2 | Monitor | Team lead | Async |
| 3 | Act + inform | Stakeholder | Direct message |
| 4 | Act immediately | All stakeholders | Direct message + call |
| 5 | Emergency protocol | Everyone | Call + all channels |
