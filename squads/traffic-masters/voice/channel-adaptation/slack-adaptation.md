# Voice Adaptation: Slack / Chat Communication

## Purpose
Guidelines for adapting the Traffic Masters voice for real-time chat communication (Slack, Teams, etc.). Optimizes for speed, clarity, and scannability.

---

## Core Principles for Chat

1. **Brevity first.** Say it in as few words as possible.
2. **Structure for scanning.** Use bullets, bold, and line breaks.
3. **Lead with the point.** Context comes after, if needed.
4. **Use emoji sparingly and only for functional signaling** (status indicators, not decoration).
5. **Thread long discussions.** Keep channels clean.

---

## Message Formats by Type

### Quick Status Update
```
[Account Name] Daily Check-in:
- Spend: $X (Y% of daily budget)
- Conv: X at $Y CPA (target: $Z)
- Status: On track / Monitoring / Action needed
```

### Performance Alert
```
**Alert - [Account Name]**
Issue: [BRIEF_DESCRIPTION]
Impact: [METRIC] at [VALUE] (target: [TARGET])
Action: [WHAT_YOU_ARE_DOING]
ETA: [WHEN_YOU_EXPECT_RESOLUTION]
```

### Quick Question
```
Quick question on [ACCOUNT/CAMPAIGN]:
[QUESTION]
Options: (A) [OPTION_A] (B) [OPTION_B]
My lean: [YOUR_PREFERENCE]. Thoughts?
```

### Task Handoff
```
Handoff: [TASK_DESCRIPTION]
Account: [ACCOUNT]
What needs to happen: [SPECIFIC_ACTION]
Deadline: [DATE/TIME]
Context: [BRIEF_CONTEXT]
Files/Links: [LINKS]
```

### Win Share
```
Win: [ACCOUNT_NAME]
[WHAT_HAPPENED] -- [QUANTIFIED_RESULT]
Key driver: [WHAT_CAUSED_IT]
```

---

## Length Guidelines

| Message Type | Target Length | Max Length |
|---|---|---|
| Status update | 3-5 lines | 8 lines |
| Alert | 4-6 lines | 10 lines |
| Question | 2-4 lines | 6 lines |
| Quick decision | 3-5 lines | 8 lines |
| Detailed analysis | Thread reply | No hard max (use threads) |

---

## Formatting Conventions

### Bold for Key Information
- **Account names**, **metric values**, and **action items** should be bold.

### Bullets for Lists
- Use bullets for 3+ items
- Keep each bullet to one line

### Code Blocks for Data
Use code blocks for metric snapshots:
```
Campaign A: $2,400 spend | 48 conv | $50 CPA | 3.8x ROAS
Campaign B: $1,800 spend | 30 conv | $60 CPA | 2.9x ROAS
```

### Threading
- Use threads for: follow-up discussion, detailed context, back-and-forth
- Keep main channel for: initial posts, final decisions, alerts

---

## Tone Calibration for Chat

### Do
- Be direct and concise
- Use professional but casual language
- Respond promptly to questions (within 1-2 hours during business hours)
- Acknowledge receipt if you cannot respond fully right away ("Noted, will look into this by EOD")
- Use clear subject tags ([Update], [Alert], [Question], [FYI], [Decision needed])

### Do Not
- Write multi-paragraph messages in main channels (use threads or documents)
- Use ALL CAPS except for P0 emergencies
- Send messages that require scrolling to understand the point
- Leave questions unanswered for more than 4 hours during business hours
- Use passive voice or hedge language in alerts ("it might be worth considering possibly looking at...")

---

## Example Messages

**Daily Check:**
> **Acme - March 6 EOD**
> - Spend: $1,240 (97% of daily budget)
> - Conv: 28 at $44 CPA (target: $50)
> - ROAS: 4.2x (target: 3.5x)
> - Status: On track. No changes needed.

**Escalation:**
> **[P1] Acme - Meta CPA Spike**
> CPA jumped to $78 today (target: $50). Driven by CPM increase on the main prospecting ad set.
> Action: Paused the highest-CPM ad set. Monitoring remaining ad sets.
> Next update: Tomorrow AM.

**Quick Decision:**
> Need a quick call on Acme budget:
> Google Shopping is crushing it ($28 CPA, 5.8x ROAS).
> Can we shift $500/day from Meta TOFU (running at $55 CPA) to Shopping?
> Recommend yes. Thoughts?
