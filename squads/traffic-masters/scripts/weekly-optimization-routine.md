# Weekly Optimization Routine — Automation Script

> Systematic weekly workflow for optimizing all active campaigns across accounts.

---

## Purpose

Perform a thorough weekly optimization cycle covering bid adjustments, budget reallocation, audience review, creative health assessment, and test monitoring. This is the primary optimization cadence.

---

## Trigger / Schedule

- **Schedule:** Every Monday (or first business day of the week)
- **Recommended time:** 10:00 local timezone
- **Duration:** 1-2 hours per account
- **Owner:** Optimization Agent
- **Supporting Agents:** Budget Agent, Creative Strategist Agent, Audience Agent

---

## Pre-Conditions

- [ ] Previous week's data fully reported (allow 24-48h for platform lag)
- [ ] Daily check routine completed for Monday
- [ ] Weekly Optimization Checklist available
- [ ] KPI targets current in config.yaml
- [ ] Previous week's optimization log reviewed

---

## Step-by-Step Workflow

### Step 1: Performance Review (15 minutes per account)

```yaml
action: Compile and review 7-day performance
metrics:
  account_level:
    - Total spend, impressions, clicks, conversions
    - Blended CPA, ROAS, CTR, CPC
    - Week-over-week comparison
    - Performance vs. targets
  campaign_level:
    - Sort by primary KPI (best to worst)
    - Identify top 3 and bottom 3 performers
    - Flag campaigns outside target thresholds
  ad_set_level:
    - Identify saturated ad sets (frequency > threshold)
    - Check learning phase status
    - Review audience performance
output: Performance summary with flagged items
```

### Step 2: Budget Optimization (15 minutes per account)

```yaml
action: Review and optimize budget allocation
checks:
  - Budget utilization last 7 days (target: 85-105%)
  - Marginal CPA/ROAS by campaign
  - Campaigns limited by budget vs. those underspending
  - Pacing accuracy vs. weekly/monthly plan
actions:
  - Reallocate from underperformers to top performers
  - Increase budget on campaigns below CPA target with headroom
  - Decrease budget on campaigns above CPA target
  - Ensure reallocation follows Budget Change Checklist for changes > 20%
rules:
  - Maximum single budget change: 20-30%
  - Do not change budgets on campaigns in learning phase
  - Document all changes with rationale
```

### Step 3: Bid Strategy Review (10 minutes per account)

```yaml
action: Evaluate bid strategy performance
checks:
  - Current bid strategy effectiveness
  - Learning phase completion status
  - Cost cap / bid cap hit rates
  - Auction competition indicators (CPM trends)
actions:
  - Adjust cost caps that are too restrictive (underspending)
  - Tighten cost caps on overspending campaigns
  - Consider strategy changes for underperforming campaigns
  - Allow newly changed strategies at least 7 days before re-evaluating
```

### Step 4: Creative Health Assessment (15 minutes per account)

```yaml
action: Review creative performance and fatigue
checks:
  - CTR trend by creative (declining = potential fatigue)
  - Frequency by ad set
  - Days running per creative
  - Ad relevance / quality diagnostics
  - Creative diversity assessment (formats, hooks, angles)
actions:
  - Flag creatives showing fatigue (CTR down 20%+ from peak)
  - Pause creatives below minimum CTR threshold after sufficient spend
  - Initiate creative refresh if > 50% of creatives show fatigue
  - Brief new creative variations for next week
decision:
  fatigue_widespread:
    yes: "Trigger Creative Refresh Workflow"
    no: "Note findings, continue monitoring"
```

### Step 5: Audience Review (10 minutes per account)

```yaml
action: Evaluate audience health and performance
checks:
  - Audience-level CPA/ROAS comparison
  - Frequency by audience segment
  - Audience overlap between ad sets (threshold: 30%)
  - Retargeting window effectiveness
  - Exclusion list currency
actions:
  - Reduce budget on saturated audiences
  - Expand or refresh high-performing audiences
  - Update exclusion lists with recent converters
  - Consolidate overlapping audiences
  - Test new audience segments if current ones are saturated
```

### Step 6: Search Term / Keyword Review (Google/Bing only, 10 minutes)

```yaml
action: Review search terms and keyword performance
checks:
  - Search term report for irrelevant queries
  - Keyword-level CPA/ROAS
  - Quality Score changes
  - Impression share and competitive metrics
actions:
  - Add negative keywords for irrelevant search terms
  - Pause keywords with CPA > 2x target and > $200 spend
  - Adjust bids on high-performing keywords
  - Test new keyword opportunities identified
```

### Step 7: Test Monitoring (5 minutes per active test)

```yaml
action: Check status of active A/B tests
checks:
  - Sample size progress (% of target reached)
  - Estimated completion date
  - Early directional signals (not for decision-making)
  - Test integrity (no contamination, proper isolation)
actions:
  - Document progress
  - Flag tests approaching completion for analysis
  - Extend duration if sample pace is slower than expected
  - Flag any tests with integrity issues
rules:
  - Do NOT make decisions on incomplete test data
  - Do NOT modify test campaigns during the test period
```

### Step 8: Documentation & Planning (10 minutes)

```yaml
action: Document all changes and plan for next week
document:
  - All optimization actions taken with rationale
  - Performance trends and notable observations
  - Issues flagged for escalation
  - Creative requests submitted
  - Test status updates
plan:
  - Priority actions for daily checks this week
  - Upcoming test completions to analyze
  - Creative deliverables expected
  - Budget changes planned for mid-week (if any)
```

---

## Decision Points

| Condition | Action |
|-----------|--------|
| Campaign CPA > 1.5x target for 7+ days | Major intervention: restructure, new creative, or pause |
| Creative fatigue across > 50% of ads | Trigger Creative Refresh Workflow |
| Audience frequency > 5.0 | Expand targeting or rotate audiences |
| Budget utilization < 70% | Investigate bid caps, audience size, ad relevance |
| Test completed with significance | Analyze, declare winner, implement, document |
| Competitor surge detected | Brief Intelligence Agent for competitive analysis |

---

## Output / Deliverables

- Weekly optimization log with all actions and rationale
- Updated campaign settings (budgets, bids, paused ads)
- Creative refresh brief (if needed)
- Updated exclusion lists and negative keywords
- Test status report
- Weekly status summary for stakeholders

---

## Post-Conditions

- [ ] All active campaigns reviewed and optimized
- [ ] Budget reallocation implemented (if applicable)
- [ ] Underperforming ads paused
- [ ] Exclusion lists updated
- [ ] Optimization log completed
- [ ] Creative refresh initiated (if needed)
- [ ] Test status documented
- [ ] Weekly status shared with stakeholders
