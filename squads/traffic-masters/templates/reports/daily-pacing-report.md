# Daily Pacing Report

> **Type**: Template
> **Category**: reports
> **Used by tasks**: daily-monitoring, budget-pacing, performance-alerts
> **Filled by agents**: media-buyer-agent, analyst-agent

## Purpose
Provides a daily snapshot of spend pacing, CPA trends, and key alerts, enabling quick decisions on budget adjustments and issue resolution before small problems become costly ones.

## Template

### Report Header
**Date**: [YYYY-MM-DD]
**Day of month**: [X of Y]
**Reporting period**: [month name, year]
**Prepared by**: [person or agent]

### Spend Summary
| Metric | Today | Yesterday | MTD | Monthly Budget | Pacing |
|---|---|---|---|---|---|
| Total spend | $[X] | $[X] | $[X] | $[X] | [ahead/on-track/behind] |
| Meta spend | $[X] | $[X] | $[X] | $[X] | [pacing] |
| Google spend | $[X] | $[X] | $[X] | $[X] | [pacing] |
| TikTok spend | $[X] | $[X] | $[X] | $[X] | [pacing] |
| Other spend | $[X] | $[X] | $[X] | $[X] | [pacing] |

**Pacing note**: [On track to spend $X by end of month vs. $X budget. X% through month, X% through budget.]

### CPA Trend
| Platform | Today CPA | 7-Day Avg CPA | MTD CPA | Target CPA | Status |
|---|---|---|---|---|---|
| Blended | $[X] | $[X] | $[X] | $[X] | [green/yellow/red] |
| Meta | $[X] | $[X] | $[X] | $[X] | [status] |
| Google | $[X] | $[X] | $[X] | $[X] | [status] |
| TikTok | $[X] | $[X] | $[X] | $[X] | [status] |

**Trend direction**: [CPA improving / stable / worsening over last 3 days]

### Key Metrics Today
| Metric | Today | vs. Yesterday | vs. 7-Day Avg |
|---|---|---|---|
| Impressions | [value] | [+/- %] | [+/- %] |
| Clicks | [value] | [+/- %] | [+/- %] |
| CTR | [value] | [+/- %] | [+/- %] |
| Conversions | [value] | [+/- %] | [+/- %] |
| Revenue | $[value] | [+/- %] | [+/- %] |
| ROAS | [ratio] | [+/- %] | [+/- %] |

### Alerts
| Alert Level | Issue | Platform | Action Required |
|---|---|---|---|
| [RED] | [Description of critical issue] | [platform] | [immediate action] |
| [YELLOW] | [Description of warning] | [platform] | [monitor / take action if persists] |
| [GREEN] | [Positive development] | [platform] | [no action / consider scaling] |

**Common alert triggers**:
- CPA exceeds target by 30%+ for 2 consecutive days
- Spend pacing more than 15% ahead or behind
- CTR drops below floor threshold
- Zero conversions on a campaign that normally converts
- CPM spike above 25% of 7-day average

### Actions Taken Today
1. [Action taken and rationale]
2. [Action taken and rationale]
3. [Action taken and rationale]

### Tomorrow's Plan
1. [Planned action or focus area]
2. [Planned action or focus area]
3. [Tests or launches scheduled]

### Notes
**Observations**: [Any qualitative observations about performance, market conditions, or anomalies]
**External factors**: [Holidays, competitor activity, platform issues, weather, news events]

## Usage Notes
- Complete this report by 10 AM daily using previous day's finalized data.
- Share with stakeholders via Slack, email, or shared dashboard.
- Focus on exceptions and actions, not just data recitation.
- If nothing noteworthy happened, say so briefly rather than padding the report.

## Example
March 6 pacing report: $1,450 spent today (on track for $45k monthly target). Meta CPA at $38 vs. $35 target (yellow alert, up from $33 two days ago). Paused underperforming ad set. Tomorrow: launch 2 new creatives to combat fatigue.

## Related
- weekly-performance-report.md
- monthly-growth-report.md
- media-plan-template.md
