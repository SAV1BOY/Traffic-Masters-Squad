# Tracking Layer

> **Type**: Stack Layer
> **Domain**: Measurement Infrastructure — Pixel, Analytics, Attribution
> **Used by agents**: Pixel Specialist, Performance Analyst, Media Buyer

## Overview

The Tracking Layer is the measurement backbone of the entire traffic operation. Without accurate tracking, every other layer operates on flawed data. This layer covers pixel implementation, Conversions API (CAPI), Google Tag Manager, GA4 configuration, UTM architecture, deduplication, and QA protocols. Tracking setup runs in parallel with creative production and must be verified before any campaign launches.

## When to Use

- New client onboarding (mandatory before any campaign launch)
- Platform expansion requiring new tracking implementation
- Tracking discrepancy investigation
- iOS/privacy update response
- Website or funnel migration
- Annual tracking audit

## The Framework

### Tracking Components

#### 1. Meta Pixel + CAPI
**Owner**: Pixel Specialist
**Duration**: 1-2 days

**Pixel Setup**:
- One pixel per ad account (standard).
- Install base pixel code via GTM or direct placement on all pages.
- Configure standard events: PageView, ViewContent, AddToCart, InitiateCheckout, Purchase, Lead, CompleteRegistration.
- Custom events for non-standard conversion actions.
- Verify events in Events Manager > Test Events tool.

**Conversions API (CAPI)**:
- Server-side tracking to supplement browser-side pixel.
- Required for reliable attribution post-iOS 14.5+.
- Implementation via: platform integration (Shopify, WordPress plugins), GTM server-side container, or custom API.
- Must send same events as pixel with matching event IDs for deduplication.
- Include user parameters: email (hashed), phone (hashed), IP, user agent, fbc/fbp cookies.

**Aggregated Event Measurement (AEM)**:
- Configure top 8 prioritized events per domain.
- Rank by business importance (Purchase > Lead > AddToCart > ViewContent).
- Verify domain ownership in Business Manager.

#### 2. Google Ads Conversion Tracking
**Owner**: Pixel Specialist
**Duration**: 1-2 days

- Google Ads conversion action created for primary conversion (Purchase, Lead).
- Enhanced Conversions enabled — sends hashed first-party data for better match rates.
- Conversion linker tag active in GTM.
- Attribution model: Data-Driven (default) or Last Click depending on account maturity.
- Conversion window: 30-day click, 1-day view for most accounts. Adjust for sales cycle.
- Import GA4 conversions for secondary conversion tracking.

#### 3. Google Tag Manager (GTM)
**Owner**: Pixel Specialist
**Duration**: 1-2 days

GTM is the centralized tag management system. All tracking implementations go through GTM.

**Standard Container Setup**:
- Meta Pixel (via partner tag or custom HTML)
- Google Ads Conversion Tracking
- Google Analytics 4 (GA4)
- Custom event triggers for key user actions
- Consent management integration (if applicable)

**Trigger Architecture**:
| Trigger | Type | Fires |
|---------|------|-------|
| All Pages | Page View | GA4 pageview, Meta PageView |
| Product Page View | Custom Event / URL match | ViewContent |
| Add to Cart | Custom Event / Button Click | AddToCart |
| Checkout Initiated | Custom Event / URL match | InitiateCheckout |
| Purchase Complete | Custom Event / URL match / Data Layer | Purchase (with value) |
| Lead Form Submit | Form Submission / Custom Event | Lead / CompleteRegistration |

**Data Layer**:
- Implement data layer on all conversion pages.
- Push transaction value, currency, order ID, product IDs.
- Order ID required for deduplication between pixel and CAPI.

#### 4. GA4 Configuration
**Owner**: Pixel Specialist
**Duration**: 1 day

- GA4 property created and linked to Google Ads.
- Enhanced Measurement enabled (scrolls, outbound clicks, site search, video engagement).
- Custom events configured for key conversion actions.
- Audiences created for remarketing: purchasers, cart abandoners, high-engagement visitors.
- Conversion events marked in GA4 admin.
- Data retention set to 14 months.
- Cross-domain tracking configured if applicable.
- UTM parameters auto-captured by GA4.

#### 5. UTM Architecture
**Owner**: Pixel Specialist, Media Buyer
**Duration**: 0.5 days

**Standard UTM Structure**:
```
utm_source = [platform] (meta, google, youtube, tiktok)
utm_medium = [campaign type] (cpc, cpm, social, video)
utm_campaign = [campaign name] (matches ad platform naming)
utm_content = [ad identifier] (ad name or creative ID)
utm_term = [keyword or audience] (search term or audience name)
```

**Rules**:
- All UTM values lowercase, no spaces (use hyphens or underscores).
- UTM builder template shared with all agents who create ads.
- Auto-tagging enabled on Google Ads (gclid) — UTMs are supplementary.
- Meta auto-parameters (fbclid) enabled by default.
- UTMs must be testable — click every ad destination before launch.

#### 6. Deduplication
**Owner**: Pixel Specialist
**Duration**: 0.5 days

When running both pixel (browser) and CAPI (server), the same conversion can be counted twice.

**Deduplication Method**:
- Use identical `event_id` parameter in both pixel and CAPI events.
- Generate unique event ID per conversion (order ID, lead ID, or UUID).
- Meta automatically deduplicates events with matching event_id + event_name within 48 hours.
- Verify deduplication in Events Manager — check "Event Match Quality" score.
- Target Event Match Quality: Good or Great (above 6/10).

### QA Protocol

#### Pre-Launch QA (Mandatory)

1. **Pixel Verification**: Use Meta Events Manager Test Events and Google Tag Assistant to verify all events fire on correct pages.
2. **CAPI Verification**: Check server events in Events Manager. Confirm events arriving with user parameters.
3. **GTM Preview Mode**: Walk through entire funnel in GTM preview, verifying each trigger fires correctly.
4. **Test Transaction**: Submit a real test conversion (purchase or lead). Verify it appears in all platforms within 1 hour.
5. **UTM Verification**: Click ad preview links. Verify UTMs pass to GA4 and CRM correctly.
6. **Deduplication Check**: After test transaction, verify only one conversion recorded (not duplicated).
7. **Cross-Device Test**: Verify tracking on desktop, mobile (iOS and Android), and tablet.
8. **Consent Check**: If consent management is active, verify tracking behaves correctly for opt-in and opt-out scenarios.

#### Ongoing QA (Monthly)

- Compare platform-reported conversions vs GA4 vs CRM. Variance should be under 20%.
- Check Event Match Quality score on Meta — flag if below 6/10.
- Verify no broken events (events that stopped firing).
- Audit GTM container for unused or conflicting tags.
- Confirm enhanced conversions still sending data on Google Ads.
- Test new pages or funnel changes for tracking coverage.

## Key Concepts

- **Server-Side Is Non-Negotiable**: Browser-only tracking loses 20-40% of conversions due to ad blockers, iOS restrictions, and cookie limitations. CAPI is required on all accounts.
- **Tracking Precedes Everything**: No campaign launches until tracking QA is passed. Period.
- **Attribution Is Approximate**: No tracking system captures 100% of conversions. Accept directional accuracy and use multiple data sources for triangulation.
- **Privacy Compliance**: Tracking must comply with GDPR, CCPA, and platform-specific data policies. Implement consent management where required.

## Decision Rules

1. Tracking QA must pass before any campaign activation — no exceptions.
2. CAPI must be implemented alongside pixel on all Meta accounts — browser-only is insufficient.
3. GTM is the standard tag management system — no hardcoded tags on websites.
4. Monthly tracking audit is mandatory — degradation happens silently.
5. Any website change (redesign, new pages, platform migration) triggers tracking re-verification.
6. UTM naming must follow the standard architecture — no freelancing on parameter values.

## Common Mistakes

- Launching campaigns before completing end-to-end tracking verification.
- Implementing pixel without CAPI and wondering why attribution is poor.
- Not using event IDs for deduplication — double-counting inflates conversion numbers.
- Hardcoding tracking scripts instead of using GTM — creates maintenance nightmares.
- Ignoring Event Match Quality scores on Meta.
- Not testing tracking on mobile devices — mobile often behaves differently.
- Setting up tracking once and never auditing — drift accumulates silently.

## Integration

- Tracking infrastructure supports all campaigns built in `media-buying-layer.md`.
- UTM data feeds `client-ops-handoff.md` CRM reconciliation.
- Conversion data drives `pacing-and-guardrails.md` metric monitoring.
- Attribution data informs `optimization-layer.md` decisions.
- Measurement plan defined in `strategy-layer.md` — tracking layer implements it.
- Platform-specific tracking connects to `account-structure-meta.md` and `account-structure-google.md`.

## Output

- Tracking implementation document with all tags, triggers, and variables.
- Pre-launch QA checklist (completed and signed off by Pixel Specialist).
- Event mapping document — every tracked event with parameters and platforms.
- UTM naming convention sheet for all agents.
- Monthly tracking health report with discrepancy analysis.
- Deduplication verification log.
