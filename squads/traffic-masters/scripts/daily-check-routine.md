# Daily Check Routine — Automation Script

> Morning monitoring routine for campaign health checks across all active accounts.

---

## Purpose

Perform a systematic daily review of all active campaigns to identify anomalies, catch issues early, and implement quick wins before they compound. This routine is the first line of defense against performance degradation.

---

## Trigger / Schedule

- **Schedule:** Every business day, within 1 hour of business start
- **Recommended time:** 09:00 local timezone
- **Duration:** 30-60 minutes per account
- **Owner:** Optimization Agent

---

## Pre-Conditions

- [ ] Access to all active ad platform accounts
- [ ] Access to analytics dashboard
- [ ] Previous day's data has fully reported (check platform reporting lag)
- [ ] Alert notification queue reviewed
- [ ] Config.yaml thresholds are current

---

## Step-by-Step Workflow

### Step 1: Review Overnight Alerts (5 minutes)

```yaml
action: Check alert queue
check_items:
  - Performance alerts triggered overnight
  - Budget pacing alerts
  - Ad disapproval notifications
  - Platform policy notifications
  - Account status changes
decision:
  critical_alerts_found:
    yes: "Address critical alerts immediately before continuing routine"
    no: "Proceed to Step 2"
```

### Step 2: Account-Level Health Check (5 minutes per account)

```yaml
action: Review account-level metrics for last 24 hours
metrics_to_check:
  - Total spend vs. daily target (threshold: +/- 20%)
  - Total conversions vs. daily average (threshold: +/- 25%)
  - Blended CPA vs. target (threshold: +25%)
  - Blended ROAS vs. target (threshold: -20%)
  - Account delivery status (active, limited, error)
comparison: Compare today vs. 7-day average and vs. same day last week
decision:
  anomaly_detected:
    yes: "Flag for investigation in Step 3"
    no: "Proceed to campaign-level review"
```

### Step 3: Campaign-Level Review (10 minutes per account)

```yaml
action: Review each active campaign
for_each_campaign:
  check:
    - Spend pacing (on track, over, under)
    - CPA/ROAS vs. target
    - Delivery status (learning, active, limited)
    - Any ads disapproved or under review
  flag_if:
    - CPA > 1.3x target for 2+ consecutive days
    - ROAS < 0.8x target for 2+ consecutive days
    - Spend pacing < 70% or > 130% of daily target
    - Campaign in learning phase for > 7 days
    - Any ad disapproved
decision:
  flagged_campaigns:
    critical: "Investigate immediately"
    warning: "Add to investigation queue for weekly optimization"
    healthy: "No action needed"
```

### Step 4: Quick Win Identification (5 minutes per account)

```yaml
action: Identify low-risk, high-impact optimizations
quick_win_types:
  - Pause ads with CPA > 2x target and > $100 spend
  - Pause ads with CTR < 0.3% and > 5,000 impressions
  - Add obvious negative keywords (Google/Bing)
  - Refresh exclusion lists if recently converted users are being served
  - Adjust dayparting if clear time-of-day performance patterns exist
rules:
  - Only implement changes that are clearly beneficial
  - Do not make changes to campaigns in learning phase
  - Do not make changes that affect test integrity
  - Log all actions taken
```

### Step 5: Landing Page Quick Check (3 minutes)

```yaml
action: Verify key landing pages are functional
check:
  - Primary landing pages load without errors
  - Forms are submitting correctly
  - Page load speed is within acceptable range
  - No unexpected content changes
decision:
  issues_found:
    yes: "Escalate to tracking/web team immediately"
    no: "Proceed to documentation"
```

### Step 6: Documentation (5 minutes)

```yaml
action: Document daily check findings
record:
  - Date and time of review
  - Accounts reviewed
  - Anomalies detected (if any)
  - Quick wins implemented (if any)
  - Issues flagged for follow-up
  - Escalations made (if any)
output_location: "Optimization log / daily status notes"
```

---

## Decision Points

| Condition | Action |
|-----------|--------|
| Critical alert (broken tracking, account suspension) | Stop routine, address immediately |
| CPA > 1.5x target for 3+ days | Trigger Performance Recovery Workflow |
| Single ad underperforming | Pause and note for creative rotation |
| Budget severely over-pacing | Reduce daily budget or set spending limit |
| Budget severely under-pacing | Check bid caps, audience size, ad relevance |
| Landing page down | Pause affected campaigns, notify web team |

---

## Output / Deliverables

- Daily status summary (internal communication)
- Optimization log entries for any actions taken
- Escalation tickets for critical issues
- Flagged items for weekly optimization cycle

---

## Post-Conditions

- [ ] All active accounts reviewed
- [ ] All alerts addressed or escalated
- [ ] Quick wins implemented and logged
- [ ] Critical issues escalated with appropriate urgency
- [ ] Daily status summary shared with team
- [ ] Items flagged for weekly optimization cycle
