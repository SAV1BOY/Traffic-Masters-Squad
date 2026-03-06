# Google Search Campaign Quality Gate

> Quality gate for Google Search campaign setup and configuration. Must pass before the campaign is enabled in Google Ads.

## Section 1: Campaign Settings
- [ ] Campaign type is set to Search (not accidentally Performance Max or Display)
- [ ] Campaign goal aligns with business objective (Sales, Leads, Website Traffic)
- [ ] Networks setting is reviewed: Search Partners and Display Network are intentionally included or excluded
- [ ] Geographic targeting matches the media plan (locations, radius targeting, or location groups)
- [ ] Location targeting is set to "Presence" (not "Presence or interest") unless intentionally broader

## Section 2: Bidding Strategy
- [ ] Bidding strategy matches the campaign maturity: Manual CPC for new campaigns, Target CPA/ROAS for campaigns with 30+ conversions/month
- [ ] Target CPA or Target ROAS values are based on historical data or realistic benchmarks
- [ ] Enhanced CPC is enabled or disabled with documented rationale
- [ ] Portfolio bid strategies are used only when campaigns share the same conversion goals
- [ ] Maximum CPC bid limits are set for automated strategies to prevent outlier spend

## Section 3: Ad Group Structure
- [ ] Each ad group contains tightly themed keywords (no more than 15-20 keywords per ad group)
- [ ] Single Keyword Ad Groups (SKAGs) or themed ad groups are used based on documented strategy
- [ ] Ad group names clearly describe the keyword theme (e.g., "Brand_Exact", "NonBrand_Running_Shoes")
- [ ] No ad group contains a mix of branded and non-branded keywords
- [ ] Each ad group has at least 1 Responsive Search Ad (RSA) with fully populated assets

## Section 4: Ad Copy Quality
- [ ] Each RSA has at least 10 unique headlines and 4 unique descriptions
- [ ] Headlines include the primary keyword in at least 3 positions
- [ ] Headlines include differentiators: pricing, promotions, USPs, social proof
- [ ] Descriptions contain a clear CTA and value proposition
- [ ] Ad customizers (countdown, location, keyword insertion) are used where appropriate
- [ ] Pin positions are used sparingly (only for compliance or critical messaging)

## Section 5: Extensions and Assets
- [ ] Sitelink extensions are configured with at least 4 sitelinks per campaign
- [ ] Callout extensions highlight key benefits (free shipping, 24/7 support, etc.)
- [ ] Structured snippet extensions display relevant categories
- [ ] Call extensions are enabled for campaigns targeting phone leads
- [ ] Image extensions are uploaded for eligible campaigns

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: media-buyer-agent
- **Escalation**: If bidding strategy or ad group structure items fail, campaign must be restructured before activation
