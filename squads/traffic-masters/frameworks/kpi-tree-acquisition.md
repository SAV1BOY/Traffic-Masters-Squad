# KPI Tree for Acquisition
> **Type**: Performance Measurement Framework
> **Used by agents**: Performance Analyst, Traffic Chief

## Overview
A hierarchical KPI structure rooted in Revenue that branches into Traffic, Leads, MQLs, and Customers. Distinguishes leading indicators (predictive) from lagging indicators (outcome). Includes alert thresholds per node that trigger investigation or action when metrics deviate from targets.

## When to Use
- Setting up measurement frameworks for new campaigns or accounts
- Diagnosing performance problems by tracing from outcome to cause
- Creating dashboards and reporting structures
- Aligning team members on which metrics matter at each funnel level

## The Framework

### Root: Revenue
- The ultimate lagging indicator. Everything flows up to revenue.
- Decomposition: Revenue = Customers x AOV x Purchase Frequency

### Branch 1: Traffic Metrics (Leading)
- Impressions, Clicks, Sessions, Unique Visitors
- KPIs: CTR, CPC, CPM, traffic volume by source
- Alert: CTR drops >20% from baseline — investigate ad relevance
- Alert: CPC increases >30% — check auction competition and quality score

### Branch 2: Lead Metrics (Leading/Lagging)
- Visitors, Leads, Cost per Lead
- KPIs: Conversion rate (visitor to lead), lead volume, CPL
- Alert: CVR drops >15% — investigate landing page or offer
- Alert: CPL exceeds target by >25% — review traffic quality and landing page

### Branch 3: Qualification Metrics (Leading)
- Leads, MQLs, SQLs
- KPIs: MQL rate, SQL rate, lead-to-MQL time, MQL-to-SQL time
- Alert: MQL rate drops >20% — review lead quality or scoring criteria
- Alert: SQL rate drops — check sales follow-up speed and quality

### Branch 4: Customer Metrics (Lagging)
- SQLs, Opportunities, Customers
- KPIs: Close rate, sales cycle length, CAC, LTV
- Alert: Close rate drops >15% — investigate sales process or lead quality
- Alert: Sales cycle lengthens >20% — check qualification criteria

## Key Concepts
- Leading indicators predict the future; lagging indicators report the past
- Fix problems at the leading indicator level before they become lagging problems
- Alert thresholds trigger investigation, not automatic action
- The tree structure shows causality: traffic problems become revenue problems
- KPIs without targets are just numbers — always set benchmarks

## Decision Rules
- IF revenue is declining — trace down the tree to find the broken branch
- IF traffic is strong but leads are weak — problem is at conversion level
- IF leads are strong but customers are weak — problem is qualification or sales
- IF all branches are healthy but revenue is down — check AOV and frequency
- IF multiple branches decline — check for external factors (market, season)

## Integration
- Feeds into: All performance optimization and reporting workflows
- Pairs with: LTV-CAC Unit Economics (customer branch metrics)
- Complements: MER Marketing Efficiency Ratio (cross-branch blended metric)
- Source data: Tracking Stack Standard (data collection for all branches)

## Output
- Hierarchical KPI tree visualization from Revenue down to traffic-level metrics
- KPI definitions with formulas, owners, and data sources
- Alert threshold table with triggers and response protocols
- Dashboard specification based on the KPI tree structure
