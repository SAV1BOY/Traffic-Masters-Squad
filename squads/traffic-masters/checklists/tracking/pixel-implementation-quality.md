# Cross-Platform Pixel Implementation Quality Gate

> Quality gate for pixel implementation across all advertising platforms. Must pass before any conversion-optimized campaign is launched on any platform.

## Section 1: Pixel Inventory and Documentation
- [ ] All required platform pixels are documented: Meta Pixel, Google Tag, TikTok Pixel, LinkedIn Insight Tag, Twitter/X Pixel
- [ ] Each pixel ID is mapped to the correct advertising account and documented in the tracking sheet
- [ ] Pixel ownership and access permissions are documented (who has admin access to each pixel)
- [ ] A pixel implementation map shows which pixels fire on which pages/events
- [ ] Version control is maintained for pixel configurations (changes are logged with date, author, and reason)

## Section 2: Base Pixel Installation
- [ ] All base pixels fire a pageview event on every page of the website (verified per platform helper tool)
- [ ] Pixels load asynchronously and do not block page rendering
- [ ] No duplicate pixel installations exist for any platform on any page
- [ ] Pixel loading order is correct: consent manager > GTM container > platform pixels
- [ ] Base pixel fires correctly on both HTTP and HTTPS versions of the site (if applicable)

## Section 3: Event Pixel Configuration
- [ ] Standard events are mapped to the correct user actions for each platform (Purchase, Lead, AddToCart, etc.)
- [ ] Event naming is consistent across platforms where possible (standardized internal event taxonomy)
- [ ] Event parameters (value, currency, content_id, content_type) are populated correctly per platform requirements
- [ ] Dynamic values (transaction amount, product IDs) are pulled from the data layer, not hardcoded
- [ ] Custom events follow a documented naming convention (lowercase_with_underscores)

## Section 4: Cross-Platform Consistency
- [ ] The same conversion event fires all relevant platform pixels simultaneously (e.g., purchase triggers Meta, Google, TikTok)
- [ ] Conversion values are consistent across all platforms (same currency, same transaction amount)
- [ ] Event deduplication logic prevents the same conversion from being counted multiple times per platform
- [ ] Cross-domain tracking is configured if the user journey spans multiple domains
- [ ] Single Page Application (SPA) navigation triggers virtual pageview events across all pixels

## Section 5: Testing and Validation
- [ ] Each pixel has been tested using the platform's diagnostic tool (Meta Pixel Helper, Google Tag Assistant, TikTok Pixel Helper)
- [ ] End-to-end test conversions have been triggered and verified in each platform's event manager
- [ ] No JavaScript errors appear in the browser console related to pixel code
- [ ] Page load time impact of all pixels combined is under 500ms (measured via WebPageTest or Lighthouse)
- [ ] Pixel health monitoring is set up to alert on pixel firing failures or volume drops

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: tracking-specialist-agent
- **Escalation**: Duplicate pixels or missing base installations are hard blocks; must be fixed before any campaign relying on that pixel is launched
