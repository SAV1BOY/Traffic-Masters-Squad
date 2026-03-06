# Dynamic Creative Optimization
> **Type**: Creative Strategy Framework
> **Used by agents**: Media Buyer, Ad Midas, Creative Analyst, Performance Analyst

## Overview
Framework for leveraging platform-native dynamic creative tools to test multiple asset combinations at scale. DCO allows the algorithm to serve the best-performing combination of headline, image/video, copy, and CTA to each user. Covers when to use DCO vs manual testing, setup methodology, and critical limitations.

## When to Use
- Large product catalogs requiring personalized ad experiences
- Multiple audience segments with unknown creative preferences
- Scale phase where manual A/B testing cannot keep pace with volume
- When sufficient conversion data exists (50+ conversions/week)
- Testing multiple creative elements simultaneously

## The Framework

### Setup: Asset Groups
- Organize assets by product category or theme
- Per group: 5+ headlines, 5+ descriptions, 5+ images, 1+ video
- Each element must be meaningfully different, not trivially altered
- Any random assembly of elements should make coherent sense together

### Headline/Image/Description Variations
- Headlines: Test different angles — benefit, feature, CTA, social proof, urgency
- Images: Test lifestyle vs product vs UGC vs graphic vs before/after
- Descriptions: Test long vs short, emotional vs rational, story vs direct

### Meta Advantage+ Creative
- Upload up to 10 images/videos, 5 primary texts, 5 headlines, 5 descriptions
- Set optimization event (purchase, lead, add to cart)
- Let system run minimum 7 days before drawing conclusions
- Review breakdown by asset to identify winners

### Google Responsive Ads
- RSA: Up to 15 headlines, 4 descriptions. Pin critical headlines sparingly.
- Performance Max: Runs across all Google surfaces with automated creative assembly
- Audience signals are suggestions, not restrictions

### Limitations
- **Black Box**: Cannot see which specific combination served to which user
- **Less Control**: Algorithm decides distribution, not the marketer
- **Creative Learning Loss**: DCO tells you what won but not deeply why
- **Cannibalization Risk**: ASC/PMax can cannibalize branded search if not configured with exclusions
- **Fatigue Masking**: DCO rotates assets, potentially hiding overall decline

### DCO vs Manual Testing
- DCO: Fast, many combinations, low control, opaque significance
- Manual A/B: Slow, one variable, high control, clear significance
- Use DCO for scale optimization, manual for deep creative learning

## Key Concepts
- Combinatorial scale: 5 images x 5 headlines x 5 descriptions = 125 combinations
- Algorithm favors clicks over conversions if optimization event is set wrong
- Graduate winners from DCO to standalone ads for maximum control
- DCO is a tool, not a strategy — always have a creative hypothesis

## Decision Rules
1. Never rely solely on DCO — maintain manual testing for strategic learning
2. Review asset breakdowns weekly; remove consistently underperforming assets
3. ASC and PMax require brand exclusion lists — non-negotiable
4. Graduate winning combinations to standalone ads every 30 days
5. If DCO performance declines, inject new assets before pausing
6. Minimum 50 conversions/week per ad set for reliable DCO optimization

## Integration
- Assets from creative production pipeline and creative angle matrix
- Account structure accommodates DCO campaigns per platform standards
- Winners feed back into hook library with performance tags
- Scaling decisions connect to scaling playbook

## Output
- DCO campaign setup documentation with asset inventory
- Weekly asset performance breakdown report
- Monthly winner extraction log — top combinations moved to standalone
- Quarterly DCO vs manual test performance comparison
