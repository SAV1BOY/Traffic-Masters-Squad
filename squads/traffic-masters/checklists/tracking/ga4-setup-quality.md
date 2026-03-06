# GA4 Property and Event Setup Quality Gate

> Quality gate for Google Analytics 4 property configuration and event tracking setup. Must pass before GA4 data is used for reporting or campaign optimization.

## Section 1: Property Configuration
- [ ] GA4 property is created with the correct property name, time zone, and currency
- [ ] Data stream is configured for the correct website URL (web stream) and/or app (iOS/Android streams)
- [ ] Measurement ID (G-XXXXXXXXXX) is installed on all pages via GTM or gtag.js
- [ ] Enhanced measurement is enabled for: page views, scrolls, outbound clicks, site search, video engagement, file downloads
- [ ] Internal traffic filters are configured to exclude office IPs, VPNs, and agency IPs
- [ ] Data retention is set to 14 months (maximum available)

## Section 2: Event Tracking
- [ ] Automatically collected events are verified: page_view, first_visit, session_start, user_engagement
- [ ] Enhanced measurement events are firing correctly (verified in DebugView)
- [ ] Custom events are created for key business actions: generate_lead, sign_up, purchase, add_to_cart, begin_checkout
- [ ] Event parameters are populated with relevant data: value, currency, items array (for e-commerce), method, content_type
- [ ] Event names follow GA4 conventions: lowercase, underscores, no spaces (max 40 characters)
- [ ] No more than 500 distinct event names are used (GA4 limit)

## Section 3: Conversions and Key Events
- [ ] Key conversion events are marked as "Key Events" (formerly "Conversions") in GA4 admin
- [ ] Conversion counting method is set correctly: "Once per event" for leads, "Once per session" or "Every" for purchases
- [ ] Conversion values are passed with the event (value and currency parameters)
- [ ] Google Ads is linked to GA4 for conversion import and audience sharing
- [ ] Google Search Console is linked for organic search data integration

## Section 4: Audiences and User Properties
- [ ] Remarketing audiences are created: All Users, Purchasers, Cart Abandoners, High-Value Users
- [ ] Predictive audiences are enabled where sufficient data exists (likely 7-day purchasers, likely churning users)
- [ ] User properties are configured for segmentation: user_type (new/returning), membership_level, etc.
- [ ] User-ID tracking is implemented for cross-device user identification (if applicable)
- [ ] Google Signals is enabled for cross-device reporting and demographics data

## Section 5: Reporting and Exploration
- [ ] Default channel grouping is validated (UTM-tagged traffic maps to correct channels)
- [ ] Custom dimensions and metrics are created for business-specific analysis needs
- [ ] Standard reports are reviewed: Acquisition, Engagement, Monetization, Retention
- [ ] At least one Exploration report is created for deep-dive analysis (Funnel, Path, Segment Overlap)
- [ ] BigQuery export is enabled for raw event data access (if applicable)
- [ ] Data quality indicators in reports show no sampling or thresholding issues for key reports

## Approval
- **Minimum pass rate**: 21/25 items (84%)
- **Reviewer**: analytics-agent
- **Escalation**: Missing conversion marking or broken Google Ads linking are hard blocks; must be resolved before GA4 data is used for optimization decisions
