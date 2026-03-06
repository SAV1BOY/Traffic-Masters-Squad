# Tracking Layer
> **Type**: Stack Layer
> **Used by agents**: Pixel Specialist

## Overview
The Tracking Layer is the measurement backbone of the entire traffic operation. Without accurate tracking, every other layer operates on flawed data. Covers pixel implementation, Conversions API (CAPI), Google Tag Manager (GTM), GA4 configuration, UTM architecture, deduplication, and QA protocols. Runs in parallel with creative production. Duration: 2-5 days.

## When to Use
- New client onboarding (mandatory before any campaign launch)
- Platform expansion requiring new tracking implementation
- Tracking discrepancy investigation
- iOS/privacy update response
- Website or funnel migration

## The Framework

### 1. Pixel + CAPI Setup
- Install base pixel via GTM on all pages (Meta, Google, TikTok, LinkedIn)
- Configure standard events: PageView, ViewContent, AddToCart, InitiateCheckout, Purchase, Lead
- Custom events for non-standard conversion actions
- CAPI implementation: server-side tracking to supplement browser pixel
- CAPI via platform integration, GTM server-side container, or custom API
- Must send same events as pixel with matching event IDs for deduplication
- Include user parameters: email (hashed), phone (hashed), IP, user agent

### 2. Google Tag Manager (GTM)
- Central tag management for all tracking codes
- Data layer implementation on all conversion pages
- Push transaction value, currency, order ID, product IDs
- Trigger architecture: page views, button clicks, form submissions, URL matches
- Server-side GTM preferred for CAPI
- Version control and workspace management

### 3. GA4 Configuration
- GA4 property created and linked to Google Ads
- Enhanced measurement enabled (scrolls, outbound clicks, site search)
- Custom events for key conversion actions
- Audiences created for remarketing
- Data retention set to 14 months
- Cross-domain tracking if applicable

### 4. UTM Architecture
- Standard structure: utm_source, utm_medium, utm_campaign, utm_content, utm_term
- All values lowercase, no spaces (underscores only)
- UTM builder template shared with all agents who create ads
- Auto-tagging enabled (gclid for Google, fbclid for Meta)
- Every ad destination URL tested before launch

### 5. Deduplication
- Use identical event_id in both pixel and CAPI events
- Generate unique event ID per conversion (order ID, lead ID, or UUID)
- Verify in Events Manager — check Event Match Quality score
- Target: Good or Great (above 6/10)

### 6. QA Protocol
- **Pre-Launch (Mandatory)**: Pixel verification, CAPI verification, GTM preview walkthrough, test transaction, UTM verification, deduplication check, cross-device test, consent check
- **Monthly (Ongoing)**: Platform vs GA4 vs CRM comparison (variance under 20%), Event Match Quality check, broken event audit, GTM container audit, enhanced conversions verification

## Key Concepts
- Server-side tracking is non-negotiable: browser-only loses 20-40% of conversions
- Tracking precedes everything: no campaign launches until QA passes
- Attribution is approximate: accept directional accuracy, use multiple sources
- Privacy compliance: GDPR, CCPA, and platform-specific data policies

## Decision Rules
1. Tracking QA must pass before any campaign activation — no exceptions
2. CAPI alongside pixel on all Meta accounts — browser-only is insufficient
3. GTM is the standard — no hardcoded tags on websites
4. Monthly tracking audit is mandatory — degradation happens silently
5. Any website change triggers tracking re-verification
6. UTM naming must follow standard architecture

## Integration
- Tracking infrastructure supports all campaigns in Media Buying Layer
- UTM data feeds CRM reconciliation
- Conversion data drives pacing and guardrails monitoring
- Attribution data informs Optimization Layer decisions
- Measurement plan from Strategy Layer implemented here

## Output
- Tracking implementation document with all tags, triggers, and variables
- Pre-launch QA checklist (completed and signed off)
- Event mapping document — every tracked event with parameters
- UTM naming convention sheet for all agents
- Monthly tracking health report with discrepancy analysis
- Deduplication verification log
