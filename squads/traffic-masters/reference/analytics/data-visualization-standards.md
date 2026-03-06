# Data Visualization Standards for Ad Performance Reports

> Standards and best practices for creating clear, actionable ad performance reports and dashboards.

---

## 1. Core Principles

### The 5-Second Rule
Any chart or dashboard should communicate its main message within 5 seconds. If a stakeholder has to study it, it's too complex.

### Key Principles

1. **Lead with the answer**: Title charts with the insight, not the metric ("CPA Decreased 18% in March" not "Cost per Acquisition Over Time")
2. **Right chart for the data**: Don't use pie charts for time series or bar charts for correlations
3. **Minimize clutter**: Remove gridlines, borders, legends (when possible), and decorative elements
4. **Consistent formatting**: Same colors, fonts, scales across all reports
5. **Context over data**: Always include benchmarks, targets, or prior period comparisons
6. **Actionable focus**: Every chart should answer "So what should we do?"

---

## 2. Chart Type Selection Guide

### When to Use Each Chart Type

| Data Relationship | Chart Type | Example |
|-------------------|-----------|---------|
| **Trend over time** | Line chart | CPA over 30 days |
| **Comparison across categories** | Horizontal bar chart | ROAS by campaign |
| **Part of a whole** | Stacked bar or 100% stacked bar | Budget allocation by channel |
| **Distribution** | Histogram or box plot | CPC distribution across ad sets |
| **Correlation** | Scatter plot | Spend vs. Conversions by campaign |
| **Single KPI** | Scorecard / Big number | Total conversions this week |
| **KPI vs. Target** | Bullet chart or gauge | CPA vs. target CPA |
| **Geographic** | Map / Choropleth | Conversions by state/region |
| **Funnel** | Funnel chart | Impression > Click > Lead > Sale |
| **Multiple KPIs over time** | Small multiples (faceted charts) | CTR, CPC, CR for each campaign |

### Charts to AVOID in Ad Reporting

| Chart | Problem | Use Instead |
|-------|---------|-------------|
| **Pie chart** | Hard to compare slices; useless for >5 categories | Bar chart or table |
| **3D charts** | Distorts perception; looks unprofessional | 2D versions |
| **Dual-axis charts** | Misleading; implies correlation | Two separate charts or indexed chart |
| **Donut chart** | Same problems as pie chart | Bar chart or table |
| **Area chart** (stacked, multiple series) | Hard to read middle layers | Stacked bar or small multiples |

---

## 3. Color Standards

### Recommended Color Palette

**Performance indicators**:
- Green (`#2E7D32`): Positive / above target / improvement
- Red (`#C62828`): Negative / below target / decline
- Yellow/Amber (`#F9A825`): Warning / near target / watch
- Gray (`#757575`): Neutral / baseline / prior period

**Platform colors** (for source identification):
- Meta: `#1877F2`
- Google Ads: `#4285F4`
- TikTok: `#000000` or `#EE1D52`
- LinkedIn: `#0A66C2`
- YouTube: `#FF0000`
- Email: `#757575`

### Color Rules

1. **Maximum 5-6 colors per chart**; use shades for additional series
2. **Consistent color mapping**: If Meta is blue in one chart, it's blue in all charts
3. **Colorblind-friendly**: Avoid red/green only; use shapes or patterns as secondary indicators
4. **Highlight what matters**: Use a bold color for the key data point; gray everything else
5. **Dark backgrounds**: Avoid; they reduce readability in presentations and prints

---

## 4. KPI Dashboard Layout

### Executive Dashboard Structure

```
┌─────────────────────────────────────────────────────┐
│                  DATE RANGE SELECTOR                 │
│              [Last 7 days] [Last 30 days] [Custom]  │
├──────────┬──────────┬──────────┬──────────┬─────────┤
│  SPEND   │ REVENUE  │   ROAS   │   CPA    │  CONV   │
│  $24.5K  │  $98.2K  │  4.01x   │  $32.40  │  756    │
│  +12% ▲  │  +18% ▲  │  +5% ▲   │  -8% ▼   │ +22% ▲ │
├──────────┴──────────┴──────────┴──────────┴─────────┤
│                                                      │
│  [LINE CHART: Revenue & Spend Over Time]            │
│                                                      │
├────────────────────────┬─────────────────────────────┤
│                        │                             │
│  [BAR CHART:           │  [TABLE:                    │
│   ROAS by Channel]     │   Top 5 Campaigns]          │
│                        │                             │
├────────────────────────┼─────────────────────────────┤
│                        │                             │
│  [FUNNEL:              │  [PIE/BAR:                  │
│   Conversion Funnel]   │   Budget Allocation]        │
│                        │                             │
└────────────────────────┴─────────────────────────────┘
```

### Campaign-Level Dashboard

```
┌─────────────────────────────────────────────────────┐
│  CAMPAIGN: [Dropdown Selector]                       │
├──────────┬──────────┬──────────┬──────────┬─────────┤
│  CTR     │  CPC     │  CR      │  CPA     │ ROAS    │
│  1.82%   │  $1.24   │  4.2%    │  $29.50  │ 3.8x   │
├──────────┴──────────┴──────────┴──────────┴─────────┤
│                                                      │
│  [LINE CHART: Daily CPA with Target Line]           │
│                                                      │
├────────────────────────┬─────────────────────────────┤
│  [TABLE:               │  [BAR CHART:                │
│   Ad Set Performance]  │   Creative Performance]     │
│                        │   (CTR by Ad)               │
├────────────────────────┼─────────────────────────────┤
│  [SCATTER:             │  [TABLE:                    │
│   Spend vs CPA         │   Audience Segments]        │
│   by Ad Set]           │                             │
└────────────────────────┴─────────────────────────────┘
```

---

## 5. Table Formatting Standards

### Performance Tables

**Good table practices**:
- Right-align numbers; left-align text
- Use consistent decimal places ($1.24 not $1.2 or $1.243)
- Include trend arrows or color coding for performance vs. prior period
- Bold the most important column
- Sort by the most actionable metric (not alphabetically)
- Limit to 10-15 rows; use "Top N" with option to expand

**Example format**:

| Campaign | Spend | Conv | CPA | ROAS | vs. Target |
|----------|------:|-----:|----:|-----:|:----------:|
| Prospecting - Broad | $8,450 | 245 | $34.49 | 3.2x | On Track |
| Prospecting - LAL | $5,200 | 198 | $26.26 | 4.1x | Above |
| Retargeting - Web | $3,100 | 156 | $19.87 | 5.8x | Above |
| Non-Brand Search | $4,800 | 112 | $42.86 | 2.4x | Below |
| Brand Search | $2,950 | 245 | $12.04 | 9.2x | Above |

### Number Formatting Standards

| Metric | Format | Example |
|--------|--------|---------|
| Currency (small) | $X.XX | $12.45 |
| Currency (large) | $X.XK or $X.XM | $24.5K, $1.2M |
| Percentages | X.X% (one decimal) | 3.2% |
| Large numbers | X,XXX or X.XK | 1,245 or 1.2K |
| ROAS | X.XXx | 3.45x |
| Ratios | X:1 or X.Xx | 3.5:1 or 3.5x |
| Dates | MMM DD | Mar 06 |

---

## 6. Time Series Best Practices

### Daily vs. Weekly vs. Monthly Data

| Granularity | When to Use | Audience |
|-------------|-------------|----------|
| **Daily** | Monitoring, anomaly detection | Media buyers, ops team |
| **Weekly** | Performance reviews, optimization | Team leads, managers |
| **Monthly** | Strategic reviews, trend analysis | Directors, C-suite |
| **Quarterly** | Business reviews, planning | Executives, stakeholders |

### Smoothing Noisy Data

Daily ad data is inherently noisy. For trend visualization:
- **7-day rolling average**: Smooths day-of-week effects; best for weekly reviews
- **14-day rolling average**: Smoother trend line; good for presentations
- **Show both**: Raw daily data (light, thin line) + rolling average (bold line)

### Annotations

Always annotate significant events on time series charts:
- Campaign launches / pauses
- Budget changes
- Creative swaps
- Platform algorithm updates
- Holidays / sales events
- Website changes
- Competitor actions

---

## 7. Comparison Frameworks

### Period-over-Period Comparison

| Comparison | Use Case |
|-----------|----------|
| Week-over-Week (WoW) | Short-term optimization decisions |
| Month-over-Month (MoM) | Medium-term performance trends |
| Year-over-Year (YoY) | Seasonality-adjusted growth measurement |
| Same Period Last Year | Best for seasonal businesses |

### Benchmark Visualization

Show metrics in context with benchmarks:

```
CPA: $32.40
├────────────────────┤
Target: $35.00       ← Green (below target = good)
Industry Avg: $42.00 ← Well below industry average
```

### Waterfall Charts for Variance Analysis

Show what drove changes between periods:

```
January ROAS:    3.2x
+ CTR improvement:    +0.3x
+ CR improvement:     +0.2x
- CPC increase:       -0.1x
- AOV decrease:       -0.1x
= February ROAS: 3.5x
```

---

## 8. Funnel Visualization

### Standard Ad Funnel

```
Impressions:    1,000,000  (100%)
    │
    ├──> CTR: 1.5%
    │
Clicks:            15,000  (1.5%)
    │
    ├──> LP CR: 8%
    │
Leads/ATC:          1,200  (0.12%)
    │
    ├──> Checkout CR: 45%
    │
Purchases:            540  (0.054%)
```

### Funnel Best Practices
- Show absolute numbers AND percentages
- Highlight the biggest drop-off point (the bottleneck)
- Include stage-over-stage conversion rates
- Color-code by performance vs. benchmark
- Place funnel next to a table with detailed metrics per stage

---

## 9. Dashboard Tools

### Recommended Tools by Use Case

| Tool | Best For | Cost | Skill Level |
|------|----------|------|-------------|
| **Looker Studio (Data Studio)** | Google Ads + GA4 dashboards | Free | Low-Medium |
| **Tableau** | Complex multi-source analysis | $$$ | Medium-High |
| **Power BI** | Microsoft ecosystem; enterprise | $$ | Medium |
| **Supermetrics** | Data extraction to sheets/tools | $$ | Low |
| **Google Sheets** | Quick ad-hoc analysis | Free | Low |
| **Databox** | Mobile-friendly KPI dashboards | $$ | Low |
| **Klipfolio** | Multi-source KPI dashboards | $$ | Medium |
| **Custom (Metabase, Redash)** | Data warehouse dashboards | Free-$ | High |

### Looker Studio Best Practices

1. **Use blended data** to combine Google Ads + GA4 in one chart
2. **Create date range controls** at the top of every page
3. **Use calculated fields** for custom metrics (ROAS, CR, profit)
4. **Set up email delivery** for automated weekly reports
5. **Use community connectors** for Meta, TikTok, LinkedIn data

---

## 10. Report Templates by Audience

### For the Media Buyer (Daily)
- Pacing vs. budget
- CPA and ROAS by campaign (today + 7-day trend)
- Top/bottom performing ad sets
- Creative performance leaderboard
- Anomaly alerts

### For the Team Lead (Weekly)
- Week-over-week KPI summary
- Channel-level performance comparison
- Budget utilization and reallocation needs
- A/B test results
- Key wins and losses

### For the Director/VP (Monthly)
- Revenue and ROAS trend (monthly)
- Channel contribution to pipeline/revenue
- CAC and LTV trends by cohort
- Budget efficiency vs. target
- Competitive landscape changes

### For the C-Suite (Quarterly)
- Revenue growth attributed to paid channels
- Blended CAC trend
- LTV:CAC ratio by channel
- Market share / share of voice
- Strategic recommendations with projected impact

---

## 11. Common Visualization Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| Starting Y-axis at non-zero | Exaggerates small changes | Start at 0 unless explicitly noted |
| Using dual Y-axes | Implies false correlation | Use two separate charts |
| Too many series on one chart | Unreadable | Limit to 5 series; use small multiples |
| No context (benchmarks, targets) | Numbers are meaningless without context | Always include comparison points |
| Showing data without insight | Stakeholders don't know what to do | Add annotations and recommendations |
| Inconsistent date ranges | Apples-to-oranges comparisons | Standardize comparison periods |
| Over-decorating | Distracts from the data | Remove chartjunk; maximize data-ink ratio |
| Using averages without distribution | Hides important variance | Show distributions or include range |

---

*Last updated: March 2026. Good data visualization is a competitive advantage in paid traffic management. Reports that drive action are more valuable than reports that simply display data.*
