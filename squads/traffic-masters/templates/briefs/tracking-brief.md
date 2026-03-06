# Tracking Brief

> **Type**: Template
> **Category**: briefs
> **Used by tasks**: tracking-setup, pixel-implementation, analytics-configuration
> **Filled by agents**: tracking-agent, analytics-agent

## Purpose
Defines all tracking requirements for a campaign or funnel, including events, UTM structure, pixel configuration, CAPI setup, GA4 events, attribution model, and QA procedures.

## Template

### Events to Track
| Event Name | Trigger | Parameters | Priority | Platform(s) |
|---|---|---|---|---|
| PageView | Page load | page_title, page_url | Required | Meta, GA4 |
| ViewContent | Product/landing page view | content_id, content_name, value | Required | Meta, GA4 |
| Lead | Form submission | form_name, lead_type | Required | Meta, Google, GA4 |
| AddToCart | Cart button click | content_id, value, currency | Required | Meta, GA4 |
| InitiateCheckout | Checkout start | value, currency, num_items | Required | Meta, GA4 |
| Purchase | Order confirmation | value, currency, order_id | Required | Meta, Google, GA4 |
| [Custom Event 1] | [trigger] | [params] | [priority] | [platforms] |
| [Custom Event 2] | [trigger] | [params] | [priority] | [platforms] |

### UTM Structure
**Pattern**: `utm_source=[platform]&utm_medium=[paid-type]&utm_campaign=[campaign-name]&utm_content=[creative-id]&utm_term=[keyword-or-audience]`

**Source values**: meta, google, youtube, tiktok, linkedin
**Medium values**: cpc, cpm, paid-social, paid-search, paid-video
**Campaign naming**: [reference campaign-naming-standard.md]
**Content naming**: [creative ID format]
**Term values**: [keyword or audience segment identifier]

### Pixel Requirements
**Meta Pixel ID**: [pixel ID]
**Google Ads Tag**: [conversion ID]
**TikTok Pixel**: [pixel ID]
**LinkedIn Insight Tag**: [partner ID]
**Installation method**: [GTM / hardcoded / plugin]
**Pages requiring pixel**: [list all pages]

### CAPI Setup
**Enabled**: [yes / no]
**Server-side platform**: [Shopify / WordPress / custom / Stape]
**Events sent via CAPI**: [list events]
**Deduplication method**: [event_id / fbp+timestamp]
**Test event code**: [code for testing]
**Gateway endpoint**: [URL if custom]

### GA4 Events
**Property ID**: [GA4 property ID]
**Measurement ID**: [G-XXXXXXX]
**Custom events**:
- [event_name]: [trigger and parameters]
- [event_name]: [trigger and parameters]
**Custom dimensions**: [list]
**Custom metrics**: [list]
**Enhanced measurement**: [which features enabled]

### Attribution Model
**Primary model**: [last-click / data-driven / first-click / linear / MER]
**Attribution window**: [7-day click, 1-day view / 28-day click / etc.]
**Cross-platform blending**: [how to reconcile platform vs GA4 data]
**MER calculation**: [total revenue / total ad spend formula]

### QA Plan
**Pre-launch QA**:
1. [ ] Verify pixel fires on all required pages
2. [ ] Confirm event parameters pass correct values
3. [ ] Test CAPI events in Events Manager
4. [ ] Validate deduplication (no double-counting)
5. [ ] Check UTM parameters render correctly on landing pages
6. [ ] Confirm GA4 events appear in DebugView
7. [ ] Test conversion tracking in platform dashboards

**Post-launch QA**:
1. [ ] Monitor event volume for anomalies in first 24 hours
2. [ ] Compare platform-reported vs GA4-reported conversions
3. [ ] Verify attribution windows are set correctly
4. [ ] Check for data loss or delays

## Usage Notes
- Complete this brief before any campaign goes live.
- Run the full QA checklist using qa-checklist-template.md.
- Update when new events, pages, or platforms are added.

## Example
Ecommerce brand running Meta + Google needs PageView, ViewContent, AddToCart, Purchase tracked via GTM with CAPI through Shopify, GA4 custom events for quiz completion, 7-day click attribution.

## Related
- event-map-template.md
- qa-checklist-template.md
- utm-standard.md
- data-layer-spec-template.md
