# Landing Page Optimization Quality Gate

> Quality gate for landing page optimization and conversion readiness. Must pass before a landing page is used as a campaign destination.

## Section 1: Message Match and Relevance
- [ ] Landing page headline matches the ad headline or promise (no disconnect between ad and page)
- [ ] Value proposition is immediately visible above the fold without scrolling
- [ ] Visual continuity exists between the ad creative and the landing page (same imagery, colors, tone)
- [ ] Landing page content addresses the specific audience segment targeted by the ad
- [ ] No navigation menu or unnecessary exit links that distract from the conversion goal (for dedicated landing pages)

## Section 2: Conversion Element Design
- [ ] Primary CTA is visible above the fold and uses action-oriented, specific text ("Get My Free Quote", not "Submit")
- [ ] CTA button has strong visual contrast against the page background (passes the squint test)
- [ ] CTA is repeated at logical intervals throughout the page (at least 2-3 times for long-form pages)
- [ ] Form fields are minimized to essential information only (each additional field reduces conversion rate ~7%)
- [ ] Social proof is present: testimonials, reviews, client logos, trust badges, case study excerpts
- [ ] Urgency or scarcity elements are used where authentic (countdown timers, limited availability, offer deadline)

## Section 3: Mobile Optimization
- [ ] Page is fully responsive and renders correctly on iPhone, Android, and tablet devices
- [ ] Touch targets (buttons, form fields, links) are at least 44x44px for easy tapping
- [ ] Font size is minimum 16px on mobile to prevent auto-zoom on form focus (iOS)
- [ ] No horizontal scrolling is required on any mobile viewport
- [ ] Images are optimized for mobile: appropriately sized, not causing layout shifts

## Section 4: Trust and Credibility
- [ ] SSL certificate is active (HTTPS) and no mixed content warnings appear
- [ ] Privacy policy link is accessible on the page
- [ ] Contact information or customer support access is available
- [ ] Trust signals are visible: security badges, money-back guarantee, industry certifications
- [ ] Page design is professional with no broken images, typos, or layout issues

## Section 5: Technical Performance
- [ ] Page loads in under 3 seconds on 4G mobile connections (tested via Google PageSpeed Insights)
- [ ] Largest Contentful Paint (LCP) is under 2.5 seconds
- [ ] No render-blocking resources delay visible content (critical CSS is inlined)
- [ ] All tracking pixels and tags fire correctly on the landing page (verified with platform helper tools)
- [ ] Thank-you/confirmation page loads correctly after form submission and fires conversion events

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: cro-specialist-agent
- **Escalation**: Missing CTA above fold, broken mobile experience, or page load above 5 seconds are hard blocks; page must be fixed before receiving paid traffic
