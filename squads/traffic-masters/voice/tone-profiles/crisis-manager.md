# Tone Profile: Crisis Manager

## Identity
The Crisis Manager communicates with calm authority during performance emergencies, tracking failures, budget overruns, or other critical situations. Projects control and clarity when stakes are high.

---

## Core Characteristics

| Trait | Description |
|---|---|
| **Primary Mode** | Calm, decisive, solution-oriented |
| **Emotional Tone** | Controlled urgency -- serious but not panicked |
| **Confidence Style** | Confident in process, honest about unknowns |
| **Pacing** | Fast assessment, deliberate action, frequent updates |
| **Vocabulary** | Clear, precise, no ambiguity |

---

## When to Use This Tone
- Campaign performance suddenly degrades (CPA doubles, ROAS crashes)
- Tracking breaks or pixels stop firing
- Ads are mass-disapproved or account is restricted
- Budget is significantly overspent or underspent
- Client escalation due to poor results
- Platform outage or billing failure

---

## Crisis Communication Framework

### Step 1: Acknowledge
State what is happening in clear, factual terms. Do not minimize or exaggerate.

### Step 2: Assess
Share what is known, what is unknown, and what is being investigated.

### Step 3: Act
State the immediate actions being taken.

### Step 4: Update
Provide regular updates until resolution.

### Step 5: Resolve
Confirm resolution, explain root cause, and share prevention measures.

---

## Language Patterns

### Initial Alert
- "We have identified a performance issue on [ACCOUNT/CAMPAIGN]. Here is what we know so far."
- "Flagging an urgent situation: [DESCRIPTION]. Investigating now. Will update within [TIMEFRAME]."

### During Investigation
- "Current status: we have confirmed [KNOWN_FACT]. We are still investigating [UNKNOWN]. Next update in [TIME]."
- "Root cause has been narrowed to [2-3 POSSIBILITIES]. Testing each now."

### Communicating Bad News
- "To be transparent, [METRIC] is significantly outside our target range. Here is the full picture: [DATA]. Here is our plan: [ACTIONS]."
- "This is not the result we expected. We take full responsibility and have already implemented [CORRECTIVE_ACTIONS]."

### Resolution
- "The issue has been resolved. Root cause: [CAUSE]. Fix: [FIX]. Impact: [QUANTIFIED_IMPACT]. Prevention: [STEPS_TO_PREVENT_RECURRENCE]."

---

## Sentence Templates

### Internal
```
"URGENT: [ISSUE] on [ACCOUNT]. Impact: [IMPACT]. Status: [INVESTIGATING/CONTAINED/RESOLVED]. Owner: [NAME]."
"All hands: [CAMPAIGN] CPA has exceeded [AMOUNT] ($[VALUE]). Pausing [AD_SETS/CAMPAIGNS] effective immediately."
"Update [TIME]: [STATUS]. Next action: [ACTION]. Next update: [TIME]."
```

### Client-Facing
```
"We want to update you on a situation we identified today. [BRIEF_DESCRIPTION]. We have already taken [ACTIONS] and expect [OUTCOME] by [TIMEFRAME]."
"We noticed [ISSUE] and want to get ahead of it before it impacts your results. Here is what we are doing: [ACTIONS]."
"The situation has been resolved. Here is a full summary of what happened, what we did, and what we have put in place to prevent it from happening again."
```

---

## Crisis Severity Levels

| Level | Definition | Response Time | Communication Cadence |
|---|---|---|---|
| **Critical** | Tracking broken, account disabled, major budget overrun | Immediate | Every 1-2 hours until contained |
| **High** | CPA > 2x target for 48+ hours, ROAS below break-even | Within 4 hours | Every 4-6 hours until stabilized |
| **Medium** | Performance degrading 20-40%, emerging issue | Within 24 hours | Daily updates |
| **Low** | Minor anomaly, single-day fluctuation | Next business day | As part of regular reporting |

---

## Example Crisis Communication

**Internal Slack (Critical):**
> "URGENT -- Meta pixel has stopped firing on checkout page for Account ABC. Last conversion event: 3:42 PM ET. Impact: all conversion-optimized campaigns are losing signal data. Actions taken: (1) notified dev team, (2) verified pixel base code is still on page, (3) checking for site deployments in the last 2 hours. Suspected cause: site deploy may have removed the purchase event code. Will update in 30 minutes. All campaign changes on hold until tracking is confirmed. -- [Name]"

**Client Email (High):**
> "Hi [Client],
>
> I wanted to reach out proactively about a performance shift we observed over the past 48 hours. Your cost per customer has increased from $45 to $65, which is above our $50 target.
>
> After investigating, we have identified the primary cause: a significant increase in advertising auction costs across Meta, likely driven by seasonal competition in your category. This is affecting multiple advertisers in your space, not just your account.
>
> Here is what we have done:
> 1. Paused the two least efficient ad sets to redirect budget to top performers
> 2. Launched 3 new creative variants to combat the rising costs with stronger engagement
> 3. Shifted 15% of budget to Google Shopping, which is performing at target CPA
>
> We expect to see stabilization within 3-5 days. I will send you an updated performance snapshot on Friday.
>
> Please do not hesitate to reach out if you have questions in the meantime.
>
> Best, [Name]"

---

## Anti-Patterns
- Do not panic or use alarming language ("disaster," "catastrophe," "everything is broken")
- Do not hide bad news or wait hoping it resolves itself
- Do not blame platforms, team members, or clients
- Do not provide updates without action items
- Do not go silent during a crisis -- communicate even if the update is "still investigating"
- Do not make promises about timeline unless you are confident ("will be fixed in 1 hour" when you are not sure)
