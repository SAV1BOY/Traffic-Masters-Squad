# Campaign Naming Standard

> **Type**: Template
> **Category**: naming
> **Used by tasks**: campaign-setup, reporting, cross-platform management
> **Filled by agents**: media-buyer-agent, strategist-agent

## Purpose
Establishes a consistent naming convention for campaigns, ad sets, and ads across all platforms, enabling clean reporting, easy filtering, and cross-platform analysis.

## Template

### Campaign Level Pattern
```
[platform]_[objective]_[audience]_[funnelstage]_[date]
```

### Ad Set Level Pattern
```
[platform]_[objective]_[audience-detail]_[targeting-type]_[geo]_[date]
```

### Ad Level Pattern
```
[platform]_[format]_[angle]_[hook-id]_[version]_[date]
```

### Rules
- All lowercase
- Use underscores as separators (no spaces, hyphens, or special characters)
- Maximum 60 characters per name
- Date format: YYYYMMDD or YYYYMM
- Use abbreviations from the approved list below
- No platform-specific emojis or symbols

### Approved Abbreviations
| Full Term | Abbreviation |
|---|---|
| acquisition | acq |
| retargeting | rtg |
| prospecting | pros |
| lookalike | lal |
| interest-based | int |
| broad | brd |
| top-of-funnel | tofu |
| middle-of-funnel | mofu |
| bottom-of-funnel | bofu |
| conversions | conv |
| traffic | traf |
| awareness | awr |
| lead generation | lead |
| video views | vidv |
| United States | us |
| United Kingdom | uk |
| image | img |
| video | vid |
| carousel | car |
| version | v1, v2 |

### Meta Examples
**Campaign**: `meta_conv_lal1pct_tofu_202603`
**Ad Set**: `meta_conv_lal1pct_purchasers_us_202603`
**Ad**: `meta_vid_pain_hook01_v1_20260301`

### Google Examples
**Campaign**: `google_search_brand_bofu_202603`
**Ad Group**: `google_search_brand_exact_us_202603`
**Ad**: `google_rsa_benefit_v2_20260301`

### YouTube Examples
**Campaign**: `youtube_vidv_pros_tofu_202603`
**Ad Group**: `youtube_vidv_int_fitness_us_202603`
**Ad**: `youtube_vid_aducate_hook03_v1_20260301`

### TikTok Examples
**Campaign**: `tiktok_conv_brd_tofu_202603`
**Ad Group**: `tiktok_conv_brd_18to34_us_202603`
**Ad**: `tiktok_ugc_desire_hook02_v1_20260301`

### Folder / Label Structure
- Group campaigns by funnel stage: TOFU, MOFU, BOFU
- Tag by objective: prospecting, retargeting, brand
- Label by creative batch: batch01, batch02

## Usage Notes
- Apply this standard to every new campaign before launch.
- Rename legacy campaigns during audit or optimization passes.
- Use the same naming in UTM campaign parameter for cross-reference.
- When a name would exceed 60 characters, drop the date suffix first.

## Example
A Meta prospecting campaign targeting US lookalike audiences for conversions launched in March 2026: `meta_conv_lal1pct_tofu_202603`

## Related
- utm-standard.md
- taxonomy-tags.md
- campaign-brief.md
