# Tracking Stack Standard
> **Type**: Technical Implementation Framework
> **Used by agents**: Pixel Specialist, Performance Analyst, Media Buyer

## Overview
The standard tracking infrastructure required for accurate measurement and optimization. Covers pixel implementation, Conversions API (CAPI), Google Tag Manager (GTM), GA4 configuration, CRM integration, event taxonomy, deduplication, governance, QA cadence, and privacy compliance. No campaign launches without a validated tracking stack.

## When to Use
- New account setup (mandatory before any campaign launch)
- Auditing existing tracking for accuracy and completeness
- Adding new conversion events or tracking requirements
- Troubleshooting data discrepancies between platforms
- Privacy regulation changes requiring tracking updates

## The Framework

### Layer 1: Pixel (Browser-Side)
- Meta Pixel, Google Tag (gtag), TikTok Pixel, LinkedIn Insight Tag
- Fires on page load and user interactions via browser JavaScript
- Subject to ad blockers, ITP, and cookie restrictions
- Necessary but insufficient alone — must pair with CAPI

### Layer 2: Conversions API (Server-Side)
- Meta CAPI, Google Enhanced Conversions, TikTok Events API
- Fires from server, bypasses browser limitations
- Requires event_id matching with pixel for deduplication
- Improves match rates by 20-40% over pixel alone

### Layer 3: Google Tag Manager (GTM)
- Central tag management for all pixels and events
- Server-side GTM preferred for CAPI implementation
- Data layer standardization across all pages
- Version control and approval workflows for tag changes

### Layer 4: GA4 (Google Analytics 4)
- Central analytics platform. Event-based model.
- Configure key events: page_view, lead, purchase, add_to_cart
- Link to Google Ads for conversion import
- Enable enhanced measurement and cross-domain tracking

### Layer 5: CRM Integration
- Offline conversion import for lead-gen businesses
- Match CRM stages (MQL, SQL, Customer) back to ad platforms
- Enables optimization for downstream quality, not just lead volume

### Events to Track
- Standard: PageView, ViewContent, AddToCart, InitiateCheckout, Purchase, Lead
- Custom: BookDemo, StartTrial, UpgradeSubscription, Refund

### Deduplication
- Use event_id parameter to match pixel and CAPI events
- Without deduplication, conversions are double-counted
- Test deduplication in Events Manager before scaling spend

### QA Cadence
- Pre-launch: Full tracking audit (pixel helper, CAPI diagnostics, test conversions)
- Weekly: Spot-check event counts between platform and GA4
- Monthly: Full reconciliation of platform conversions vs CRM/backend data
- Quarterly: Comprehensive tracking audit including privacy compliance

### Privacy Compliance
- Consent management platform (CMP) for GDPR/CCPA
- Respect ATT opt-out signals on iOS
- First-party data collection strategy to offset signal loss

## Key Concepts
- Pixel + CAPI together is the minimum standard; pixel alone is insufficient
- Deduplication is non-negotiable — double-counted conversions distort optimization
- GA4 is the source of truth for cross-platform analytics
- CRM integration transforms lead-gen from volume game to quality game

## Decision Rules
1. No campaign launches until tracking is validated end-to-end
2. CAPI must be implemented for any channel spending over $1,000/month
3. Any data discrepancy >15% between platform and backend triggers investigation
4. Privacy consent must be implemented before any EU-targeted campaign

## Integration
- Feeds into: All measurement, attribution, and optimization workflows
- Pairs with: Attribution and Incrementality, iOS Privacy Framework
- Required by: Tracking Layer (stack layer execution)

## Output
- Tracking implementation checklist per platform
- Event taxonomy document with naming conventions
- Deduplication validation report
- QA audit report with pass/fail per event
- Privacy compliance documentation
