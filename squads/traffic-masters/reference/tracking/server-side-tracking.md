# Server-Side Tracking Guide
> **Category**: Advanced Tracking Implementation
> **Last Updated**: 2026-03

## Overview
Server-side tracking moves data collection from the user's browser to a server you control, improving data accuracy, reducing ad blocker impact, and enabling better privacy compliance.

## Architecture
1. Browser sends first-party data to YOUR server (not directly to Meta/Google)
2. Your server processes, enriches, and forwards data to ad platforms
3. Platform APIs receive server events alongside (or instead of) browser events

## Implementation Options
- **GTM Server-Side**: Google Tag Manager server container on Google Cloud or other hosting
- **Stape.io**: Managed GTM server-side hosting (simplified setup)
- **Custom Server**: Node.js, Python, or PHP server forwarding events via APIs
- **Platform Solutions**: Meta Gateway, Google Enhanced Conversions

## Benefits
- Bypasses ad blockers (events come from your domain, not third-party scripts)
- Improved data accuracy (server events are more reliable than browser events)
- Better privacy control (filter and redact data before sending to platforms)
- First-party cookies set by your server (longer cookie lifetime)
- Reduced page load time (fewer browser-side scripts)

## Key Considerations
- Hosting cost: server container requires compute resources ($50-200/month typical)
- Consent management: LGPD/GDPR consent still required before data processing
- Deduplication: must coordinate with browser-side events to avoid double-counting
- Maintenance: server infrastructure requires monitoring and updates

## Setup Steps
1. Choose hosting (Google Cloud, AWS, Stape, custom)
2. Deploy server-side GTM container or custom application
3. Configure custom domain (subdomain of your site for first-party context)
4. Set up client tags (receive data from browser)
5. Set up vendor tags (forward data to Meta CAPI, Google, etc.)
6. Implement deduplication with browser-side events
7. Test and validate all event flows

## Key Takeaways
- Server-side tracking is becoming standard for serious advertisers
- Start with Meta CAPI and Google Enhanced Conversions as priority
- Always set up a custom subdomain for first-party cookie context
- Monitor server health and data flow continuously
- Server-side does not eliminate need for consent — it improves data quality within consent
