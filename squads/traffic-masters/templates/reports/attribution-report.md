# Attribution Report

> **Type**: Template
> **Category**: reports
> **Used by tasks**: attribution-analysis, cross-channel-measurement, budget-allocation
> **Filled by agents**: analyst-agent, strategist-agent

## Purpose
Compares attribution data across models and platforms, reconciles discrepancies between platform-reported and blended metrics, performs sanity checks, and provides recommendations for budget allocation based on true channel contribution.

## Template

### Report Header
**Period**: [date range]
**Prepared by**: [person or agent]
**Date**: [date]
**Total ad spend**: $[X]
**Total revenue**: $[X] (source: [internal system])

### Model Used
**Primary attribution model**: [last-click / data-driven / first-click / linear / MER]
**Platform attribution windows**:
| Platform | Click Window | View Window | Notes |
|---|---|---|---|
| Meta | [7-day / 28-day] | [1-day / 7-day] | [default or custom] |
| Google | [30-day / 90-day] | [N/A] | [data-driven / last-click] |
| TikTok | [7-day / 28-day] | [1-day] | [default or custom] |
| GA4 | [data-driven / last-click] | [N/A] | [default model] |

**Why this model**: [Rationale for primary model selection]

### Channel Attribution Comparison
| Channel | Platform-Reported Revenue | GA4 Revenue | Blended/MER Revenue | Platform ROAS | GA4 ROAS | Blended ROAS |
|---|---|---|---|---|---|---|
| Meta | $[X] | $[X] | $[X] | [ratio] | [ratio] | [ratio] |
| Google Search | $[X] | $[X] | $[X] | [ratio] | [ratio] | [ratio] |
| Google Shopping | $[X] | $[X] | $[X] | [ratio] | [ratio] | [ratio] |
| YouTube | $[X] | $[X] | $[X] | [ratio] | [ratio] | [ratio] |
| TikTok | $[X] | $[X] | $[X] | [ratio] | [ratio] | [ratio] |
| Organic / Direct | N/A | $[X] | N/A | N/A | N/A | N/A |
| **Total** | **$[X]** | **$[X]** | **$[X]** | | | |

**Sum of platform-reported revenue**: $[X]
**Actual total revenue**: $[X]
**Over-reporting factor**: [X]x (platforms collectively over-report by this factor)

### Platform vs. Blended Comparison
| Channel | Platform CPA | Blended CPA | Delta | Over/Under Report |
|---|---|---|---|---|
| Meta | $[X] | $[X] | [+/- %] | [over-reports by X%] |
| Google Search | $[X] | $[X] | [+/- %] | [over/under] |
| Google Shopping | $[X] | $[X] | [+/- %] | [over/under] |
| YouTube | $[X] | $[X] | [+/- %] | [over/under] |
| TikTok | $[X] | $[X] | [+/- %] | [over/under] |

**Analysis**: [Which platforms over-report the most? Which under-report? How should we adjust our view?]

### MER (Marketing Efficiency Ratio) Analysis
**MER formula**: Total Revenue / Total Ad Spend
**Current MER**: [ratio]
**MER trend**:
| Month | Total Revenue | Total Ad Spend | MER |
|---|---|---|---|
| [Month 1] | $[X] | $[X] | [ratio] |
| [Month 2] | $[X] | $[X] | [ratio] |
| [Month 3] | $[X] | $[X] | [ratio] |

**MER direction**: [improving / stable / declining]
**Correlation analysis**: [Does MER move with specific channel spend changes?]

### Sanity Checks
| Check | Result | Status |
|---|---|---|
| Sum of platform revenue vs. actual revenue | Platforms report [X]x actual | [expected/concerning] |
| New customer count (platform) vs. CRM | Platform: [X], CRM: [X] | [aligned/misaligned] |
| Revenue trend in GA4 vs. backend | GA4: $[X], Backend: $[X] | [aligned/misaligned] |
| Conversion count consistency across platforms | [consistent/discrepant by X%] | [status] |
| Organic/direct revenue trend with ad spend changes | [correlated/independent] | [indicates halo effect?] |
| Days with zero ad spend vs. revenue on those days | Revenue without ads: $[X] | [baseline organic] |

### Cross-Channel Effects
**Halo effect observations**: [Does Meta spend lift Google brand search volume?]
**Cannibalization concerns**: [Are channels competing for the same conversions?]
**Assisted conversions**: [Which channels frequently assist but rarely get last-click credit?]
**Path analysis**: [Common conversion paths observed in GA4]

### Recommendations
**Recommendation 1**: [Budget reallocation based on true attribution]
- From: [channel at $X/month]
- To: [channel at $X/month]
- Rationale: [why this reallocation makes sense based on attribution data]

**Recommendation 2**: [Attribution model adjustment]
- Change: [what to change]
- Why: [rationale]

**Recommendation 3**: [Measurement improvement]
- Action: [specific improvement to tracking or measurement]
- Impact: [how this improves attribution accuracy]

### Next Steps
1. [Implement recommended budget reallocation]
2. [Conduct incrementality test on [channel] to validate attribution]
3. [Improve tracking for [specific gap identified]]
4. [Re-run attribution analysis in [timeframe]]

## Usage Notes
- Produce this report monthly or quarterly depending on spend level.
- Attribution is never perfectly accurate; focus on directional insights.
- Use MER as the north-star metric and platform data for optimization signals.
- Consider running holdout or geo-lift tests to validate attribution findings.

## Example
Q1 attribution analysis: Platforms collectively report $520k in revenue vs. $380k actual (1.37x over-reporting). Meta over-reports by 45%, Google under-reports by 10%. MER stable at 3.8x. Recommendation: shift 10% of Meta budget to Google Shopping which appears under-credited. Plan geo-lift test on TikTok to validate claimed contribution.

## Related
- monthly-growth-report.md
- quarterly-media-report.md
- tracking-brief.md
