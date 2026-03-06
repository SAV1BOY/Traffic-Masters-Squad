# Audience Refresh Script — Automation Script

> Audience refresh and update automation for maintaining audience quality and relevance.

---

## Purpose

Systematically review, refresh, and optimize audience segments to prevent saturation, maintain targeting quality, and ensure exclusion lists are current. Audience freshness directly impacts campaign efficiency.

---

## Trigger / Schedule

- **Scheduled trigger:** Monthly (first week of each month)
- **Alert trigger:** Audience frequency exceeds threshold, audience size drops below minimum
- **Event trigger:** Significant CRM data update, new customer segment identified
- **Duration:** 30-60 minutes per account
- **Owner:** Audience Agent
- **Supporting Agents:** Optimization Agent, Tracking Agent

---

## Pre-Conditions

- [ ] Audience registry is current
- [ ] Platform audience tools accessible
- [ ] CRM / customer data available and recent
- [ ] Audience overlap data available
- [ ] Performance data by audience segment available

---

## Step-by-Step Workflow

### Step 1: Audience Performance Review (15 minutes)

```yaml
action: Evaluate performance of all active audience segments
for_each_audience:
  metrics:
    - CPA / ROAS for the last 30 days
    - Frequency (average times served per user)
    - Reach vs. estimated audience size (saturation %)
    - Cost trend (increasing, stable, decreasing)
    - Conversion volume
  classify:
    high_performing: "CPA below target, low frequency, growing reach"
    stable: "CPA near target, moderate frequency"
    saturated: "Frequency > threshold, reach stagnant, CPA rising"
    underperforming: "CPA > 1.3x target, declining metrics"
output: Audience performance report with classification
```

### Step 2: Exclusion List Update (10 minutes)

```yaml
action: Update all exclusion audiences
update:
  recent_converters:
    source: "Last 30 days of conversion data"
    action: "Rebuild custom audience from recent converters"
    purpose: "Prevent serving acquisition ads to new customers"
  existing_customers:
    source: "CRM customer list (full)"
    action: "Upload updated customer list"
    purpose: "Exclude from prospecting campaigns"
  disqualified_leads:
    source: "CRM disqualified/rejected leads"
    action: "Upload exclusion list"
    purpose: "Stop spending on users who won't convert"
  employees_internal:
    source: "Company email domain list"
    action: "Maintain internal exclusion"
    purpose: "Prevent serving ads to internal teams"
verification:
  - Confirm exclusions are applied to all relevant campaigns
  - Verify exclusion audience sizes are reasonable
  - Check that no exclusion accidentally blocks valid prospects
```

### Step 3: Seed Audience Refresh (10 minutes)

```yaml
action: Update seed audiences used for lookalike generation
for_each_lookalike_seed:
  evaluate:
    - When was the seed last updated?
    - Has the customer profile changed significantly?
    - Is the seed using the most valuable customer segment?
  refresh_criteria:
    - Seed older than 30 days: refresh with latest data
    - Customer profile shift detected: rebuild seed
    - Seed performance declining: test alternative seed
  refresh_actions:
    - Export latest high-value customers from CRM
    - Upload new seed audience to platform
    - Rebuild lookalike audiences from new seed
    - Phase in new lookalikes while monitoring performance
  recommended_seeds:
    - Purchasers (last 180 days)
    - High-LTV customers (top 25%)
    - Repeat purchasers
    - High-engagement website visitors
```

### Step 4: Audience Overlap Analysis (10 minutes)

```yaml
action: Check for significant overlap between active audiences
analysis:
  for_each_audience_pair:
    - Calculate overlap percentage
    - Flag pairs with > 30% overlap
  remediation:
    high_overlap_options:
      - Consolidate overlapping audiences into one ad set
      - Apply mutual exclusions to eliminate overlap
      - Restructure campaign to separate audiences cleanly
    priority:
      - Address overlaps that are causing auction self-competition
      - Prioritize overlaps between highest-spend ad sets
output: Overlap report with remediation actions
```

### Step 5: Audience Expansion Assessment (10 minutes)

```yaml
action: Identify opportunities to expand or test new audiences
assessment:
  current_audiences:
    - Are high-performing audiences nearing saturation?
    - Is there headroom to scale existing audiences?
  new_opportunities:
    - Test broader lookalike percentages (if 1% works, test 3%)
    - Test interest-based audiences identified from customer research
    - Test broad/open targeting to leverage platform algorithms
    - Test engagement-based audiences (video viewers, page engagers)
  recommendations:
    - Prioritize by expected impact and testing cost
    - Brief 1-2 new audience tests per month
    - Ensure new audiences don't overlap with existing ones
```

### Step 6: Registry Updates (5 minutes)

```yaml
action: Update audience registry and documentation
updates:
  audience_registry:
    - Update status for all reviewed audiences
    - Add new audiences created
    - Update last_refreshed dates
    - Archive audiences that have been paused/retired
  decisions_log:
    - Log all audience changes with rationale
  optimization_log:
    - Note audience-related optimizations
```

---

## Decision Points

| Condition | Action |
|-----------|--------|
| Audience frequency > 5.0 | Reduce budget or expand audience |
| Audience CPA > 1.5x target for 14+ days | Pause and test alternative audiences |
| Seed audience older than 60 days | Refresh immediately |
| Overlap > 30% between ad sets | Consolidate or apply mutual exclusions |
| All audiences saturated | Test new audience types, consider new channels |
| CRM data significantly updated | Trigger unscheduled audience refresh |

---

## Output / Deliverables

- Audience performance report with classifications
- Updated exclusion lists
- Refreshed seed/lookalike audiences
- Overlap analysis with remediation plan
- Expansion recommendations
- Updated audience registry

---

## Post-Conditions

- [ ] All audiences reviewed and classified
- [ ] Exclusion lists updated with latest data
- [ ] Seed audiences refreshed (if older than 30 days)
- [ ] High-overlap audiences addressed
- [ ] New audience test recommendations documented
- [ ] Audience registry updated
- [ ] Next refresh scheduled
