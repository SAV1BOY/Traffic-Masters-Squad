# nCAC Calculator — Script Guide

## Purpose
Calculate New Customer Acquisition Cost to measure true cost of acquiring new customers.

## Formula
```
nCAC = Prospecting Ad Spend / New Customers Acquired
```

## Detailed Calculation

### Step 1: Isolate Prospecting Spend
- Include only TOFU/cold traffic campaigns
- Exclude retargeting, brand, and retention spend
- Exclude organic and referral acquisition costs

### Step 2: Count New Customers Only
- Subtract repeat purchases from total conversions
- Use CRM data to identify first-time buyers
- Exclude returning customer purchases

### Step 3: Calculate
```
nCAC = Prospecting Spend / First-Time Customers
```

## Example
| Metric | Value |
|--------|-------|
| Total Ad Spend | $30,000 |
| Prospecting Spend | $21,000 (70%) |
| Total Conversions | 600 |
| New Customers | 420 (70%) |
| Blended CPA | $50 |
| **nCAC** | **$50** ($21,000 / 420) |

## nCAC vs Blended CPA
| Metric | What It Measures | When to Use |
|--------|-----------------|-------------|
| Blended CPA | All conversions / all spend | Overall efficiency |
| nCAC | New customers / prospecting spend | Growth efficiency |
| CAC | All customers / all marketing spend | Total marketing efficiency |

## Health Benchmarks
| Ratio | Healthy | Warning | Critical |
|-------|---------|---------|----------|
| LTV:nCAC | >3:1 | 2-3:1 | <2:1 |
| Payback Period | <3 months | 3-6 months | >6 months |
| nCAC Trend | Stable/declining | Rising <10% MoM | Rising >10% MoM |

## Tracking Requirements
- CRM integration for new vs returning customer identification
- Proper UTM tracking for source attribution
- First-party data for accurate customer matching
- Regular data reconciliation between platform and CRM
