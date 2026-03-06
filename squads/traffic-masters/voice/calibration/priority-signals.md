# Priority Signals Calibration Guide

## Purpose
Framework for consistently signaling the priority and urgency of tasks, recommendations, and issues in paid traffic operations. Ensures the team and stakeholders can quickly assess what needs attention first.

---

## Priority Levels

| Level | Label | Response Time | Description | Signal Words |
|---|---|---|---|---|
| **P0** | Emergency | Immediate (minutes to hours) | Critical system failure, tracking broken, account disabled, major budget overrun | "URGENT," "IMMEDIATE," "CRITICAL" |
| **P1** | High Priority | Same day / within 24 hours | Performance significantly degraded, approaching budget limit, key campaign failing | "High priority," "Action needed today," "Time-sensitive" |
| **P2** | Standard Priority | This week | Normal optimization work, scheduled changes, routine improvements | "This week," "Standard priority," "Recommended" |
| **P3** | Low Priority | This month / when capacity allows | Nice-to-have improvements, long-term optimizations, exploratory ideas | "When time permits," "Worth considering," "Non-urgent" |
| **P4** | Backlog | No specific deadline | Future ideas, documentation improvements, process enhancements | "For future consideration," "Backlog" |

---

## P0: Emergency

### When to Use
- Tracking/pixel completely broken (zero conversions recording)
- Ad account disabled or restricted
- Budget overrun exceeding 200% of daily target
- Security breach or unauthorized account access
- All campaigns stopped delivering with no clear cause

### Communication Format
```
[P0 - EMERGENCY] [ISSUE_TITLE]

Account: {{ACCOUNT}}
Impact: {{QUANTIFIED_IMPACT}}
Started: {{TIME}}
Status: {{INVESTIGATING/CONTAINED}}
Owner: {{NAME}}
Next Update: {{TIME}}
```

### Language
- "URGENT: [ISSUE]. Immediate action required."
- "This is a P0 emergency. All other work on this account is on hold until resolved."
- "Impact: $[AMOUNT] in potential lost/wasted spend per hour this remains unresolved."

---

## P1: High Priority

### When to Use
- CPA exceeds 2x target for 48+ hours
- ROAS drops below break-even for 48+ hours
- Budget pacing significantly off-track (> 30% variance)
- Ad disapprovals on high-spend campaigns
- Client escalation or urgent request
- Critical creative fatigue (all top creatives fatigued simultaneously)

### Communication Format
```
[P1 - HIGH PRIORITY] [ISSUE_TITLE]

Summary: {{1-2 SENTENCES}}
Impact: {{QUANTIFIED}}
Deadline: {{WHEN_THIS_NEEDS_TO_BE_RESOLVED}}
Proposed Action: {{ACTION}}
Owner: {{NAME}}
```

### Language
- "High priority: [ISSUE]. Needs resolution by end of day."
- "This requires action today. If unaddressed, the impact will be [QUANTIFIED_IMPACT]."
- "Flagging as P1. Please prioritize this over P2/P3 items."

---

## P2: Standard Priority

### When to Use
- Routine weekly optimizations (pause underperformers, scale winners)
- Creative refresh within normal cadence
- Budget reallocation between campaigns
- A/B test setup and evaluation
- Regular reporting and analysis
- Audience expansion or refinement

### Communication Format
```
[P2] [TASK_DESCRIPTION] -- Due: [DATE]

Context: {{BRIEF_CONTEXT}}
Action: {{SPECIFIC_ACTION}}
Expected Impact: {{OUTCOME}}
```

### Language
- "Recommended for this week: [ACTION]."
- "Standard optimization: [TASK]. No urgency, but should be completed by [DATE]."
- "Adding to this week's optimization list."

---

## P3: Low Priority

### When to Use
- Exploratory audience tests
- Process improvements
- Documentation updates
- Long-term strategy research
- Platform feature exploration
- Nice-to-have creative variations

### Communication Format
```
[P3] [TASK_DESCRIPTION] -- No deadline

Context: {{WHY_THIS_IS_WORTH_DOING}}
Impact: {{EXPECTED_OUTCOME}}
```

### Language
- "When capacity allows, we should consider [ACTION]."
- "Non-urgent, but worth adding to the roadmap."
- "Lower priority, but this could yield [OUTCOME] if we find time this month."

---

## Urgency Modifiers

### Increasing Urgency
- "This is time-sensitive because [REASON]."
- "The window for this opportunity closes on [DATE]."
- "Each day without action increases the impact by approximately [AMOUNT]."
- "Escalating from P2 to P1 due to [NEW_INFORMATION]."

### Decreasing Urgency
- "This is important but not urgent. No immediate action needed."
- "De-escalating from P1 to P2 -- the situation has stabilized."
- "This can wait until after [OTHER_PRIORITY] is resolved."

---

## Priority Decision Matrix

### How to Assign Priority

| Factor | P0-P1 (High) | P2 (Standard) | P3-P4 (Low) |
|---|---|---|---|
| **Revenue Impact** | > $1,000/day at risk | $100-$1,000/day impact | < $100/day impact |
| **Data Loss** | Tracking broken, losing data | Partial data gap | No data impact |
| **Client Visibility** | Client has noticed or asked | Client will see in next report | Client unlikely to notice |
| **Reversibility** | Damage grows over time | Stable situation | No ongoing damage |
| **Scope** | Affects all campaigns or accounts | Affects specific campaigns | Affects minor elements |

---

## Signaling in Different Contexts

### In Slack/Chat
- P0: Use channel alerts, tag relevant people, use "URGENT" prefix
- P1: Tag the owner directly, set a clear deadline
- P2: Post in relevant channel, no tag unless specifically needed
- P3: Add to task list or weekly planning thread

### In Reports
- P0/P1: Lead the report with this issue before any other content
- P2: Include in recommendations section with standard formatting
- P3: Include in "future considerations" or appendix

### In Emails
- P0: Subject line starts with "[URGENT]" -- send immediately
- P1: Subject line starts with "[Action Needed]" -- send within business hours
- P2: Include in regular update cadence
- P3: Include as a note or appendix in regular communications

### In Meetings
- P0: Interrupt current agenda to address
- P1: First item on the agenda
- P2: Standard agenda item
- P3: "If time allows" or "parking lot"

---

## Preventing Priority Inflation

### Rules
1. Not everything is P1. If everything is urgent, nothing is urgent.
2. P0 should occur less than once per month per account.
3. P1 should be 1-3 items per week maximum.
4. Most work should be P2.
5. Regularly move resolved items off the priority list.

### Red Flags for Priority Inflation
- More than 3 P1 items simultaneously
- P0 used for non-emergency situations
- Team unable to complete P2 items because of constant P1 escalation
- Everything labeled "urgent" or "ASAP"
