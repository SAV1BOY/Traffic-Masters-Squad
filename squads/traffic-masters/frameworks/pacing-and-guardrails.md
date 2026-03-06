# Pacing and Guardrails

> **Type**: Internal
> **Domain**: Performance Monitoring — Thresholds and Alerts
> **Used by agents**: Performance Analyst, Media Buyer, Traffic Chief, Scale Optimizer

## Overview

Defines the monitoring thresholds, alert levels, and response protocols for all active campaigns. Pacing ensures budget is spent evenly and efficiently across the period. Guardrails prevent catastrophic overspend, CPA blowouts, or undetected underperformance. Every active campaign is subject to these rules — no exceptions.

## When to Use

- Daily performance monitoring (mandatory)
- Campaign launch first 72 hours (heightened monitoring)
- Scaling phases (tighter guardrails)
- Client budget changes or seasonal adjustments
- Post-mortem analysis of performance deviations

## The Framework

### Daily Pacing Check

Calculate daily pacing against monthly budget:

```
Daily Target Spend = Monthly Budget / Days in Month
Pacing % = (Actual Spend to Date / Expected Spend to Date) x 100
```

| Pacing % | Status | Action |
|----------|--------|--------|
| 90-110% | On Pace | No action needed |
| 80-89% | Underpacing | Increase bids or budgets 10-15%. Check ad rejections. |
| 111-120% | Overpacing | Reduce daily budgets 10-15%. Check for bid anomalies. |
| < 80% | Severe Underpacing | Investigate immediately. Ad rejections, audience exhaustion, platform issues. |
| > 120% | Severe Overpacing | Reduce budgets immediately. Check automated rules for errors. |

### Performance Guardrails

#### Primary Metrics

| Metric | Yellow Alert (Approaching) | Red Alert (Exceeded) | Action — Yellow | Action — Red |
|--------|--------------------------|---------------------|----------------|-------------|
| **CPA/CAC** | > 110% of target | > 150% of target | Monitor next 24h, note in log | Reduce budget 20%, diagnose cause |
| **ROAS** | < 90% of target | < 70% of target | Review creative performance | Pause underperformers, reallocate |
| **CTR** | < 80% of benchmark | < 60% of benchmark | Creative fatigue likely — queue refresh | Pause ads, swap creative immediately |
| **CVR** | < 85% of benchmark | < 65% of benchmark | Check landing page, offer, tracking | Pause campaign, investigate funnel |
| **Frequency** | > 3x/week (prospecting) | > 5x/week (prospecting) | Expand audience | Pause and restructure targeting |
| **Frequency** | > 5x/week (retargeting) | > 8x/week (retargeting) | Rotate creative | Pause, add frequency caps |
| **CPM** | > 120% of baseline | > 150% of baseline | Auction pressure — diversify placements | Reduce spend, test new audiences |

#### Secondary Metrics

| Metric | Watch Threshold | Action |
|--------|----------------|--------|
| **Hook Rate (3s views)** | < 20% | Replace hook in creative |
| **Hold Rate (ThruPlay)** | < 15% | Shorten video or improve mid-section |
| **Link Click-Through Rate** | < 0.8% | Test new CTA or creative format |
| **Cost Per Lead** | > 130% of target | Review lead quality before pausing |
| **Add to Cart Rate** | < 5% of clicks | Product page or pricing issue |
| **Landing Page Load Time** | > 3 seconds | Technical fix required — notify dev |

### Alert Levels and Escalation

**Level 1 — Green (Normal)**:
- All metrics within acceptable ranges.
- Standard daily check. Log performance. No escalation.

**Level 2 — Yellow (Caution)**:
- One or more metrics approaching thresholds.
- Increase monitoring to twice daily. Document in daily log.
- Media Buyer owns resolution. Notify Performance Analyst.

**Level 3 — Red (Critical)**:
- One or more metrics exceeded thresholds.
- Immediate action required per table above.
- Media Buyer executes. Performance Analyst reviews. Traffic Chief notified within 2 hours.

**Level 4 — Emergency**:
- Spend exceeds 200% of daily target OR CPA exceeds 200% of target.
- Pause all affected campaigns immediately.
- Traffic Chief and client notified within 1 hour.
- Post-mortem required within 24 hours.

## Key Concepts

- **Benchmark Establishment**: First 7 days of a campaign set the benchmark. Do not apply guardrails to Day 1-3 data — learning phase produces volatile numbers.
- **Rolling Averages**: Use 3-day rolling averages for decisions, not single-day spikes. Exception: Emergency level triggers on single-day data.
- **Blended vs Isolated**: Monitor individual campaign guardrails AND blended account-level metrics. A campaign can be red while the account is green.
- **Day-of-Week Patterns**: Some businesses have natural performance cycles (B2B weekdays, ecommerce weekends). Adjust daily targets accordingly.

## Decision Rules

1. Daily pacing check happens before 10 AM local time. No exceptions.
2. Yellow alerts are logged but do not require immediate client communication.
3. Red alerts require documented action plan within 4 hours.
4. Emergency alerts bypass normal communication channels — direct message to Traffic Chief.
5. Never override a Red alert stop-loss without written Traffic Chief approval.
6. Benchmark recalibration happens monthly or after significant strategic changes.

## Common Mistakes

- Reacting to single-day fluctuations instead of 3-day rolling trends.
- Setting guardrails too tight during launch phase — campaigns need room to learn.
- Not adjusting benchmarks after seasonal shifts or offer changes.
- Monitoring campaign-level metrics only and missing account-level blended performance.
- Failing to document alert history — patterns reveal systemic issues.
- Ignoring secondary metrics until primary metrics deteriorate.

## Integration

- Thresholds inform decisions in `scaling-playbook.md` — stop-loss rules reference these guardrails.
- Account structure in `account-structure-meta.md` and `account-structure-google.md` determines monitoring granularity.
- Creative refresh triggers connect to `creative-production-pipeline.md`.
- Reporting feeds `optimization-layer.md` for strategic recommendations.
- Client communication protocols align with `client-ops-handoff.md`.

## Output

- Daily pacing report (automated where possible).
- Alert log with timestamp, metric, level, action taken, outcome.
- Weekly guardrail summary report for Traffic Chief.
- Monthly benchmark recalibration document.
- Emergency post-mortem reports when Level 4 triggers.
