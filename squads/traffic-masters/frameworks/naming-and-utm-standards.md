# Naming and UTM Standards
> **Type**: Operational Standards Framework
> **Used by agents**: Media Buyer, Pixel Specialist, Performance Analyst

## Overview
Standardized naming conventions for campaigns, ad sets, and ads across all platforms, plus UTM parameter standards for consistent cross-platform tracking. Without naming discipline, reporting becomes impossible at scale. All names use lowercase and underscores. No exceptions.

## When to Use
- Setting up any new campaign, ad set, or ad on any platform
- Building UTM parameters for any trackable link
- Onboarding new team members to the naming system
- Auditing existing accounts for naming compliance

## The Framework

### Campaign Naming Convention
Format: `[platform]_[objective]_[audience]_[stage]_[date]`

- **Platform**: meta, google, tiktok, linkedin, youtube
- **Objective**: awareness, traffic, leads, conversions, retargeting
- **Audience**: prospecting, lookalike, retarget, broad, custom_[name]
- **Stage**: tofu, mofu, bofu
- **Date**: YYYYMM or YYYYMMDD

Example: `meta_conversions_lookalike_bofu_202603`

### Ad Set Naming Convention
Format: `[audience_detail]_[targeting]_[placement]_[budget_type]`

- **Audience Detail**: lal_1pct, interest_fitness, broad_25_45, retarget_7d
- **Targeting**: us, uk, global, custom_geo
- **Placement**: auto, feed_only, stories, search, display
- **Budget Type**: cbo, abo, daily, lifetime

Example: `lal_1pct_us_auto_cbo`

### Ad Naming Convention
Format: `[creative_type]_[angle]_[hook]_[version]`

- **Creative Type**: static, video, carousel, ugc, animation
- **Angle**: pain_point, transformation, social_proof, authority
- **Hook**: question, statistic, bold_claim, story
- **Version**: v1, v2, v3

Example: `video_transformation_statistic_v2`

### UTM Parameters
- **utm_source**: Platform name (meta, google, tiktok, linkedin)
- **utm_medium**: Traffic type (cpc, cpm, social, email, organic)
- **utm_campaign**: Matches campaign name or shortened version
- **utm_content**: Ad identifier or creative descriptor
- **utm_term**: Keyword (search) or audience segment

### UTM Rules
- All lowercase, always
- Underscores for spaces, never hyphens or spaces
- No special characters
- Consistent across all team members and accounts
- Every paid traffic link must have UTMs — no exceptions

Example: `?utm_source=meta&utm_medium=cpc&utm_campaign=meta_conversions_lal_bofu_202603&utm_content=video_transformation_v2&utm_term=lookalike_1pct`

## Key Concepts
- Naming conventions enable automated reporting and bulk analysis
- UTMs are the bridge between ad platforms and analytics (GA4)
- Inconsistent naming makes historical analysis impossible
- The system must be simple enough that every team member follows it

## Decision Rules
1. Every campaign, ad set, and ad must follow the naming convention
2. UTMs are mandatory on every destination URL
3. Audit naming compliance monthly; flag and fix violations immediately
4. New platforms or objectives get added to the convention before use
5. Never use platform-generated default names

## Integration
- Feeds into: GA4 reporting, cross-platform dashboards, attribution analysis
- Pairs with: Tracking Stack Standard (UTMs feed analytics)
- Required by: All campaign creation workflows

## Output
- Naming convention reference document for the team
- UTM builder template (spreadsheet or tool)
- Monthly naming compliance audit report
- Updated convention when new platforms or objectives are added
