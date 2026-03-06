# UTM Standard

> **Type**: Template
> **Category**: naming
> **Used by tasks**: tracking-setup, campaign-setup, analytics-reporting
> **Filled by agents**: tracking-agent, media-buyer-agent

## Purpose
Defines the UTM parameter naming convention for all paid traffic campaigns, ensuring consistent attribution data flows into GA4 and other analytics tools for accurate cross-platform reporting.

## Template

### UTM Pattern
```
?utm_source=[platform]&utm_medium=[paid-type]&utm_campaign=[campaign-name]&utm_content=[creative-id]&utm_term=[keyword-or-audience]
```

### Parameter Definitions

#### utm_source
**Purpose**: Identifies the traffic source platform.
**Values**:
- `meta` - Meta Ads (Facebook + Instagram)
- `google` - Google Ads (Search, Shopping, Display)
- `youtube` - YouTube Ads
- `tiktok` - TikTok Ads
- `linkedin` - LinkedIn Ads
- `email` - Email campaigns
- `affiliate` - Affiliate partners

**Rules**: Always lowercase, no spaces, use platform name not placement.

#### utm_medium
**Purpose**: Identifies the marketing medium or cost model.
**Values**:
- `cpc` - Cost per click (search ads)
- `cpm` - Cost per thousand impressions (display, awareness)
- `paid-social` - Paid social media ads
- `paid-video` - Paid video ads
- `paid-search` - Paid search ads
- `retargeting` - Retargeting campaigns
- `affiliate` - Affiliate traffic
- `email` - Email campaigns

**Rules**: Always lowercase, use hyphens for multi-word values.

#### utm_campaign
**Purpose**: Identifies the specific campaign.
**Value format**: `[objective]-[audience]-[funnelstage]-[date]`
**Examples**:
- `conv-lal1pct-tofu-202603`
- `lead-interest-mofu-202603`
- `rtg-sitevisitors-bofu-202603`

**Rules**: Lowercase, hyphens as separators, match campaign naming standard.

#### utm_content
**Purpose**: Identifies the specific creative or ad variant.
**Value format**: `[format]-[angle]-[hookid]-[version]`
**Examples**:
- `vid-pain-hook01-v1`
- `img-desire-hook03-v2`
- `car-proof-hook01-v1`

**Rules**: Lowercase, hyphens as separators, must map to creative ID.

#### utm_term
**Purpose**: Identifies the keyword (search) or audience segment (social).
**Values for search**: `[keyword]` using plus signs for spaces: `best+running+shoes`
**Values for social**: `[audience-type]-[detail]`
**Examples**:
- `brand+keyword+exact`
- `lal1pct-purchasers`
- `interest-fitness-25to44`

**Rules**: Lowercase, plus signs for keyword spaces, hyphens for segments.

### Full URL Examples

**Meta prospecting ad**:
```
https://example.com/landing?utm_source=meta&utm_medium=paid-social&utm_campaign=conv-lal1pct-tofu-202603&utm_content=vid-pain-hook01-v1&utm_term=lal1pct-purchasers
```

**Google search ad**:
```
https://example.com/product?utm_source=google&utm_medium=cpc&utm_campaign=search-brand-bofu-202603&utm_content=rsa-benefit-v2&utm_term=best+protein+powder
```

**TikTok UGC ad**:
```
https://example.com/offer?utm_source=tiktok&utm_medium=paid-social&utm_campaign=conv-broad-tofu-202603&utm_content=ugc-desire-hook02-v1&utm_term=broad-18to34
```

### Validation Rules
- No uppercase letters allowed
- No spaces (use hyphens or plus signs)
- No special characters except hyphens and plus signs
- All five parameters required for paid campaigns
- UTM campaign value must match the campaign naming convention
- Test all URLs before launch to confirm parameters pass correctly

## Usage Notes
- Use a UTM builder spreadsheet or tool to generate URLs consistently.
- Validate UTMs appear correctly in GA4 real-time reports before scaling spend.
- Never change UTM conventions mid-campaign without updating all active URLs.

## Example
A TikTok video ad for a TOFU conversions campaign targeting broad 18-34 audience with a desire-angle hook: full URL includes all five parameters following the patterns above.

## Related
- campaign-naming-standard.md
- tracking-brief.md
- taxonomy-tags.md
