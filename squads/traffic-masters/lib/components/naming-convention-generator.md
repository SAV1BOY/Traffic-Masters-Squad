# Naming Convention Generator Component

## Purpose
Reusable naming convention system for campaigns, ad sets, ads, audiences, and creatives across all paid traffic platforms. Consistent naming enables efficient filtering, reporting, and analysis.

---

## Naming Architecture

### General Format
```
[Level]_[Delimiter-Separated Fields]
```
- **Delimiter:** Use underscores `_` between major fields, hyphens `-` within fields
- **Case:** Use lowercase for consistency, except acronyms (e.g., `US`, `TOFU`)
- **No Spaces:** Never use spaces in names
- **Date Format:** YYYYMMDD or YYYY-MM

---

## Campaign Naming Convention

### Format
```
[Brand]_[Platform]_[Objective]_[Funnel-Stage]_[Geo]_[Audience-Type]_[Date-Launched]
```

### Fields

| Field | Options | Examples |
|---|---|---|
| **Brand** | Client short name | `acme`, `brandx`, `client-abc` |
| **Platform** | `meta`, `gads`, `tiktok`, `yt`, `li`, `pin`, `snap` | `meta`, `gads` |
| **Objective** | `conv`, `traffic`, `reach`, `leads`, `sales`, `app-install`, `video-views` | `conv`, `leads` |
| **Funnel Stage** | `TOFU`, `MOFU`, `BOFU`, `RET` (retention) | `TOFU`, `BOFU` |
| **Geo** | ISO country code or region | `US`, `UK`, `EU`, `GLOBAL`, `US-CA` |
| **Audience Type** | `prosp` (prospecting), `retarg`, `lal` (lookalike), `brand`, `broad` | `prosp`, `retarg` |
| **Date Launched** | YYYYMMDD | `20260301` |

### Examples
```
acme_meta_conv_TOFU_US_prosp_20260301
acme_gads_leads_BOFU_UK_brand_20260215
brandx_tiktok_sales_TOFU_US_broad_20260310
```

---

## Ad Set / Ad Group Naming Convention

### Format
```
[Audience-Name]_[Targeting-Detail]_[Placement]_[Bid-Strategy]
```

### Fields

| Field | Options | Examples |
|---|---|---|
| **Audience Name** | Descriptive name | `lal-1pct-purch`, `int-fitness`, `retarg-7d-vc` |
| **Targeting Detail** | Age, gender, interest | `25-44-F`, `all-ages`, `fitness-yoga` |
| **Placement** | `auto`, `feed`, `stories`, `reels`, `search`, `display`, `pmax` | `auto`, `feed-stories` |
| **Bid Strategy** | `cbo`, `abo`, `tcpa`, `troas`, `manual`, `max-conv` | `cbo`, `tcpa-50` |

### Examples
```
lal-1pct-purch_25-44_auto_cbo
int-fitness-yoga_18-54_feed-stories_abo
retarg-30d-atc_all_auto_cbo
brand-kw-exact_all_search_tcpa-30
```

---

## Ad / Creative Naming Convention

### Format
```
[Format]_[Angle]_[Hook-Type]_[CTA]_[Creative-ID]_[Version]
```

### Fields

| Field | Options | Examples |
|---|---|---|
| **Format** | `img`, `vid-15s`, `vid-30s`, `vid-60s`, `car` (carousel), `ugc`, `coll`, `rsp` | `vid-30s`, `img` |
| **Angle** | `pain`, `benefit`, `social-proof`, `authority`, `curiosity`, `comparison`, `how-to`, `fomo` | `pain`, `social-proof` |
| **Hook Type** | `question`, `bold-claim`, `stat`, `testimonial`, `call-out`, `demo`, `problem` | `question`, `stat` |
| **CTA** | `shop-now`, `learn-more`, `sign-up`, `get-offer`, `book-now`, `download` | `shop-now` |
| **Creative ID** | Sequential or meaningful code | `CR001`, `SP-video-A` |
| **Version** | Version letter or number | `v1`, `v2`, `vA`, `vB` |

### Examples
```
vid-30s_pain_question_shop-now_CR001_v1
img_social-proof_testimonial_learn-more_CR015_v2
ugc_benefit_demo_get-offer_CR022_vA
car_comparison_bold-claim_shop-now_CR030_v1
```

---

## Audience Naming Convention

### Format
```
[Source]_[Type]_[Description]_[Lookback]_[Size-Indicator]
```

### Fields

| Field | Options | Examples |
|---|---|---|
| **Source** | `px` (pixel), `crm`, `social`, `video`, `lead`, `app` | `px`, `crm` |
| **Type** | `retarg`, `lal`, `custom`, `saved`, `intent` | `retarg`, `lal-1pct` |
| **Description** | What defines the audience | `all-visitors`, `purchasers`, `cart-abandon`, `video-50pct` |
| **Lookback** | Duration | `7d`, `30d`, `90d`, `180d`, `365d` |
| **Size Indicator** | Optional | `sm` (<10K), `md` (10-100K), `lg` (100K+) |

### Examples
```
px_retarg_all-visitors_30d_md
crm_lal-1pct_purchasers_180d_lg
social_retarg_ig-engagers_90d_sm
px_retarg_cart-abandon_14d_sm
video_retarg_viewers-50pct_30d_md
crm_custom_high-ltv-customers_365d_sm
```

---

## UTM Parameter Naming

### Format
```
utm_source=[platform]
utm_medium=[paid-type]
utm_campaign=[campaign-name]
utm_content=[ad-name]
utm_term=[keyword-or-audience]
```

### Standard Values

| Parameter | Convention | Examples |
|---|---|---|
| `utm_source` | Platform name | `facebook`, `google`, `tiktok`, `youtube`, `linkedin` |
| `utm_medium` | Paid channel type | `paid-social`, `paid-search`, `cpc`, `paid-video`, `display` |
| `utm_campaign` | Match campaign name (URL-safe) | `acme-conv-tofu-us-prosp` |
| `utm_content` | Ad/creative identifier | `vid-30s-pain-question-cr001-v1` |
| `utm_term` | Keyword or audience | `fitness-yoga`, `brand-exact`, `lal-1pct-purch` |

---

## File Naming (Creative Assets)

### Format
```
[Client]_[Platform]_[Format]_[Dimensions]_[Angle]_[ID]_[Version].[ext]
```

### Examples
```
acme_meta_video_1080x1080_pain-point_CR001_v1.mp4
acme_meta_static_1080x1920_social-proof_CR015_v2.png
acme_gads_responsive_multi_benefit_CR020_v1.zip
```

---

## Quick Reference Card

| Level | Template |
|---|---|
| **Campaign** | `brand_platform_objective_funnel_geo_audience_date` |
| **Ad Set** | `audience_targeting_placement_bidding` |
| **Ad** | `format_angle_hook_cta_id_version` |
| **Audience** | `source_type_description_lookback_size` |
| **UTM** | `source=platform&medium=type&campaign=name&content=ad&term=audience` |
| **File** | `client_platform_format_dimensions_angle_id_version.ext` |

---

## Implementation Checklist

- [ ] Agree on field values with team before launch
- [ ] Document any client-specific overrides
- [ ] Set up naming convention validation in campaign management tool
- [ ] Train all team members on the convention
- [ ] Create platform-specific templates (some fields vary by platform)
- [ ] Review and update naming conventions quarterly
