# Tracking & Governance Guide

## Purpose
Standards for tracking setup, UTM management, and data governance.

## Tracking Stack
1. **Pixels:** Meta Pixel, Google Tag, TikTok Pixel, LinkedIn Insight Tag
2. **Server-Side:** CAPI (Meta), Enhanced Conversions (Google)
3. **Analytics:** GA4 with proper event configuration
4. **Tag Management:** Google Tag Manager (recommended)

## UTM Standards
- `utm_source`: Platform (meta, google, tiktok, youtube, linkedin)
- `utm_medium`: Ad type (cpc, cpm, paid-social, paid-video)
- `utm_campaign`: Campaign name (follow naming convention)
- `utm_content`: Creative identifier
- `utm_term`: Keyword or audience identifier

## Naming Convention
`[PLATFORM]_[OBJECTIVE]_[GEO]_[AUDIENCE]_[OFFER]_[DATE]`
Example: `META_CONV_US_LAL1_FreeTrial_2026Q1`

## Data Governance Rules
1. All tracking changes must be QA'd before going live
2. UTM parameters must follow the standard format
3. Conversion events must be verified weekly
4. Pixel health monitored daily
5. CAPI/server-side tracking is mandatory for primary platforms
6. Privacy compliance (consent mode, LGPD, GDPR) enforced

## QA Process
- Pre-launch: Verify all events fire correctly
- Post-launch: Monitor event match quality for 48 hours
- Weekly: Spot-check conversion accuracy
- Monthly: Full tracking audit

## Incident Response
- Tracking failure detected > notify team immediately
- Pause affected campaigns if conversion data is unreliable
- Document issue and resolution in decisions log
