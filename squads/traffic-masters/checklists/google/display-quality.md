# Google Display Network Campaign Quality Gate

> Quality gate for Google Display Network (GDN) campaign setup. Must pass before the campaign is enabled in Google Ads.

## Section 1: Campaign Settings
- [ ] Campaign type is explicitly set to Display (not Search with Display expansion)
- [ ] Campaign goal matches the funnel stage: Awareness (impressions/reach) or Retargeting (conversions)
- [ ] Geographic and language targeting match the media plan
- [ ] Ad schedule (dayparting) is configured based on audience activity data or set to all hours with monitoring
- [ ] Frequency capping is enabled: maximum 3-5 impressions per user per day for prospecting, 5-7 for retargeting

## Section 2: Targeting Configuration
- [ ] Targeting method is intentionally set to "Targeting" (not "Observation") for restrictive targeting
- [ ] Audience segments are appropriate: In-market, Affinity, Custom Intent, or Remarketing lists
- [ ] Custom intent audiences use relevant keywords and URLs (10-15 signals per audience)
- [ ] Placement targeting (if used) includes vetted, brand-safe websites and apps
- [ ] Content exclusion settings block sensitive categories (tragedy, conflict, sexually suggestive content)
- [ ] App category exclusions are applied to prevent wasted spend on accidental clicks in mobile games

## Section 3: Responsive Display Ads
- [ ] At least 5 unique marketing images (1200x628 landscape + 1200x1200 square) are uploaded
- [ ] At least 1 logo in both landscape (1200x300) and square (1200x1200) formats
- [ ] 5 unique headlines (max 30 characters each) with varied messaging angles
- [ ] 5 unique descriptions (max 90 characters each) with clear value propositions
- [ ] Long headline (max 90 characters) tells the complete value story
- [ ] Business name is accurate and consistent with the brand

## Section 4: Static Banner Ads (if applicable)
- [ ] All required sizes are provided: 300x250, 728x90, 160x600, 320x50 (mobile), 300x600
- [ ] File sizes are under 150KB per banner
- [ ] Animations do not exceed 30 seconds and loop no more than 3 times
- [ ] CTA is clearly visible and actionable in every banner size
- [ ] HTML5 banners are tested across Chrome, Safari, and Firefox

## Section 5: Landing Pages and Tracking
- [ ] Landing page is relevant to the ad creative and offer
- [ ] UTM parameters are appended to all destination URLs
- [ ] Conversion tracking is verified on the landing page (Google tag fires correctly)
- [ ] View-through conversion window is set appropriately (default 1 day; adjust with justification)
- [ ] Click-through conversion window matches the campaign attribution model

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: media-buyer-agent
- **Escalation**: Missing content exclusions or brand safety settings are a hard block; must be configured before launch
