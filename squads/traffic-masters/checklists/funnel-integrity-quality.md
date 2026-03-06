# Funnel Integrity Quality
> **Type**: Quality Gate
> **Domain**: Funnel Architecture
> **Reviewed by**: Funnel Architect

## Purpose
Ensures every step of the funnel is functional, congruent, and optimized for conversion before traffic is sent. Broken funnels waste budget and destroy trust.

## Checklist

### Step-by-Step Flow
- [ ] Every page in the funnel has a single, clear next action
- [ ] Navigation distractions are minimized or removed on conversion pages
- [ ] The logical sequence makes sense from the prospect's perspective
- [ ] No dead-end pages exist anywhere in the funnel
- [ ] Exit intent or abandonment recovery is configured where appropriate

### Messaging Congruence
- [ ] Ad copy promise matches the landing page headline
- [ ] Landing page messaging matches the checkout or form page
- [ ] Thank-you page messaging confirms what the user just did
- [ ] Tone and voice are consistent across all funnel steps
- [ ] Visual branding is consistent from ad to final confirmation

### Tracking at Transitions
- [ ] Every step transition fires an appropriate tracking event
- [ ] Funnel stage events are correctly named and parameterized
- [ ] UTM parameters persist through the entire funnel
- [ ] Cross-domain tracking is configured if multiple domains are used
- [ ] Event firing has been verified in a live test environment

### Link Integrity
- [ ] All internal links have been clicked and verified
- [ ] All external links open correctly and in the intended tab
- [ ] Form submissions lead to the correct destination
- [ ] No 404 or error pages exist in the funnel path
- [ ] Redirect chains are minimal (two hops maximum)

### Mobile Experience
- [ ] All funnel pages are fully responsive on mobile devices
- [ ] Forms are easy to complete on mobile with appropriate input types
- [ ] Buttons are large enough for thumb tapping (minimum 44px)
- [ ] Text is readable without zooming on standard mobile screens
- [ ] Pop-ups and modals work correctly on mobile

### Page Speed
- [ ] All funnel pages load in under 3 seconds on mobile
- [ ] Images are compressed and properly sized
- [ ] Unnecessary scripts are deferred or removed
- [ ] Core Web Vitals meet acceptable thresholds

### Thank-You Page Optimization
- [ ] Thank-you page confirms the action and sets expectations
- [ ] Next steps are clearly communicated
- [ ] Upsell, cross-sell, or referral opportunity is presented if appropriate
- [ ] Conversion tracking fires on the thank-you page
- [ ] Social sharing or additional engagement is encouraged

## Pass/Fail Criteria
All checklist items must pass. Any broken link, missing tracking event, or non-functional mobile element blocks launch.

## If Failed
Flag specific issues with screenshots and device details. Fix and retest within 24 hours. Conduct a full walkthrough on desktop and mobile before re-submitting.

## Related
- `landing-page-quality.md`
- `tracking-plan-quality.md`
- `pixel-and-capi-quality.md`
