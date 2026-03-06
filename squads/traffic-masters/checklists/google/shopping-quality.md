# Google Shopping / Performance Max Campaign Quality Gate

> Quality gate for Google Shopping and Performance Max campaign setup. Must pass before the campaign is enabled in Google Ads.

## Section 1: Merchant Center Setup
- [ ] Google Merchant Center account is verified and claimed for the website domain
- [ ] Product feed is approved with no critical errors (disapproved products below 5% of total catalog)
- [ ] Feed refresh schedule is set (at least daily for inventory/price changes)
- [ ] Product data quality: titles contain brand + product type + key attributes (color, size, material)
- [ ] Product descriptions are unique, accurate, and at least 150 characters
- [ ] GTINs/MPNs are populated for all applicable products (required for most countries)

## Section 2: Feed Optimization
- [ ] Product titles follow the recommended structure: Brand + Product Type + Attributes (color, size, gender)
- [ ] Product images meet specifications: white background for standard Shopping, lifestyle images for PMax
- [ ] Product categories use the most specific Google Product Category taxonomy available
- [ ] Custom labels (custom_label_0 through custom_label_4) are configured for campaign segmentation (margin tiers, best sellers, seasonality)
- [ ] Sale price and sale price effective date are populated for promotional items
- [ ] Shipping and tax settings are configured correctly in Merchant Center

## Section 3: Campaign Structure (Shopping)
- [ ] Standard Shopping campaigns are segmented by priority (High, Medium, Low) if using tiered strategy
- [ ] Product groups are subdivided logically (by brand, category, custom label, or item ID)
- [ ] Negative keywords are applied to filter irrelevant search queries
- [ ] Campaign priority settings prevent budget cannibalization between overlapping campaigns

## Section 4: Performance Max Configuration
- [ ] Asset groups contain: at least 5 headlines, 5 descriptions, 5 images, 1 video (YouTube), and logos
- [ ] Final URL expansion is intentionally enabled or disabled based on landing page strategy
- [ ] Audience signals include: customer lists, website visitors, in-market segments, and custom intent
- [ ] Search themes are populated with relevant keywords to guide the algorithm
- [ ] Brand exclusions are configured to prevent PMax from cannibalizing branded search campaigns

## Section 5: Measurement and Goals
- [ ] Conversion actions are set to the correct goal (Purchase with revenue values, not just page views)
- [ ] New customer acquisition goal is configured if prioritizing new customers over returning
- [ ] ROAS or CPA targets are set based on product margin data and historical performance
- [ ] Merchant Center is linked to Google Ads and Google Analytics 4
- [ ] Product-level reporting is enabled for granular performance analysis

## Approval
- **Minimum pass rate**: 21/25 items (84%)
- **Reviewer**: media-buyer-agent + feed-specialist-agent
- **Escalation**: Merchant Center disapprovals or feed errors above 5% are a hard block; must be resolved before launch
