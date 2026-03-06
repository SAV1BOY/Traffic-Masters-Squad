# Monthly Reporting Routine — Automation Script

> End-of-month reporting generation workflow for comprehensive performance documentation.

---

## Purpose

Generate a thorough monthly performance report covering all active accounts, campaigns, and channels. This report serves as the primary stakeholder communication for monthly performance.

---

## Trigger / Schedule

- **Schedule:** 3rd business day of each month
- **Duration:** 2-4 hours per account
- **Owner:** Reporting Agent
- **Supporting Agents:** Diagnostics Agent, Strategy Agent

---

## Pre-Conditions

- [ ] Full month of data has reported (allow 48-72h after month end for platform lag)
- [ ] All weekly optimization logs for the month are complete
- [ ] Previous month's report is available for comparison
- [ ] KPI targets for the month are documented
- [ ] Monthly Performance Report template is available

---

## Step-by-Step Workflow

### Step 1: Data Collection (30 minutes per account)

```yaml
action: Gather all performance data for the reporting period
sources:
  - Ad platform dashboards (Meta, Google, TikTok, etc.)
  - Google Analytics / analytics platform
  - CRM / conversion data
  - Budget tracking sheets
data_points:
  - Spend by campaign, channel, and total
  - Impressions, reach, frequency
  - Clicks, CTR, CPC
  - Conversions, CPA, conversion rate
  - Revenue, ROAS (if applicable)
  - Audience metrics (size, overlap, saturation)
  - Creative metrics (performance by asset)
validation:
  - Cross-check platform data vs. analytics data
  - Document any discrepancies and note the cause
  - Verify currency and date range consistency
```

### Step 2: Performance Analysis (45 minutes per account)

```yaml
action: Analyze performance across all dimensions
analyses:
  month_over_month:
    - Compare all primary KPIs to previous month
    - Calculate percentage change
    - Identify significant improvements and declines
  vs_targets:
    - Compare actuals to monthly targets
    - Calculate target attainment percentage
    - Classify each KPI as above/on/below target
  trend_analysis:
    - Review 3-month trends for primary KPIs
    - Identify sustained trends vs. one-time fluctuations
    - Note seasonal context
  campaign_analysis:
    - Rank campaigns by primary KPI
    - Identify top 3 and bottom 3 performers
    - Root cause analysis for underperformers
  channel_analysis:
    - Compare channel-level efficiency
    - Calculate channel contribution percentages
    - Assess cross-channel synergies
  audience_analysis:
    - Performance by audience segment
    - Audience health indicators
    - Expansion and contraction recommendations
  creative_analysis:
    - Performance by creative format, hook, and angle
    - Creative lifecycle status (new, peak, fatigued, retired)
    - Top-performing creative identification
```

### Step 3: Report Generation (45 minutes per account)

```yaml
action: Compile report using Monthly Performance Report template
sections:
  1_executive_summary:
    content: "3-5 sentence overview of monthly performance"
    include: "Key wins, key concerns, overall trajectory"
  2_kpi_dashboard:
    content: "Table of all KPIs vs. targets and prior period"
    format: "Metric | This Month | Last Month | MoM Change | Target | Status"
  3_channel_performance:
    content: "Platform-by-platform breakdown"
  4_campaign_performance:
    content: "Campaign-level analysis with commentary"
  5_audience_performance:
    content: "Segment-level performance comparison"
  6_creative_performance:
    content: "Creative analysis and fatigue status"
  7_budget_analysis:
    content: "Spend vs. plan, pacing accuracy"
  8_trend_analysis:
    content: "3-month trend charts with context"
  9_test_results:
    content: "Summary of tests completed this month"
  10_recommendations:
    content: "Prioritized actions for next month"
quality_check: "Apply Reporting Quality Checklist before finalizing"
```

### Step 4: Recommendations Development (20 minutes per account)

```yaml
action: Develop actionable recommendations for next month
categories:
  - Budget recommendations (increase, decrease, reallocate)
  - Creative recommendations (new briefs, refreshes, retirements)
  - Audience recommendations (expand, refine, refresh)
  - Testing recommendations (new tests to run)
  - Strategic recommendations (channel changes, offer changes)
format:
  each_recommendation:
    - Specific action to take
    - Expected impact (quantified)
    - Rationale based on data
    - Priority level (high, medium, low)
    - Proposed timeline
```

### Step 5: Review and Quality Assurance (15 minutes per report)

```yaml
action: Apply Reporting Quality Checklist
checks:
  - [ ] All data points verified against source
  - [ ] Calculations and percentages double-checked
  - [ ] Consistent terminology throughout
  - [ ] Reporting period clearly stated
  - [ ] Insights are actionable, not just descriptive
  - [ ] Formatting is professional and consistent
  - [ ] Executive summary accurately reflects the full report
  - [ ] Recommendations are specific and prioritized
  - [ ] No confidential information exposed inappropriately
```

### Step 6: Delivery (5 minutes)

```yaml
action: Deliver report to stakeholders
delivery:
  - Send report via agreed channel (email, shared drive, dashboard)
  - Include brief cover note highlighting top 3 items
  - Schedule review meeting if needed
  - Set calendar reminder for next month's report
archive:
  - Save final report to reports archive
  - Update report registry with RPT-ID
  - Archive raw data snapshot
```

---

## Decision Points

| Condition | Action |
|-----------|--------|
| KPIs significantly below target | Include root cause analysis and recovery plan |
| KPIs significantly above target | Include scaling recommendations |
| Major platform changes occurred | Include impact assessment and adaptation plan |
| Test results available | Include test summary and implementation plan |
| Competitive shifts detected | Include competitive context section |

---

## Output / Deliverables

- Completed monthly performance report
- Data appendix with detailed tables
- Prioritized recommendations for next month
- Archived data snapshot
- Updated report registry

---

## Post-Conditions

- [ ] Report completed and quality-checked
- [ ] Report delivered to all stakeholders
- [ ] Report archived with RPT-ID
- [ ] Raw data snapshot archived
- [ ] Next month's report date scheduled
- [ ] Recommendations logged for tracking
