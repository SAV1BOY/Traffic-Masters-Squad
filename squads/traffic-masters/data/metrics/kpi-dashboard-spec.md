# KPI Dashboard Specification

## Purpose
Define the structure and metrics for the traffic squad's KPI dashboard.

## Dashboard Sections

### 1. Executive Summary
- Total spend (period)
- Blended ROAS / CPA
- Revenue attributed to paid
- Budget pacing status

### 2. Platform Performance
| Metric | Meta | Google | TikTok | YouTube | LinkedIn |
|--------|------|--------|--------|---------|----------|
| Spend | | | | | |
| ROAS | | | | | |
| CPA | | | | | |
| CTR | | | | | |
| Conv | | | | | |

### 3. Funnel Metrics
- TOFU: Impressions, reach, CPM, CTR
- MOFU: Engagement rate, video views, page visits
- BOFU: Conversions, CPA, ROAS, AOV

### 4. Creative Performance
- Top 5 creatives by CPA
- Creative fatigue alerts (frequency > 3, CTR declining)
- Format distribution (video / static / carousel)

### 5. Experiment Tracker
- Active tests count
- Tests completed this period
- Win rate percentage

## Data Sources
- Platform APIs (Meta, Google, TikTok, LinkedIn)
- Analytics (GA4)
- CRM (for lead quality and LTV)

## Update Frequency
- Real-time: Spend pacing
- Daily: Core metrics
- Weekly: Full dashboard refresh
- Monthly: Trend analysis and insights

## Tools
- Looker Studio, Supermetrics, or Triple Whale
