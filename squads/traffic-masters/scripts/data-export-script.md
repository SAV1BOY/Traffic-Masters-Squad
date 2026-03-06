# Data Export Script — Automation Script

> Data export and consolidation automation for aggregating performance data across platforms.

---

## Purpose

Systematically export, consolidate, and standardize performance data from multiple ad platforms and analytics tools into a unified format for reporting, analysis, and decision-making.

---

## Trigger / Schedule

- **Scheduled trigger:** Weekly (for weekly reports), monthly (for monthly reports)
- **Event trigger:** Ad-hoc analysis request, quarterly business review preparation
- **Duration:** 30-60 minutes per export cycle
- **Owner:** Reporting Agent
- **Supporting Agents:** Tracking Agent

---

## Pre-Conditions

- [ ] Access to all ad platform reporting interfaces / APIs
- [ ] Access to analytics platform (GA4 or equivalent)
- [ ] Export templates / data schemas defined
- [ ] Date ranges confirmed
- [ ] Metric definitions standardized across platforms

---

## Step-by-Step Workflow

### Step 1: Define Export Parameters (5 minutes)

```yaml
action: Set parameters for the data export
parameters:
  date_range:
    start: "[Period start date]"
    end: "[Period end date]"
    comparison_period: "[Previous period start] to [Previous period end]"
  granularity: "daily"           # daily | weekly | monthly
  breakdowns:
    - campaign
    - ad_set
    - ad
    - placement (optional)
    - device (optional)
    - age_gender (optional)
  metrics:
    core:
      - spend
      - impressions
      - reach
      - clicks
      - conversions
      - revenue
    calculated:
      - ctr (clicks / impressions)
      - cpc (spend / clicks)
      - cpa (spend / conversions)
      - roas (revenue / spend)
      - conversion_rate (conversions / clicks)
      - cpm (spend / impressions * 1000)
      - frequency (impressions / reach)
  filters:
    - Active campaigns only (or all, depending on need)
    - Minimum spend threshold (optional, to filter noise)
```

### Step 2: Platform Data Export (15 minutes)

```yaml
action: Export data from each active platform
platforms:
  meta:
    source: "Meta Ads Manager / Ads Reporting"
    export_method: "CSV export or API pull"
    fields:
      - Campaign Name, Ad Set Name, Ad Name
      - Spend, Impressions, Reach, Frequency
      - Clicks (Link), CTR (Link), CPC (Link)
      - Results (Conversions), Cost per Result
      - Purchase ROAS, Revenue
      - Video Views (if applicable), ThruPlay (if applicable)
    notes: "Ensure attribution window matches config (7d click, 1d view)"

  google_ads:
    source: "Google Ads Reporting"
    export_method: "CSV export or API pull"
    fields:
      - Campaign, Ad Group, Ad
      - Cost, Impressions, Clicks
      - CTR, Avg CPC
      - Conversions, Cost/Conv, Conv Rate
      - Conversion Value, Conv Value / Cost
      - Search Impr Share (search only)
      - Quality Score (keyword level)
    notes: "Include all conversion actions or filter to primary only"

  tiktok:
    source: "TikTok Ads Manager"
    export_method: "CSV export"
    fields:
      - Campaign Name, Ad Group Name, Ad Name
      - Spend, Impressions, Reach
      - Clicks, CTR, CPC
      - Conversions, CPA
      - Video Views, Video View Rate
    notes: "Check attribution settings match config"

  other_platforms:
    action: "Repeat export for each additional active platform"
    standard: "Match fields to the consolidated schema as closely as possible"
```

### Step 3: Analytics Data Export (10 minutes)

```yaml
action: Export analytics data for cross-referencing
source: "GA4 or equivalent"
export:
  traffic_data:
    dimensions: "Source, Medium, Campaign, Landing Page"
    metrics: "Sessions, Users, Bounce Rate, Pages/Session, Avg Session Duration"
  conversion_data:
    dimensions: "Source, Medium, Campaign"
    metrics: "Conversions (by type), Revenue"
  landing_page_data:
    dimensions: "Landing Page"
    metrics: "Sessions, Conversion Rate, Bounce Rate, Avg Page Load Time"
purpose: "Cross-reference with platform data for validation and post-click analysis"
```

### Step 4: Data Consolidation (10 minutes)

```yaml
action: Merge platform exports into unified format
consolidated_schema:
  fields:
    - date
    - platform (meta | google_ads | tiktok | etc.)
    - campaign_name
    - campaign_id (registry CMP-XXX)
    - ad_set_name
    - ad_name
    - creative_id (registry CRE-XXX)
    - audience_id (registry AUD-XXX)
    - spend
    - impressions
    - reach (where available)
    - clicks
    - conversions
    - revenue (where available)
    - ctr
    - cpc
    - cpa
    - roas (where available)
    - conversion_rate
    - cpm
    - frequency (where available)
  standardization:
    - Ensure all currency values are in the same currency
    - Standardize date format to YYYY-MM-DD
    - Map platform-specific metric names to unified names
    - Calculate derived metrics consistently
    - Handle null/missing values consistently (0 vs. null)
```

### Step 5: Data Validation (10 minutes)

```yaml
action: Validate consolidated data for accuracy
checks:
  completeness:
    - [ ] All active platforms represented
    - [ ] All active campaigns present in export
    - [ ] Date range is complete (no missing days)
    - [ ] No duplicate rows
  accuracy:
    - [ ] Total spend matches platform dashboards (within 1%)
    - [ ] Conversion counts match platform reports
    - [ ] Calculated metrics are mathematically correct
    - [ ] Currency is consistent across all rows
  consistency:
    - [ ] Naming conventions match registry entries
    - [ ] Platform names are standardized
    - [ ] Date formats are consistent
decision:
  validation_passes:
    yes: "Proceed to output"
    no: "Identify and fix discrepancies before proceeding"
```

### Step 6: Output and Archive (5 minutes)

```yaml
action: Save consolidated data and distribute
output:
  primary_file:
    format: "CSV or YAML"
    location: "data/exports/[date-range]-consolidated.csv"
    naming: "YYYY-MM-DD_to_YYYY-MM-DD_consolidated_export.csv"
  summary_file:
    format: "YAML or Markdown"
    location: "data/metrics/"
    content: "Account-level and platform-level summary metrics"
  archive:
    - Save raw platform exports to archive
    - Save consolidated file to archive
    - Maintain at least 12 months of export history
distribution:
  - Reporting Agent (for report generation)
  - Diagnostics Agent (for analysis)
  - Budget Agent (for efficiency analysis)
```

---

## Decision Points

| Condition | Action |
|-----------|--------|
| Platform data not available (reporting lag) | Wait 24-48 hours and retry |
| Data discrepancy > 5% between export and dashboard | Re-export and verify settings |
| Missing campaign data | Check campaign status and date range filters |
| Currency mismatch | Convert all values to account base currency |
| New platform added | Create export template matching consolidated schema |

---

## Output / Deliverables

- Consolidated cross-platform performance data file
- Platform-level summary metrics
- Archived raw exports
- Data validation confirmation
- Discrepancy notes (if any)

---

## Post-Conditions

- [ ] Data exported from all active platforms
- [ ] Analytics data exported for cross-reference
- [ ] Data consolidated into unified format
- [ ] Validation checks passed
- [ ] Files saved and archived
- [ ] Data ready for reporting and analysis use
