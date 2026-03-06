# Google Conversion Tracking Quality Gate

> Quality gate for Google Ads conversion tracking setup and validation. Must pass before campaigns relying on conversion data are launched.

## Section 1: Google Tag Installation
- [ ] Google tag (gtag.js) or Google Tag Manager container is installed on all website pages
- [ ] Tag fires on every page load (verified via Google Tag Assistant browser extension)
- [ ] Tag ID matches the correct Google Ads account (AW-XXXXXXXXX)
- [ ] No duplicate Google tags exist on the same page (causes double-counting)
- [ ] Tag is placed in the <head> section for optimal loading priority

## Section 2: Conversion Action Configuration
- [ ] All required conversion actions are created in Google Ads: Purchase, Lead, Sign Up, Add to Cart
- [ ] Each conversion action has the correct category assigned (Purchase/Sale, Lead, Sign-up, etc.)
- [ ] Conversion value is configured: static value for leads, dynamic value for e-commerce transactions
- [ ] Conversion counting is set appropriately: "One" for leads, "Every" for purchases
- [ ] Click-through conversion window matches the sales cycle (default 30 days; adjust as needed)
- [ ] View-through conversion window is set (default 1 day for Search, customizable for Display/Video)

## Section 3: Enhanced Conversions
- [ ] Enhanced conversions for web are enabled and configured with first-party user data (email, phone, address)
- [ ] User data is hashed using SHA-256 before transmission (or auto-hashed by the tag)
- [ ] Enhanced conversions for leads are configured if using offline conversion import
- [ ] Consent mode v2 is implemented for EU/EEA traffic (basic or advanced mode)
- [ ] Consent signals are correctly passed to Google tags (ad_storage, analytics_storage, ad_user_data, ad_personalization)

## Section 4: Conversion Import and Offline Tracking
- [ ] Google Analytics 4 goals are imported into Google Ads (if using GA4 as the conversion source)
- [ ] Offline conversion import is scheduled (via GCLID upload, Salesforce, or HubSpot integration)
- [ ] GCLID capture is implemented on all lead forms and stored in the CRM
- [ ] Conversion upload latency is within 24 hours of the actual conversion event
- [ ] Imported conversions are validated against CRM data for accuracy

## Section 5: Data Validation
- [ ] Test conversions have been triggered and verified in Google Ads conversion tracking status
- [ ] Conversion action status shows "Recording conversions" (not "Unverified" or "No recent conversions")
- [ ] Conversion count in Google Ads is cross-referenced with backend analytics (within 15% tolerance)
- [ ] Tag diagnostics in Google Ads show no errors or warnings
- [ ] Conversion actions included in the "Conversions" column are intentionally selected (primary vs. secondary)

## Approval
- **Minimum pass rate**: 19/23 items (83%)
- **Reviewer**: tracking-specialist-agent
- **Escalation**: Unverified conversion actions or duplicate tags are hard blocks; must be resolved before campaign launch
