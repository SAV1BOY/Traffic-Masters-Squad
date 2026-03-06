# Audience Segment Builder Component

## Purpose
Reusable framework for building, categorizing, and structuring audience segments across paid traffic platforms. Use this component when defining target audiences for campaigns.

---

## Audience Architecture

### Tier 1: Core Segments (Always-On)

| Segment | Description | Temperature | Typical Size | Platforms |
|---|---|---|---|---|
| **Customer List** | Existing purchasers / clients | Hot | Varies | Meta, Google, TikTok |
| **High-Value Customers** | Top 20% by LTV or purchase frequency | Hot | Small | Meta, Google |
| **Website Retargeting (0-7d)** | Recent site visitors | Hot | Small-Medium | Meta, Google, TikTok |
| **Website Retargeting (8-30d)** | Mid-recency site visitors | Warm | Medium | Meta, Google, TikTok |
| **Engaged Social (0-30d)** | Recent page/profile engagers | Warm | Medium | Meta, TikTok |
| **Video Viewers (50%+)** | Watched 50%+ of video ads | Warm | Medium | Meta, YouTube, TikTok |
| **Lookalike 1% - Purchasers** | Top similarity to buyers | Cold | Large | Meta, TikTok |
| **Broad / Open Targeting** | Algorithm-driven, no restrictions | Cold | Maximum | Meta, TikTok |

### Tier 2: Expansion Segments

| Segment | Description | Temperature | When to Use |
|---|---|---|---|
| **Website Retargeting (31-90d)** | Older site visitors | Warm-Cool | When 0-30d is saturated |
| **Engaged Social (31-90d)** | Older engagers | Warm-Cool | Expanding retargeting pool |
| **Lookalike 1% - Leads** | Similar to lead list | Cold | Lead gen campaigns |
| **Lookalike 2-3% - Purchasers** | Broader purchaser similarity | Cold | Scaling prospecting |
| **Interest-Based** | Platform interest categories | Cold | Testing new audiences |
| **Behavior-Based** | Purchase behavior, device, etc. | Cold | Niche targeting |
| **Competitor Audiences** | People interested in competitors | Cold | Conquest campaigns |

### Tier 3: Advanced Segments

| Segment | Description | Temperature | When to Use |
|---|---|---|---|
| **Lookalike 5-10%** | Broadest similarity | Cold | Maximum scale needed |
| **Life Event Targeting** | Recently moved, married, etc. | Cold | Relevant products/services |
| **In-Market Audiences** | Actively researching category | Warm-Cold | Google, YouTube |
| **Custom Intent** | Based on search behavior | Warm | Google, YouTube |
| **Cart Abandoners** | Added to cart but didn't purchase | Hot | Recovery campaigns |
| **Lead Nurture (Opened, Not Converted)** | Engaged leads not yet converted | Warm | Mid-funnel push |

---

## Segment Building Blocks

### By Customer Journey Stage

```
AWARENESS (Cold)
  - Broad targeting
  - Interest stacking
  - Lookalike audiences (1-5%)
  - In-market audiences

CONSIDERATION (Warm)
  - Website visitors (non-converters)
  - Video viewers (25-75%)
  - Social engagers
  - Email subscribers (non-buyers)
  - Content consumers

DECISION (Hot)
  - Cart abandoners
  - Pricing page visitors
  - High-intent site visitors
  - Product page viewers (multiple visits)
  - Demo/trial requesters

RETENTION (Customer)
  - Past purchasers (for upsell/cross-sell)
  - Lapsed customers (win-back)
  - High-value customers (loyalty)
  - Subscription renewal targets
```

### By Data Source

| Source | Segment Types | Refresh Cadence | Platform Support |
|---|---|---|---|
| **1st Party - CRM** | Customer lists, lead lists, segments | Weekly | All major platforms |
| **1st Party - Pixel/CAPI** | Site visitors, event-based | Real-time | Meta, Google, TikTok |
| **1st Party - Email** | Subscribers, engagement-based | Weekly | Meta, Google |
| **2nd Party - Platform** | Interests, behaviors, demographics | Automatic | Platform-specific |
| **3rd Party - Data Partners** | Purchase data, intent data | Varies | Google, Programmatic |

---

## Segment Definition Template

Use this template for each new audience segment:

```
Segment Name: {{NAME}}
Segment ID: {{PLATFORM_AUDIENCE_ID}}
Platform: {{PLATFORM}}
Type: {{CUSTOM / LOOKALIKE / SAVED / IN-MARKET / CUSTOM INTENT}}
Data Source: {{SOURCE}}

Definition:
  - Include: {{INCLUSION_CRITERIA}}
  - Exclude: {{EXCLUSION_CRITERIA}}
  - Lookback Window: {{DAYS}}
  - Minimum Size: {{SIZE}}

Funnel Stage: {{AWARENESS / CONSIDERATION / DECISION / RETENTION}}
Temperature: {{HOT / WARM / COLD}}
Expected CPM Range: ${{MIN}} - ${{MAX}}
Expected CPA Range: ${{MIN}} - ${{MAX}}

Exclusions Applied:
  - [x] Existing customers (if prospecting)
  - [x] Recent converters ({{DAYS}} day window)
  - [x] Employees / internal traffic
  - [ ] Other: {{SPECIFY}}

Refresh Schedule: {{DAILY / WEEKLY / MONTHLY / REAL-TIME}}
Owner: {{NAME}}
Last Updated: {{DATE}}
```

---

## Exclusion Strategy

### Standard Exclusions (Apply to All Prospecting)
1. **Existing Customers** -- Upload customer list, exclude from prospecting
2. **Recent Purchasers** -- Exclude 7-30 day purchasers (avoid wasted spend)
3. **Internal Traffic** -- Exclude employee emails/IPs
4. **Converted Leads** -- Exclude from lead gen campaigns

### Retargeting Exclusions
1. **Already Purchased** -- Exclude from retargeting (unless upsell)
2. **High Frequency** -- Exclude users who have seen ad 8+ times
3. **Negative Engagers** -- Exclude users who hid ads

---

## Audience Sizing Guidelines

| Segment Type | Minimum Size | Ideal Size | Maximum Before Dilution |
|---|---|---|---|
| Retargeting (Meta) | 1,000 | 10,000-100,000 | No max |
| Custom Audience (Meta) | 1,000 | 5,000+ | No max |
| Lookalike 1% (Meta) | N/A (auto) | ~2M (US) | -- |
| RLSA (Google) | 1,000 | 10,000+ | No max |
| Custom Intent (Google) | N/A (auto) | -- | -- |
| Retargeting (TikTok) | 1,000 | 10,000+ | No max |

---

## Audience Testing Framework

### Phase 1: Foundation (Week 1-2)
- Launch with 3-5 proven audiences
- Include at least one retargeting, one lookalike, and one broad segment
- Budget split: 50% proven, 30% high-potential, 20% experimental

### Phase 2: Expansion (Week 3-4)
- Add 2-3 new audience segments based on Phase 1 learnings
- Test interest stacks that align with winning segments
- Begin lookalike expansion (1% to 2-3%)

### Phase 3: Optimization (Week 5+)
- Consolidate around top 3-5 performing audiences
- Kill audiences with CPA > 150% of target after sufficient data
- Layer in demographic or placement optimizations

---

## Platform-Specific Notes

### Meta Ads
- Advantage+ Audience uses your targeting as suggestions, not hard constraints
- Lookalike audiences based on value (purchase value) often outperform count-based
- Broad targeting with strong creative often beats detailed targeting at scale

### Google Ads
- Observation mode lets you monitor audience performance without restricting reach
- Custom Intent audiences built from competitor URLs and keywords are powerful
- Layer audiences with search campaigns for bid adjustments

### TikTok Ads
- Interest categories are broader than Meta; creative does more targeting work
- Lookalike audiences require minimum 10,000 source audience
- Broad targeting with strong hooks is the primary strategy at scale
