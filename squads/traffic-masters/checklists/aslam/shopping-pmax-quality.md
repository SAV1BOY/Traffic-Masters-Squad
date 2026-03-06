# Shopping + PMax Dual Strategy Quality Gate

> Quality gate for Kasim Aslam's Shopping + Performance Max dual strategy for e-commerce. Must pass before the combined Shopping/PMax architecture is launched.

## Section 1: Product Feed Quality
- [ ] Product titles include primary keyword, brand, key attributes (color, size, material)
- [ ] Product descriptions are detailed and keyword-rich (not manufacturer defaults)
- [ ] Product images meet Google's requirements (white background, no watermarks, high resolution)
- [ ] GTINs, MPNs, and brand attributes are populated for all eligible products
- [ ] Product categories are mapped to the most specific Google Product Category
- [ ] Custom labels are applied to segment products by margin, price tier, or performance group

## Section 2: Standard Shopping Campaign Structure
- [ ] Standard Shopping campaign is structured by product performance tiers (heroes, mid, long-tail)
- [ ] Top-performing products are isolated in dedicated campaigns with higher bids
- [ ] Campaign priority settings are used strategically (High, Medium, Low) to control query routing
- [ ] Negative keywords funnel traffic between Shopping campaigns by query intent
- [ ] Manual CPC or Enhanced CPC is used in Standard Shopping for bid control

## Section 3: Performance Max Configuration
- [ ] PMax campaign has well-organized asset groups by product category or theme
- [ ] Final URLs are set to specific product or category pages (not just homepage)
- [ ] Text assets (headlines, descriptions) are diverse and keyword-informed
- [ ] Image assets include product images, lifestyle images, and branded graphics
- [ ] Video assets are included (Google will auto-generate low-quality video if none provided)
- [ ] Audience signals are configured with custom segments, customer lists, and in-market audiences

## Section 4: Shopping + PMax Coexistence
- [ ] Both Standard Shopping and PMax campaigns can run simultaneously without destructive overlap
- [ ] Brand exclusions are applied in PMax to prevent it from stealing branded traffic
- [ ] Product-level performance is monitored in PMax (not just campaign-level aggregates)
- [ ] Standard Shopping serves as a control group to benchmark PMax performance
- [ ] Budget allocation between Shopping and PMax is strategic (not arbitrary 50/50)

## Section 5: Measurement & Optimization
- [ ] Product-level ROAS is tracked and used for bid/budget decisions
- [ ] New vs. returning customer revenue is segmented in reporting
- [ ] Search term insights in PMax are reviewed for quality and relevance
- [ ] Asset group performance is analyzed to identify which groups drive results
- [ ] Low-performing products are excluded or moved to separate low-bid campaigns
- [ ] Feed optimization is an ongoing process (not set-and-forget)

## Approval
- **Minimum pass rate**: 21/25 items (84%)
- **Reviewer**: aslam-google-ads-strategist
- **Escalation**: If product feed quality items fail, fix the feed before launching any Shopping or PMax campaign; garbage in = garbage out
