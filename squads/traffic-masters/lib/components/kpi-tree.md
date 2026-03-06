# KPI Tree Component

## Purpose
Hierarchical KPI structure connecting business goals to tactical metrics.

## Tree Structure

```
Revenue (Business Goal)
├── ROAS
│   ├── AOV (Average Order Value)
│   │   ├── Upsell rate
│   │   └── Bundle adoption
│   └── Conversion Rate
│       ├── Landing page CVR
│       ├── Checkout completion
│       └── Ad-to-page relevance
├── Volume (Conversions)
│   ├── Traffic Volume
│   │   ├── Impressions × CTR
│   │   └── Budget ÷ CPC
│   └── Lead Quality
│       ├── MQL rate
│       └── SQL rate
└── Efficiency (CPA / nCAC)
    ├── CPM (cost per 1000)
    ├── CTR (click-through rate)
    └── CVR (conversion rate)
```

## Usage
1. Start at business goal level
2. Identify which branch is underperforming
3. Drill down to find the root cause metric
4. Optimize at the most specific level possible

## Example Diagnosis
- Revenue down → ROAS stable but volume down
- Volume down → Traffic volume down
- Traffic down → CTR dropped (creative fatigue)
- Action: Refresh creative, not increase budget

## Component Fields
- `goal`: Top-level business objective
- `primary_kpis`: First-level metrics
- `secondary_kpis`: Diagnostic metrics
- `tactical_metrics`: Day-to-day optimization metrics
- `relationships`: How metrics connect and influence each other
