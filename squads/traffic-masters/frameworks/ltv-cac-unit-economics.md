# LTV-CAC Unit Economics
> **Type**: Financial Analysis Framework
> **Used by agents**: Performance Analyst, Traffic Chief

## Overview
Framework for calculating and optimizing the fundamental unit economics of paid traffic: Customer Lifetime Value (LTV), Customer Acquisition Cost (CAC), and the ratio between them. Profitable scaling requires mastery of these numbers. No campaign should scale without validated unit economics.

## When to Use
- Before launching any paid campaign to establish baseline economics
- Monthly and quarterly business reviews
- When evaluating new channels or making scaling decisions
- When profitability declines or CAC rises unexpectedly

## The Framework

### LTV Calculation Methods
1. **Historical LTV**: Total revenue from a customer cohort / Number of customers in that cohort
2. **Predictive LTV**: Average Order Value x Purchase Frequency x Customer Lifespan
3. **Cohort LTV**: Track revenue per cohort (month/quarter of acquisition) over time. Plot LTV curves. Compare cohorts to detect trend shifts early.

### CAC Calculation
- **Blended CAC**: Total marketing spend / Total new customers acquired
- **Channel CAC**: Channel-specific spend / Channel-attributed new customers
- **Fully Loaded CAC**: (Ad spend + tools + salaries + agency fees) / New customers

### LTV:CAC Ratio Benchmarks
- Below 1:1 — Losing money on every customer. Stop and fix immediately.
- 1:1 to 2:1 — Unprofitable or barely breaking even. Optimize before scaling.
- 3:1 — Target ratio. Healthy and scalable.
- 5:1+ — Potentially under-investing in growth. Scale more aggressively.

### Payback Period
- Time required to recover CAC from customer revenue
- Target: Under 90 days for ecommerce, under 12 months for SaaS
- Formula: CAC / (Monthly Revenue per Customer x Gross Margin)

### Marginal Contribution
- Revenue per unit minus all variable costs (COGS, shipping, processing, ad cost)
- Must be positive before scaling. Negative marginal contribution cannot be fixed with volume.

## Key Concepts
- LTV is a trailing metric; use cohort analysis to detect changes early
- CAC rises as you scale beyond core audiences into colder traffic
- Payback period determines cash flow requirements and scaling velocity
- Always use gross-margin-adjusted LTV, not raw revenue

## Decision Rules
1. Do not scale any channel where LTV:CAC is below 2:1
2. If payback period exceeds available cash runway, reduce spend or improve conversion
3. Re-calculate unit economics monthly; refresh cohort data quarterly
4. When CAC rises 20%+ without corresponding LTV change, diagnose before increasing budget
5. Factor in refund rates and churn when computing true LTV

## Integration
- Feeds into: Budget Allocation Model, MER Framework, Scaling Layer
- Receives from: Tracking Stack, Attribution Framework, CRM data

## Output
- LTV by cohort and channel
- CAC by channel (blended and fully loaded)
- LTV:CAC ratio with trend line
- Payback period in days
- Marginal contribution per customer
- Go/no-go recommendation for scaling
