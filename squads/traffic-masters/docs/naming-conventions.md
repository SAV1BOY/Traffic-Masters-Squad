# Naming Conventions

> Standard naming conventions for campaigns, ad sets, ads, assets, files, and all squad artifacts. Consistent naming enables searchability, organization, and automated processing.

---

## Campaign Names

**Format:** `[PLATFORM]_[OBJECTIVE]_[GEO]_[FUNNEL]_[OFFER]_[PERIOD]`

### Platform Codes
| Code | Platform |
|------|----------|
| `META` | Meta (Facebook/Instagram) |
| `GOOG` | Google Ads (Search, Display, YouTube) |
| `TIKTOK` | TikTok Ads |
| `LI` | LinkedIn Ads |
| `SNAP` | Snapchat Ads |
| `PIN` | Pinterest Ads |
| `TWITTER` | X (Twitter) Ads |
| `PROG` | Programmatic (DV360, The Trade Desk) |

### Objective Codes
| Code | Objective |
|------|-----------|
| `CONV` | Conversions |
| `SEARCH` | Search / Intent-based |
| `LEAD` | Lead generation |
| `TRAF` | Traffic / Clicks |
| `AWARE` | Awareness / Reach |
| `VID` | Video views |
| `APP` | App installs |
| `SHOP` | Shopping / Catalog |
| `BRAND` | Brand campaigns |

### Geography Codes
| Code | Region |
|------|--------|
| `US` | United States |
| `UK` | United Kingdom |
| `CA` | Canada |
| `AU` | Australia |
| `EU` | European Union |
| `GLOBAL` | Global / Multi-region |
| `[ISO]` | Use ISO 3166-1 alpha-2 for others |

### Funnel Stage Codes
| Code | Stage |
|------|-------|
| `TOFU` | Top of funnel (cold / awareness) |
| `MOFU` | Middle of funnel (consideration) |
| `BOFU` | Bottom of funnel (decision / conversion) |
| `COLD` | Cold prospecting |
| `WARM` | Warm / engaged audiences |
| `HOT` | Hot / high-intent audiences |
| `RT` | Retargeting |
| `CX` | Customer / post-purchase |

### Period Codes
| Format | Usage |
|--------|-------|
| `2026Q1` | Quarterly |
| `2026-03` | Monthly |
| `2026W10` | Weekly |
| `AO` | Always-on (no end date) |

### Examples
- `META_CONV_US_TOFU_FreeTrial_2026Q1`
- `GOOG_SEARCH_US_BRAND_CoreProduct_2026Q1`
- `TIKTOK_CONV_US_COLD_UGCtest_2026-03`
- `LI_LEAD_US_MOFU_Whitepaper_2026Q2`
- `META_CONV_UK_RT_CartAbandoners_AO`

---

## Ad Set / Ad Group Names

**Format:** `[AUDIENCE]_[TARGETING]_[BID]`

### Audience Type Codes
| Code | Audience Type |
|------|---------------|
| `LAL1` | Lookalike 1% |
| `LAL3` | Lookalike 3% |
| `LAL5` | Lookalike 5% |
| `LAL10` | Lookalike 10% |
| `INT` | Interest-based |
| `BROAD` | Broad / open targeting |
| `RT` | Retargeting |
| `CRM` | CRM / customer list |
| `ENGAGER` | Engagers (social, video, page) |
| `WEB` | Website visitors |
| `PURCH` | Past purchasers |
| `LEAD` | Lead list |

### Bid Strategy Codes
| Code | Strategy |
|------|----------|
| `Auto` | Automatic / lowest cost |
| `tCPA[XX]` | Target CPA of $XX |
| `tROAS[XX]` | Target ROAS of X.Xx |
| `MaxConv` | Maximize conversions |
| `Manual` | Manual bidding |
| `BidCap[XX]` | Bid cap of $XX |
| `CostCap[XX]` | Cost cap of $XX |

### Examples
- `LAL1_Purchasers180d_tCPA30`
- `INT_Skincare_F2545_Auto`
- `RT_SiteVisitors7d_Manual`
- `BROAD_US_2565_CostCap25`
- `CRM_HighValueCustomers_tROAS4`

---

## Ad / Creative Names

**Format:** `[FORMAT]_[HOOK]_[ANGLE]_[VERSION]`

### Format Codes
| Code | Format |
|------|--------|
| `VID` | Video |
| `STAT` | Static image |
| `CAR` | Carousel |
| `COL` | Collection |
| `DYN` | Dynamic creative |
| `GIF` | Animated GIF |
| `UGC` | User-generated content style |
| `STORY` | Stories / Reels format |
| `TEXT` | Text-only (search, text ads) |

### Hook Codes
| Code | Hook Type |
|------|-----------|
| `QuestionHook` | Question-based opener |
| `StatHook` | Statistic / data opener |
| `StoryHook` | Story / narrative opener |
| `BoldClaim` | Bold claim opener |
| `Contrast` | Contrarian / controversial |
| `Testimonial` | Testimonial / social proof |
| `Demo` | Product demonstration |
| `Problem` | Problem statement |

### Angle Codes
| Code | Angle |
|------|-------|
| `PainAngle` | Pain / problem agitation |
| `DesireAngle` | Desire / aspiration |
| `ProofAngle` | Proof / results / case study |
| `AuthAngle` | Authority / expertise |
| `UrgAngle` | Urgency / scarcity |
| `CuriAngle` | Curiosity / intrigue |
| `SocAngle` | Social proof |

### Version Format
- `v1`, `v2`, `v3` — Sequential versions
- `vA`, `vB`, `vC` — A/B test variants within the same version

### Examples
- `VID_QuestionHook_PainAngle_v1`
- `STAT_BoldClaim_ProofAngle_v3`
- `CAR_Testimonial_DesireAngle_v1`
- `UGC_StoryHook_PainAngle_v2`
- `VID_StatHook_AuthAngle_vA`

---

## UTM Parameters

### Standard Parameters
| Parameter | Convention | Examples |
|-----------|-----------|----------|
| `utm_source` | Platform name (lowercase) | `meta`, `google`, `tiktok`, `youtube`, `linkedin` |
| `utm_medium` | Channel type (lowercase, hyphens) | `paid-social`, `cpc`, `paid-video`, `display`, `shopping` |
| `utm_campaign` | Campaign name (lowercase, hyphens) | `meta-conv-us-tofu-freetrial-2026q1` |
| `utm_content` | Creative ID | `cre-001`, `vid-questionhook-painangle-v1` |
| `utm_term` | Keyword or audience ID | `aud-001`, `brand+keyword` |

### Rules
1. All UTM values must be lowercase
2. Use hyphens as word separators (not underscores or spaces)
3. Campaign UTM should map directly to the campaign name
4. Content UTM should enable creative-level attribution
5. Never use special characters or spaces in UTM values
6. Document all UTM conventions in a shared tracking sheet

---

## Registry IDs

Sequential IDs for all tracked entities:

| Entity | Format | Examples |
|--------|--------|----------|
| Campaigns | `CMP-001` | `CMP-001`, `CMP-042` |
| Creatives | `CRE-001` | `CRE-001`, `CRE-156` |
| Audiences | `AUD-001` | `AUD-001`, `AUD-033` |
| Experiments | `EXP-001` | `EXP-001`, `EXP-017` |
| Offers | `OFR-001` | `OFR-001`, `OFR-008` |
| Landing Pages | `LP-001` | `LP-001`, `LP-023` |
| Decisions | `DEC-001` | `DEC-001`, `DEC-099` |
| Lessons | `LES-001` | `LES-001`, `LES-045` |
| Reports | `RPT-001` | `RPT-001`, `RPT-012` |

### Rules
- IDs are never reused, even if the entity is archived
- Zero-pad to 3 digits minimum (expand as needed: `CMP-1001`)
- IDs are assigned sequentially at creation time
- Cross-reference IDs between registries for relationships

---

## File Naming

### Documentation & Resource Files
- Use `kebab-case.md` for all markdown files
- Examples: `getting-started.md`, `campaign-launch-script.md`, `hooks-headlines.md`

### Data Files
- Use `kebab-case.yaml` for YAML data files
- Examples: `campaigns-registry.yaml`, `weekly-scorecards.yaml`

### Asset Files
- Use descriptive names with format and dimensions
- Examples: `hero-image-1200x628-v1.png`, `product-demo-60s-v2.mp4`

---

## General Rules

1. **All codes are uppercase** except UTM parameters and file names (which are lowercase)
2. **Use underscores** as separators in campaign/ad set/ad names
3. **Use hyphens** as separators in file names and UTM values
4. **No spaces** in any names, anywhere
5. **Keep names under 100 characters** — platforms may truncate longer names
6. **Include version numbers** for any iterated asset
7. **Be consistent** — once a convention is established, follow it without exception
8. **Document exceptions** — if a deviation is necessary, document the reason in the decisions log
9. **Review quarterly** — update codes and conventions as platforms and needs evolve
