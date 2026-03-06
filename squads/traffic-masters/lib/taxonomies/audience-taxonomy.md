# Audience Taxonomy

## Purpose
Standard taxonomy for classifying audience segments and types across paid traffic operations. Provides consistent categorization for targeting, reporting, and analysis.

---

## Audience Classification Hierarchy

```
Level 1: Data Source
  Level 2: Audience Type
    Level 3: Segment Definition
      Level 4: Behavioral Detail
```

---

## Level 1: By Data Source

### First-Party Audiences (Owned Data)

| Source | Description | Quality | Size | Platforms |
|---|---|---|---|---|
| **CRM / Customer List** | Email, phone, customer IDs from business systems | Highest | Varies | All major |
| **Website Pixel** | Behavioral data from pixel/tag events on your website | High | Medium-Large | All major |
| **Server-Side (CAPI)** | Server-sent events, typically higher match rate than pixel alone | Highest | Medium-Large | Meta, Google |
| **App SDK** | In-app behavioral data | High | Varies | Meta, Google, TikTok |
| **Email List** | Subscriber and engagement data | High | Small-Medium | Meta, Google |
| **Offline Data** | In-store purchases, call center data | High | Small | Meta, Google |

### Second-Party Audiences (Platform Data)

| Source | Description | Quality | Platforms |
|---|---|---|---|
| **Interest Categories** | Platform-inferred user interests | Medium | Meta, TikTok, LinkedIn |
| **Behavioral Categories** | Platform-inferred purchase and browsing behaviors | Medium | Meta, Google |
| **Demographic Data** | Age, gender, location, income, education | Medium-High | All major |
| **In-Market Segments** | Users actively researching a category | High | Google, YouTube |
| **Life Events** | Users experiencing specific life changes | Medium | Google, Meta |
| **Custom Intent** | Users who recently searched relevant terms | High | Google, YouTube |

### Third-Party Audiences (Partner Data)

| Source | Description | Quality | Platforms |
|---|---|---|---|
| **Data Partners** | Purchase data, intent signals from external providers | Medium | Programmatic, Google |
| **Publisher Data** | Contextual and behavioral data from website publishers | Medium | Programmatic |

### Algorithmic Audiences (Platform-Generated)

| Source | Description | Quality | Platforms |
|---|---|---|---|
| **Lookalike / Similar** | Modeled on seed audience characteristics | Medium-High | Meta, TikTok, Google |
| **Broad / Open** | No targeting constraints; algorithm finds converters | Variable | Meta, TikTok |
| **Advantage+ Audience** | Platform suggests targeting based on signals | Variable | Meta |

---

## Level 2: Audience Types

### By Customer Relationship

| Type | Definition | Temperature | Examples |
|---|---|---|---|
| **Unknown Prospect** | No prior interaction with the brand | Cold | Broad targeting, interests, in-market |
| **Engaged Prospect** | Has interacted but not converted | Warm | Social engagers, video viewers, email subscribers |
| **Active Lead** | Has submitted info but not purchased | Warm-Hot | Lead form submitters, demo requesters |
| **Cart/Checkout Abandoner** | Has shown strong purchase intent | Hot | Cart abandoners, checkout abandoners |
| **First-Time Customer** | Has made one purchase | Customer | Recent purchasers (0-30 days) |
| **Repeat Customer** | Has made 2+ purchases | Loyal Customer | Multi-purchasers |
| **High-Value Customer** | Top percentile by LTV or spend | VIP Customer | Top 10-20% by revenue |
| **Lapsed Customer** | Has not purchased within expected cycle | At-Risk Customer | No purchase in 90-180 days |
| **Churned Customer** | Inactive beyond expected lifecycle | Former Customer | No purchase in 180+ days |

### By Funnel Stage

| Stage | Audience Types | Campaign Type |
|---|---|---|
| **TOFU (Awareness)** | Unknown prospects, broad, interests, LAL 3-10% | Prospecting |
| **MOFU (Consideration)** | Engaged prospects, video viewers, social engagers, LAL 1% | Nurture |
| **BOFU (Decision)** | Active leads, cart abandoners, pricing page visitors | Retargeting |
| **Post-Purchase** | First-time buyers, repeat buyers | Retention, Cross-sell |

---

## Level 3: Segment Definitions

### Website Behavior Segments

| Segment | Definition | Lookback | Use Case |
|---|---|---|---|
| **All Visitors** | Anyone who visited any page | 30-180 days | General retargeting |
| **Product Page Viewers** | Visited specific product/service pages | 7-30 days | Product retargeting |
| **Category Browsers** | Viewed multiple pages in a category | 14-30 days | Category retargeting |
| **Blog/Content Readers** | Visited content/blog pages | 30-90 days | Content retargeting |
| **Pricing Page Visitors** | Visited pricing or plans page | 7-14 days | High-intent retargeting |
| **Cart Abandoners** | Added to cart but did not purchase | 1-14 days | Recovery campaigns |
| **Checkout Abandoners** | Initiated checkout but did not complete | 1-7 days | Urgent recovery |
| **Recent Purchasers** | Completed a purchase recently | 0-30 days | Cross-sell, upsell, or exclude |
| **Repeat Visitors** | Visited site 2+ times | 7-30 days | High-intent nurture |
| **High Time on Site** | Spent > X minutes on site | 14-30 days | Engaged visitor retargeting |

### Engagement Segments

| Segment | Definition | Lookback | Platform |
|---|---|---|---|
| **Page/Profile Followers** | Follow the brand's social page | Evergreen | Meta, TikTok |
| **Post Engagers** | Liked, commented, shared, or saved a post | 30-90 days | Meta, TikTok |
| **Video Viewers (25%)** | Watched 25% of a video | 30-90 days | Meta, TikTok, YouTube |
| **Video Viewers (50%)** | Watched 50% of a video | 30-60 days | Meta, TikTok, YouTube |
| **Video Viewers (75%)** | Watched 75% of a video | 14-30 days | Meta, TikTok, YouTube |
| **Video Viewers (95%)** | Watched 95%+ of a video | 7-30 days | Meta, TikTok, YouTube |
| **Ad Clickers (non-convert)** | Clicked ad but did not convert | 7-14 days | All platforms |
| **Lead Form Openers** | Opened lead form but did not submit | 7-14 days | Meta, LinkedIn |
| **Email Openers** | Opened marketing emails | 30-90 days | Via CRM upload |
| **Email Clickers** | Clicked links in marketing emails | 14-30 days | Via CRM upload |

### CRM-Based Segments

| Segment | Definition | Refresh Cadence |
|---|---|---|
| **All Customers** | Complete customer list | Weekly |
| **High-LTV Customers** | Top 20% by lifetime spend | Monthly |
| **Recent Buyers (0-30d)** | Purchased in last 30 days | Daily/Weekly |
| **Active Subscribers** | Currently subscribed/active | Weekly |
| **Trial Users** | On free trial, not yet converted | Daily |
| **Lapsed (90-180d)** | No purchase in 90-180 days | Weekly |
| **Churned (180d+)** | No purchase in 180+ days | Monthly |
| **VIP / Loyalty Members** | Members of loyalty program | Weekly |

---

## Level 4: Demographic and Behavioral Overlays

### Demographic Tags

| Dimension | Values |
|---|---|
| **Age** | 18-24, 25-34, 35-44, 45-54, 55-64, 65+ |
| **Gender** | Male, Female, All |
| **Location** | Country, Region, City, DMA, Radius |
| **Language** | Primary language |
| **Income** | Low, Medium, High (where available) |
| **Education** | High School, College, Graduate (where available) |
| **Job Title / Seniority** | C-Level, Director, Manager, Individual Contributor (LinkedIn) |
| **Industry** | Technology, Finance, Healthcare, Retail, etc. (LinkedIn) |
| **Company Size** | 1-50, 51-200, 201-1000, 1001+ (LinkedIn) |

### Behavioral Tags

| Behavior | Description | Platform |
|---|---|---|
| **Purchase Behavior** | Online shoppers, frequent buyers | Meta, Google |
| **Device** | Mobile, Desktop, Tablet | All |
| **OS** | iOS, Android | All |
| **Travel** | Frequent travelers, recent travelers | Meta, Google |
| **Tech Adoption** | Early adopters, tech enthusiasts | Meta |

---

## Audience Naming Convention

```
[Source]_[Type]_[SegmentDefinition]_[Lookback]_[SizeTag]
```

**Examples:**
```
px_retarg_all-visitors_30d_md
crm_custom_high-ltv_365d_sm
social_retarg_video-50pct_60d_md
px_retarg_cart-abandon_14d_sm
platform_lal-1pct_purchasers_180d_lg
platform_interest_fitness-yoga_na_lg
broad_open_no-targeting_na_max
```

**Size Tags:** `sm` (< 10K) | `md` (10-100K) | `lg` (100K-1M) | `max` (1M+)

---

## Exclusion Taxonomy

| Exclusion Type | When to Apply | Why |
|---|---|---|
| **Existing Customers** | All prospecting campaigns | Avoid paying to reach existing buyers |
| **Recent Purchasers (7-30d)** | Prospecting + retargeting | Avoid over-messaging recent buyers |
| **Converted Leads** | Lead gen campaigns | Stop spending on captured leads |
| **Internal/Employees** | All campaigns | Avoid wasting impressions on staff |
| **Negative Engagers** | All campaigns (where possible) | People who hid or reported ads |
| **Existing Retargeting Pool** | Prospecting campaigns | Clean prospecting/retargeting separation |
