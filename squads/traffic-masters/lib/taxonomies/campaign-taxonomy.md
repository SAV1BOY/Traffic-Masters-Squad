# Campaign Taxonomy

## Purpose
Standard taxonomy for classifying campaign types, objectives, and structures across paid traffic operations. Ensures consistent categorization for reporting and analysis.

---

## Campaign Classification Hierarchy

```
Level 1: Business Objective
  Level 2: Campaign Type
    Level 3: Campaign Subtype
      Level 4: Targeting Strategy
```

---

## Level 1: Business Objectives

| Objective | Definition | Primary KPI | Secondary KPIs |
|---|---|---|---|
| **Awareness** | Maximize brand visibility and reach | Reach, CPM | Brand Lift, Video Views |
| **Consideration** | Drive engagement and interest | CPC, CTR | Video View Rate, Engagement Rate |
| **Conversion** | Generate sales, leads, or signups | CPA, ROAS | CVR, Revenue |
| **Retention** | Re-engage existing customers | Repeat Purchase Rate | LTV, Upsell Revenue |
| **Growth** | Scale customer acquisition efficiently | CAC, MER | New Customer Rate, LTV:CAC |

---

## Level 2: Campaign Types

### Prospecting Campaigns (Objective: Awareness + Conversion)

| Type | Description | Audience Temperature | Typical Platforms |
|---|---|---|---|
| **Broad Prospecting** | Minimal targeting, algorithm-driven | Cold | Meta, TikTok |
| **Interest-Based** | Targeting by declared interests or behaviors | Cold | Meta, TikTok, LinkedIn |
| **Lookalike / Similar** | Audiences modeled on seed data | Cold-Warm | Meta, TikTok, Google |
| **In-Market** | Users actively researching a category | Warm | Google, YouTube |
| **Competitor Targeting** | Targeting users interested in competitors | Cold | Google (keywords), Meta (interests) |
| **Content / Value-First** | Leading with content, not direct response | Cold | Meta, YouTube, TikTok |
| **Advantage+ / PMax** | Fully automated, cross-placement | Mixed | Meta (ASC), Google (PMax) |

### Retargeting Campaigns (Objective: Conversion)

| Type | Description | Audience Temperature | Typical Window |
|---|---|---|---|
| **Website Retargeting** | Past site visitors who did not convert | Warm-Hot | 1-30 days |
| **Engaged Retargeting** | Social engagers, video viewers | Warm | 7-90 days |
| **Cart Abandonment** | Users who added to cart but did not purchase | Hot | 1-14 days |
| **Lead Nurture** | Leads who have not yet converted to customers | Warm-Hot | 1-30 days |
| **Dynamic Product Retargeting** | Auto-shows products users viewed | Hot | 1-14 days |
| **Sequential Retargeting** | Multi-step retargeting with escalating messaging | Warm-Hot | 1-30 days |
| **Checkout Abandonment** | Users who initiated checkout but did not complete | Hot | 1-7 days |

### Brand Campaigns (Objective: Awareness + Consideration)

| Type | Description | Primary Metric |
|---|---|---|
| **Brand Search** | Bidding on own brand keywords | CPC, Impression Share |
| **Brand Video** | Video campaigns for brand storytelling | Video Views, View Rate |
| **Brand Awareness** | Reach-optimized campaigns | CPM, Reach, Frequency |
| **Brand Defense** | Protecting brand keywords from competitors | Impression Share, CPC |

### Retention Campaigns (Objective: Retention)

| Type | Description | Primary Metric |
|---|---|---|
| **Cross-Sell** | Promoting complementary products to buyers | Revenue, ROAS |
| **Upsell** | Promoting higher-tier products to buyers | AOV, Revenue |
| **Win-Back** | Re-engaging lapsed customers | Re-Activation Rate |
| **Loyalty** | Rewarding repeat customers | Repeat Purchase Rate |
| **Referral** | Encouraging customer referrals | Cost per Referral |

### Testing Campaigns (Objective: Learning)

| Type | Description | Primary Metric |
|---|---|---|
| **Creative Test** | A/B testing creative variables | CTR, CPA (per variant) |
| **Audience Test** | Testing new audience segments | CPA, CVR |
| **Offer Test** | Testing different offers or pricing | CVR, Revenue |
| **Landing Page Test** | Testing destination page variations | CVR, Bounce Rate |
| **Channel Test** | Testing new advertising platforms | CPA, ROAS |

---

## Level 3: Campaign Subtypes by Platform

### Meta Ads Campaign Objectives

| Meta Objective | Maps To | Optimization Event |
|---|---|---|
| Awareness | Brand Awareness | Reach, Ad Recall Lift |
| Traffic | Consideration | Link Clicks, Landing Page Views |
| Engagement | Consideration | Post Engagement, Video Views |
| Leads | Conversion (Lead Gen) | Lead Form Submissions |
| App Promotion | Conversion (App) | App Installs, App Events |
| Sales | Conversion (Purchase) | Purchases, Add to Cart |

### Google Ads Campaign Types

| Google Type | Maps To | Key Feature |
|---|---|---|
| Search | Intent Capture | Keyword-triggered text ads |
| Shopping | Product Discovery | Product listing ads |
| Display | Awareness | Banner ads across Display Network |
| Video (YouTube) | Awareness / Consideration | In-stream and discovery video ads |
| Performance Max | Full Funnel | Cross-channel automated campaign |
| Demand Gen | Consideration | Visual ads across Google surfaces |
| App | App Install | App promotion across Google ecosystem |

### TikTok Ads Campaign Objectives

| TikTok Objective | Maps To | Optimization Event |
|---|---|---|
| Reach | Awareness | Impressions |
| Traffic | Consideration | Clicks |
| Video Views | Consideration | Video Views |
| Community Interaction | Engagement | Followers, Profile Visits |
| App Promotion | Conversion (App) | App Installs |
| Website Conversions | Conversion | Purchase, Lead, ATC |
| Product Sales | Conversion (E-commerce) | Catalog Sales |

---

## Level 4: Targeting Strategy Tags

| Tag | Definition | Example |
|---|---|---|
| `prosp` | Prospecting (new users) | First-time visitors |
| `retarg` | Retargeting (known users) | Website visitors, cart abandoners |
| `brand` | Brand-related targeting | Brand keyword, brand audience |
| `broad` | No specific targeting constraints | Algorithm-driven |
| `lal` | Lookalike audience | LAL 1% purchasers |
| `interest` | Interest-based targeting | Fitness enthusiasts |
| `custom` | Custom audience (1st party data) | CRM list upload |
| `intent` | Intent-based targeting | In-market, custom intent |
| `competitor` | Competitor targeting | Competitor brand keywords |

---

## Taxonomy Application

### In Naming Conventions
```
[Brand]_[Platform]_[Objective]_[CampaignType]_[Geo]_[TargetingTag]_[Date]
```
**Example:** `acme_meta_conv_retarg-cart_US_custom_20260301`

### In Reporting
Group campaigns by taxonomy level for roll-up reporting:
- Level 1: "How is our Conversion spend performing vs. Awareness?"
- Level 2: "How is Prospecting performing vs. Retargeting?"
- Level 3: "Which Meta objective is delivering the best CPA?"
- Level 4: "Are Lookalike audiences outperforming Interest-based?"

### In Budget Allocation
Use taxonomy levels to set allocation rules:
- Conversion campaigns: 60-70% of budget
- Awareness campaigns: 15-25% of budget
- Testing campaigns: 10% of budget
- Retention campaigns: 5-10% of budget
