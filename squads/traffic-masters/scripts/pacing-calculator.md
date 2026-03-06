# Pacing Calculator — Script Guide

## Purpose
Calculate budget pacing to ensure spend is on track throughout the period.

## Daily Pacing Formula
```
Daily Target = Monthly Budget / Days in Month
MTD Target = Daily Target x Days Elapsed
Pacing % = (MTD Spend / MTD Target) x 100
```

## Pacing Status Definitions

| Pacing % | Status | Action |
|----------|--------|--------|
| 95-105% | On Track | No action needed |
| 85-94% | Slightly Under | Monitor, may need bid/budget increase |
| 106-115% | Slightly Over | Monitor, may need bid/budget decrease |
| <85% | Under-Pacing | Investigate delivery issues |
| >115% | Over-Pacing | Reduce budgets or pause lower priority |

## Example Calculation
- Monthly Budget: $10,000
- Days in Month: 30
- Daily Target: $333.33
- Today is Day 15
- MTD Target: $5,000
- MTD Spend: $4,200
- Pacing: 84% (Slightly Under)

## Projection Formula
```
Projected Monthly Spend = (MTD Spend / Days Elapsed) x Days in Month
Projected Variance = Projected Spend - Monthly Budget
```

## Common Pacing Issues

| Issue | Likely Cause | Fix |
|-------|-------------|-----|
| Severe under-pacing | Audience too small, bid too low | Broaden targeting or increase bids |
| Severe over-pacing | Broad targeting, high bids | Tighten targeting or reduce bids |
| Erratic daily spend | Learning phase, small audience | Wait for stabilization or increase budget |
| Front-loaded spend | Accelerated delivery | Switch to standard delivery |

## Monitoring Schedule
- Daily: Quick pacing check (morning)
- Weekly: Detailed pacing review with projection
- Monthly: Final reconciliation vs budget
