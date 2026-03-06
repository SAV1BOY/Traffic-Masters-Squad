# Conversion Engine Setup Quality Gate

> Quality gate for Charley T. Burns' Conversion Engine setup. Must pass before the full-funnel conversion system is considered operational.

## Section 1: Pixel & Tracking Infrastructure
- [ ] Meta Pixel (or platform equivalent) is installed on all pages of the funnel
- [ ] Conversions API (CAPI) is configured for server-side event tracking
- [ ] Event deduplication is enabled to prevent double-counting between pixel and CAPI
- [ ] Standard events are mapped correctly (ViewContent, AddToCart, InitiateCheckout, Purchase, Lead)
- [ ] Custom events are created for micro-conversions (scroll depth, video views, button clicks)
- [ ] Event parameters include value, currency, and content IDs for dynamic remarketing

## Section 2: Conversion Event Hierarchy
- [ ] Primary conversion event is defined (the one the algorithm optimizes toward)
- [ ] Secondary events are tracked but not used as optimization targets
- [ ] Event priority is configured correctly in Aggregated Event Measurement (AEM) for iOS
- [ ] Domain verification is complete for all tracked domains
- [ ] Event testing confirms all events fire correctly in the Events Manager test tool

## Section 3: Funnel Page Optimization
- [ ] Landing page loads in under 3 seconds on mobile
- [ ] Landing page has a single, clear CTA above the fold
- [ ] Form fields are minimized to reduce friction (name, email at minimum)
- [ ] Thank-you/confirmation page fires the correct conversion event
- [ ] Checkout or lead form is mobile-optimized with autofill support

## Section 4: Attribution & Reporting
- [ ] Attribution window matches the sales cycle (7-day click default, 28-day for high-ticket)
- [ ] UTM parameters are standardized across all campaigns for third-party attribution
- [ ] Dashboard or reporting template is built to show full-funnel metrics (CPM > CTR > CVR > CPA > ROAS)
- [ ] Offline conversions are imported if applicable (CRM integration or manual upload)

## Section 5: Quality Assurance
- [ ] End-to-end funnel test is completed by a team member (ad click through to conversion)
- [ ] Conversion data matches between the ad platform and the backend/CRM
- [ ] No duplicate conversions appear in reporting
- [ ] All links in ads resolve correctly (no 404s, no redirect chains)
- [ ] Conversion engine setup is documented for team reference and onboarding

## Approval
- **Minimum pass rate**: 20/25 items (80%)
- **Reviewer**: burns-performance-strategist
- **Escalation**: If pixel/CAPI tracking fails validation, halt all campaign launches until tracking is verified end-to-end
