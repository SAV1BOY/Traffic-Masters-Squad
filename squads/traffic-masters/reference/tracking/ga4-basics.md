# GA4 Basics Reference
> **Tool**: Google Analytics 4
> **Last Updated**: 2026-03

## Core Concepts
- Event-based data model (replaces session-based Universal Analytics)
- Every interaction is an event: page_view, click, scroll, purchase
- Parameters add context to events (e.g., item_name, value, currency)
- Users identified across sessions via User-ID, Google signals, device ID

## Key Event Types
- **Automatically collected**: page_view, session_start, first_visit, user_engagement
- **Enhanced measurement**: scroll, outbound_click, site_search, video_engagement, file_download
- **Recommended events**: add_to_cart, begin_checkout, purchase, sign_up, generate_lead
- **Custom events**: Any event specific to your business (e.g., quiz_complete, plan_selected)

## Conversion Setup
- Mark any event as a conversion in Admin > Events
- Primary conversion: the main action you optimize for (purchase, lead)
- Key events: secondary actions that indicate progress (add_to_cart, page_view of pricing)

## Audience Builder
- Create audiences based on events, parameters, user properties
- Audiences auto-sync to Google Ads for remarketing
- Predictive audiences: likely to purchase, likely to churn

## Attribution Models
- Data-driven attribution (default and recommended)
- Last click, first click available for comparison
- Attribution settings: reporting vs acquisition attribution

## Key Reports
- Realtime: live event monitoring
- Acquisition: traffic sources and campaigns
- Engagement: events, pages, and conversions
- Monetization: revenue, purchases, e-commerce
- Exploration: custom reports with funnels, paths, segments

## Key Takeaways
- GA4 is event-centric — think in events and parameters, not pageviews
- Configure Enhanced Measurement for quick wins
- Use recommended event names for compatibility with Google Ads
- Link GA4 to Google Ads for audience sharing and enhanced attribution
- Data retention set to 14 months for exploration reports
