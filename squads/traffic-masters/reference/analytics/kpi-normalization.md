# KPI Normalization Reference
> **Category**: Analytics Methodology
> **Last Updated**: 2026-03

## Overview
KPI normalization creates consistent, comparable metrics across platforms, campaigns, and time periods. Without normalization, cross-platform comparison is misleading.

## Key Normalized Metrics

### Blended CPA
- Formula: Total ad spend (all platforms) / Total conversions (deduplicated)
- Purpose: True cost of acquisition across all channels
- Note: Requires deduplication to avoid double-counting conversions claimed by multiple platforms

### Blended ROAS
- Formula: Total revenue attributed to ads / Total ad spend
- Purpose: Overall return on advertising investment
- Note: Use GA4 or CRM revenue as source of truth, not platform-reported revenue

### Efficiency Ratio
- Formula: Total revenue / Total marketing cost (including fees, tools, team)
- Purpose: True marketing efficiency including all costs, not just ad spend

### Cost Per Qualified Lead (CPQL)
- Formula: Total ad spend / Qualified leads (leads that meet criteria)
- Purpose: Measures quality-adjusted lead cost, not just form fills

### LTV-to-CPA Ratio
- Formula: Customer Lifetime Value / Cost Per Acquisition
- Purpose: Profitability indicator. Target: 3:1 or higher
- Note: Use cohort LTV, not projected LTV

## Normalization Across Platforms
- Use consistent attribution windows when comparing platforms
- Normalize currency (BRL vs USD) at daily exchange rate
- Account for different conversion definitions (Meta lead vs Google lead)
- Use UTM-tracked GA4 data as the normalization layer

## Time Normalization
- Day-of-week effects: compare same days or use 7-day rolling averages
- Seasonality: use YoY comparison for seasonal businesses
- Spend changes: use CPA/ROAS ratios, not absolute numbers

## Key Takeaways
- Raw platform metrics are not directly comparable — normalize first
- Blended metrics give the truest picture of overall performance
- Always specify methodology when reporting normalized metrics
- Update normalization methodology as data sources change
- Share normalization definitions with all team members for consistency
