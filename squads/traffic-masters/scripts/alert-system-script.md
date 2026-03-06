# Alert System Script — Automation Script

> Performance alert system setup and management for proactive issue detection.

---

## Purpose

Establish and maintain a performance alert system that detects anomalies, threshold breaches, and critical issues before they significantly impact campaign performance or waste budget.

---

## Trigger / Schedule

- **Setup trigger:** Account onboarding or alert system review
- **Monitoring:** Continuous (alerts fire when conditions are met)
- **Review trigger:** Monthly (alert effectiveness review)
- **Duration:** 30 minutes for initial setup, 15 minutes for monthly review
- **Owner:** Optimization Agent
- **Supporting Agents:** Diagnostics Agent, Tracking Agent

---

## Pre-Conditions

- [ ] Config.yaml thresholds section configured
- [ ] Access to ad platform notification settings
- [ ] Notification delivery channels established (email, Slack, dashboard)
- [ ] KPI targets and baselines documented
- [ ] Alert response protocol defined

---

## Step-by-Step Workflow

### Step 1: Define Alert Categories (10 minutes)

```yaml
action: Establish alert categories and severity levels
categories:
  performance_alerts:
    description: "KPI threshold breaches"
    severity: "Varies by metric and magnitude"
  budget_alerts:
    description: "Spend pacing anomalies"
    severity: "Medium to High"
  delivery_alerts:
    description: "Campaign delivery issues"
    severity: "High to Critical"
  tracking_alerts:
    description: "Data integrity issues"
    severity: "Critical"
  policy_alerts:
    description: "Ad disapprovals and account restrictions"
    severity: "High"
  creative_alerts:
    description: "Creative fatigue indicators"
    severity: "Medium"

severity_levels:
  critical:
    response_time: "< 1 hour"
    description: "Active revenue loss, broken tracking, account suspension"
    notification: "Immediate push notification + email"
  high:
    response_time: "< 4 hours"
    description: "Significant performance decline, delivery failure"
    notification: "Email + dashboard flag"
  medium:
    response_time: "< 24 hours"
    description: "Efficiency decline, pacing issues, fatigue"
    notification: "Dashboard flag, include in daily check"
  low:
    response_time: "< 48 hours"
    description: "Minor variance, informational"
    notification: "Dashboard flag only"
```

### Step 2: Configure Performance Alerts (10 minutes)

```yaml
action: Set up KPI threshold alerts
alerts:
  cpa_spike:
    metric: "cost_per_acquisition"
    condition: "CPA > target * 1.25 for 3 consecutive days"
    severity: "high"
    message: "CPA has exceeded target by 25%+ for 3 days on [campaign]"
    action: "Investigate creative fatigue, audience saturation, tracking issues"

  roas_drop:
    metric: "return_on_ad_spend"
    condition: "ROAS < target * 0.80 for 3 consecutive days"
    severity: "high"
    message: "ROAS has dropped below 80% of target for 3 days on [campaign]"
    action: "Review conversion volume, revenue per conversion, traffic quality"

  ctr_decline:
    metric: "click_through_rate"
    condition: "CTR < 7-day average * 0.70"
    severity: "medium"
    message: "CTR has declined 30%+ from recent average on [creative/campaign]"
    action: "Check creative fatigue, audience overlap, competitive pressure"

  conversion_drop:
    metric: "conversion_count"
    condition: "Daily conversions < 7-day average * 0.50"
    severity: "critical"
    message: "Conversion volume dropped 50%+ from average"
    action: "Immediate investigation: tracking, landing page, platform issues"

  cpc_spike:
    metric: "cost_per_click"
    condition: "CPC > 7-day average * 1.50"
    severity: "medium"
    message: "CPC spiked 50%+ above average"
    action: "Check auction competition, quality score, bid strategy"
```

### Step 3: Configure Budget Alerts (5 minutes)

```yaml
action: Set up budget pacing and spending alerts
alerts:
  overspend:
    condition: "Daily spend > daily budget * 1.20"
    severity: "medium"
    message: "Campaign [name] overspent daily budget by [%]"
    action: "Check campaign spending limits, adjust budget if needed"

  underspend:
    condition: "Daily spend < daily budget * 0.70 for 2+ days"
    severity: "medium"
    message: "Campaign [name] is significantly underspending"
    action: "Check bid caps, audience size, ad relevance, delivery status"

  monthly_pacing:
    condition: "Projected monthly spend > monthly budget * 1.10 OR < monthly budget * 0.85"
    severity: "high"
    message: "Monthly pacing is off track: projected [%] of budget"
    action: "Adjust daily budgets to correct pacing"

  spending_limit_approaching:
    condition: "Cumulative spend > spending_limit * 0.90"
    severity: "medium"
    message: "Campaign approaching spending limit ([%] consumed)"
    action: "Review if spending limit should be increased or if campaign should pause"
```

### Step 4: Configure Delivery and Policy Alerts (5 minutes)

```yaml
action: Set up delivery and policy alerts
alerts:
  no_delivery:
    condition: "Zero impressions for 4+ hours during active schedule"
    severity: "critical"
    message: "Campaign [name] has stopped delivering"
    action: "Check ad review status, budget, payment, account status"

  ad_disapproval:
    condition: "Any ad disapproved"
    severity: "high"
    message: "[X] ads disapproved on [account/campaign]"
    action: "Review policy violation, fix or appeal, check for pattern"

  account_restriction:
    condition: "Account status changes from active"
    severity: "critical"
    message: "Account [ID] status changed to [new status]"
    action: "Contact platform support immediately"

  learning_phase_extended:
    condition: "Campaign in learning phase > 7 days"
    severity: "low"
    message: "Campaign [name] still in learning phase after 7 days"
    action: "Review conversion volume, consider consolidation"
```

### Step 5: Configure Tracking Alerts (5 minutes)

```yaml
action: Set up data integrity alerts
alerts:
  conversion_zero:
    condition: "Zero conversions reported for 24+ hours on a campaign with historical daily conversions"
    severity: "critical"
    message: "No conversions recorded in 24 hours on [campaign] - possible tracking failure"
    action: "Verify pixel/CAPI, check landing page, test conversion event"

  discrepancy_spike:
    condition: "Platform vs. analytics discrepancy > 40% (7-day window)"
    severity: "high"
    message: "Data discrepancy between [platform] and analytics exceeded 40%"
    action: "Audit tracking implementation, check for broken events"

  pixel_error:
    condition: "Platform reports pixel error or warning"
    severity: "high"
    message: "Pixel health warning detected on [account]"
    action: "Check pixel diagnostics in platform event manager"
```

### Step 6: Alert Response Protocol (reference)

```yaml
action: Define response process for each alert severity
protocol:
  critical:
    1: "Acknowledge alert within 15 minutes"
    2: "Begin investigation immediately"
    3: "Notify stakeholders if campaign pause is needed"
    4: "Implement fix or mitigation"
    5: "Document in incident log"
    6: "Post-incident review within 48 hours"
  high:
    1: "Acknowledge alert within 1 hour"
    2: "Investigate during current work session"
    3: "Implement fix or plan remediation"
    4: "Document in optimization log"
  medium:
    1: "Review during daily check routine"
    2: "Address during next optimization cycle"
    3: "Document in optimization log"
  low:
    1: "Note in daily status"
    2: "Address when capacity allows"
    3: "Monitor for escalation"
```

### Step 7: Monthly Alert Review (15 minutes, monthly)

```yaml
action: Review alert system effectiveness
review:
  - Total alerts fired by category and severity
  - False positive rate (alerts that didn't indicate real issues)
  - Missed issues (problems that should have triggered alerts but didn't)
  - Average response time by severity
  - Threshold appropriateness (too sensitive or not sensitive enough)
adjustments:
  - Tighten thresholds that are missing real issues
  - Loosen thresholds that are generating too many false positives
  - Add new alert types for issues that were missed
  - Remove or modify alerts that are not providing value
  - Update config.yaml with revised thresholds
```

---

## Output / Deliverables

- Configured alert rules across all platforms
- Alert response protocol documentation
- Monthly alert effectiveness report
- Updated thresholds in config.yaml
- Alert log for auditing and review

---

## Post-Conditions

- [ ] All alert categories configured and active
- [ ] Response protocol documented and shared with team
- [ ] Notification channels tested and working
- [ ] Thresholds calibrated to account-specific baselines
- [ ] Monthly review cadence scheduled
