# UTM Builder Component

## Purpose
Reusable UTM parameter builder for consistent tracking across all paid traffic campaigns. Ensures clean attribution data in analytics platforms.

---

## UTM Parameter Reference

| Parameter | Required | Purpose | Example |
|---|---|---|---|
| `utm_source` | Yes | Identifies the traffic source (platform) | `facebook`, `google`, `tiktok` |
| `utm_medium` | Yes | Identifies the marketing medium | `paid-social`, `cpc`, `paid-video` |
| `utm_campaign` | Yes | Identifies the specific campaign | `spring-sale-tofu-us` |
| `utm_content` | Recommended | Differentiates ads/creatives within a campaign | `vid-30s-pain-cr001-v1` |
| `utm_term` | Optional | Identifies paid search keywords or audience | `running-shoes`, `lal-1pct` |

---

## Standard Values Dictionary

### utm_source

| Platform | Value | Notes |
|---|---|---|
| Facebook / Meta | `facebook` | Use `facebook` not `meta` for GA4 compatibility |
| Instagram | `instagram` | Or `facebook` if managed through Meta Ads Manager |
| Google Ads | `google` | Auto-tagged by default; use manual for override |
| TikTok | `tiktok` | |
| YouTube | `youtube` | If running through Google Ads, may auto-tag as `google` |
| LinkedIn | `linkedin` | |
| Pinterest | `pinterest` | |
| Snapchat | `snapchat` | |
| Twitter / X | `twitter` | |
| Microsoft Ads | `bing` | |
| Programmatic | `dv360`, `thetradedesk`, `{{DSP_NAME}}` | Use DSP name |
| Email | `email` | Not for paid traffic, but included for reference |

### utm_medium

| Medium | Value | When to Use |
|---|---|---|
| Paid Social | `paid-social` | Facebook, Instagram, TikTok, LinkedIn, Pinterest, Snapchat |
| Paid Search | `cpc` or `paid-search` | Google Search, Bing Search |
| Paid Shopping | `paid-shopping` | Google Shopping, PMax (shopping) |
| Paid Video | `paid-video` | YouTube, TikTok (video-specific), Connected TV |
| Display | `display` | Google Display Network, programmatic display |
| Native | `native` | Taboola, Outbrain |
| Retargeting | `retargeting` | Optional: use to separate retargeting from prospecting |
| Affiliate | `affiliate` | Affiliate/partner traffic |

### utm_campaign

**Format:** `[brand]-[objective]-[funnel]-[geo]-[audience]-[date]`

| Component | Convention | Examples |
|---|---|---|
| Brand | Lowercase short name | `acme`, `brandx` |
| Objective | Short descriptor | `conv`, `leads`, `awareness`, `sale` |
| Funnel | Stage abbreviation | `tofu`, `mofu`, `bofu`, `ret` |
| Geo | Country/region code | `us`, `uk`, `global` |
| Audience | Audience type | `prosp`, `retarg`, `broad`, `lal` |
| Date | Launch date (optional) | `202603`, `20260301` |

**Examples:**
```
acme-conv-tofu-us-prosp-202603
brandx-leads-bofu-uk-retarg
acme-spring-sale-us-broad
```

### utm_content

**Format:** `[format]-[angle]-[hook]-[creative-id]-[version]`

**Examples:**
```
vid-30s-pain-question-cr001-v1
img-social-proof-testimonial-cr015-v2
car-benefit-stat-cr022-va
ugc-how-to-demo-cr030-v1
```

### utm_term

| Use Case | Convention | Examples |
|---|---|---|
| Search Keywords | Actual keyword or keyword theme | `running-shoes`, `best-crm-software` |
| Audience Targeting | Audience segment name | `lal-1pct-purch`, `int-fitness`, `retarg-30d` |
| Placement | Placement name | `feed`, `stories`, `reels`, `search` |

---

## URL Builder

### Template
```
{{BASE_URL}}?utm_source={{SOURCE}}&utm_medium={{MEDIUM}}&utm_campaign={{CAMPAIGN}}&utm_content={{CONTENT}}&utm_term={{TERM}}
```

### Example Build
```
Base URL:     https://www.example.com/landing-page
utm_source:   facebook
utm_medium:   paid-social
utm_campaign: acme-conv-tofu-us-prosp-202603
utm_content:  vid-30s-pain-question-cr001-v1
utm_term:     lal-1pct-purch

Final URL:
https://www.example.com/landing-page?utm_source=facebook&utm_medium=paid-social&utm_campaign=acme-conv-tofu-us-prosp-202603&utm_content=vid-30s-pain-question-cr001-v1&utm_term=lal-1pct-purch
```

---

## Platform-Specific Dynamic Parameters

### Meta Ads (Facebook / Instagram)
Use dynamic URL parameters to auto-populate values:

| Parameter | Dynamic Value | What it Captures |
|---|---|---|
| `utm_source` | `facebook` (static) | Platform |
| `utm_medium` | `paid-social` (static) | Medium |
| `utm_campaign` | `{{campaign.name}}` | Campaign name |
| `utm_content` | `{{ad.name}}` | Ad name |
| `utm_term` | `{{adset.name}}` | Ad set name |

**Template:**
```
?utm_source=facebook&utm_medium=paid-social&utm_campaign={{campaign.name}}&utm_content={{ad.name}}&utm_term={{adset.name}}
```

### Google Ads
Google Ads uses auto-tagging (gclid) by default. For manual UTMs:

| Parameter | Dynamic Value | What it Captures |
|---|---|---|
| `{campaignid}` | Campaign ID | Numeric campaign ID |
| `{adgroupid}` | Ad group ID | Numeric ad group ID |
| `{keyword}` | Matched keyword | Search keyword |
| `{matchtype}` | Match type | `e`, `p`, `b` (exact, phrase, broad) |
| `{creative}` | Ad creative ID | Numeric creative ID |
| `{network}` | Network | `g` (search), `d` (display), `y` (YouTube) |

**Template:**
```
?utm_source=google&utm_medium=cpc&utm_campaign={_campaign}&utm_content={creative}&utm_term={keyword}
```

### TikTok Ads

| Parameter | Dynamic Value | What it Captures |
|---|---|---|
| `__CAMPAIGN_NAME__` | Campaign name | Campaign |
| `__AID_NAME__` | Ad group name | Ad group |
| `__CID_NAME__` | Ad name | Creative |

**Template:**
```
?utm_source=tiktok&utm_medium=paid-social&utm_campaign=__CAMPAIGN_NAME__&utm_content=__CID_NAME__&utm_term=__AID_NAME__
```

### LinkedIn Ads

| Parameter | Dynamic Value | What it Captures |
|---|---|---|
| `{{CAMPAIGN_NAME}}` | Campaign name | Campaign |
| `{{CAMPAIGN_GROUP_NAME}}` | Campaign group | Group |
| `{{CREATIVE_NAME}}` | Creative name | Ad |

**Template:**
```
?utm_source=linkedin&utm_medium=paid-social&utm_campaign={{CAMPAIGN_GROUP_NAME}}&utm_content={{CREATIVE_NAME}}&utm_term={{CAMPAIGN_NAME}}
```

---

## Rules and Best Practices

### Do
- Use all lowercase (e.g., `facebook` not `Facebook`)
- Use hyphens to separate words within a value (e.g., `paid-social`)
- Use consistent values across all team members
- Keep values URL-safe (no spaces, special characters)
- Document all UTM values in a shared reference
- Test URLs before launching campaigns

### Do Not
- Use spaces in any UTM value
- Mix cases (`Facebook` vs `facebook` creates two entries in analytics)
- Use abbreviations that are not documented
- Change UTM conventions mid-campaign without updating historical records
- Use UTM parameters on internal links (inflates session counts)
- Use `utm_source=ads` or other generic values that lose attribution clarity

---

## Validation Checklist

- [ ] Base URL loads correctly without UTM parameters
- [ ] Full URL with UTMs loads correctly (no broken redirects)
- [ ] UTM parameters appear in Google Analytics real-time view
- [ ] No duplicate `?` in the URL (check for existing query strings)
- [ ] Dynamic parameters resolve correctly on the platform
- [ ] All values follow the naming convention documented above
- [ ] No PII (personally identifiable information) in UTM values
- [ ] Redirects preserve UTM parameters (test 301/302 redirects)

---

## UTM Tracking Spreadsheet Template

| Campaign | Platform | Source | Medium | Campaign Name | Content | Term | Full URL | Status |
|---|---|---|---|---|---|---|---|---|
| `{{}}` | `{{}}` | `{{}}` | `{{}}` | `{{}}` | `{{}}` | `{{}}` | `{{}}` | `{{ACTIVE/PAUSED}}` |
