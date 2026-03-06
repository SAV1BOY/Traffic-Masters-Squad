# Attribution Models Reference

> Comprehensive comparison of attribution models for paid traffic professionals: last-click, data-driven, multi-touch, and marketing mix modeling.

---

## 1. Why Attribution Matters

Attribution determines which ads, channels, and touchpoints get credit for conversions. The model you use directly affects:
- **Budget allocation**: Where you invest more/less
- **ROAS calculation**: Which campaigns appear profitable
- **Optimization decisions**: What to scale or cut
- **Reporting accuracy**: How stakeholders perceive performance

Choosing the wrong model can lead to over-investing in bottom-funnel channels and starving top-funnel growth.

---

## 2. Single-Touch Models

### Last-Click Attribution

**How it works**: 100% credit goes to the last click before conversion.

| Pros | Cons |
|------|------|
| Simple and easy to understand | Ignores all upper/mid-funnel touchpoints |
| Available in all platforms | Over-credits brand search and retargeting |
| Deterministic (no modeling) | Under-credits prospecting and awareness |
| Good for short purchase cycles | Leads to under-investment in discovery |

**Best for**: Direct response with short (<24h) consideration windows, single-channel advertisers.

**Platform defaults**:
- Google Ads: Data-driven (default since 2021)
- Meta: 7-day click, 1-day view (default)
- TikTok: 7-day click, 1-day view
- GA4: Data-driven (default), last-click available

### First-Click Attribution

**How it works**: 100% credit goes to the first touchpoint that introduced the user.

| Pros | Cons |
|------|------|
| Values top-of-funnel activity | Ignores nurturing and closing touchpoints |
| Useful for understanding acquisition | Over-credits awareness channels |
| Simple to implement | Under-credits retargeting and brand search |

**Best for**: Understanding which channels drive new audience acquisition.

### Last Non-Direct Click

**How it works**: 100% credit to the last click, excluding direct visits.

**Best for**: Legacy GA3/Universal Analytics default. Prevents direct traffic from getting credit when the actual driver was an earlier ad click.

---

## 3. Multi-Touch Attribution (MTA) Models

### Linear Attribution

**How it works**: Equal credit to every touchpoint in the conversion path.

```
Touchpoint 1 (FB Ad)  -> 25% credit
Touchpoint 2 (Google)  -> 25% credit
Touchpoint 3 (Email)   -> 25% credit
Touchpoint 4 (Direct)  -> 25% credit
```

| Pros | Cons |
|------|------|
| Acknowledges all touchpoints | Treats all touches as equally important |
| Better than single-touch | No distinction between awareness and closing |
| Easy to understand | May over-credit incidental touchpoints |

### Time Decay Attribution

**How it works**: More credit to touchpoints closer to conversion. Uses a half-life model (typically 7 days).

```
Day 1: FB Ad       -> 10% credit
Day 5: Google Ad   -> 20% credit
Day 12: Email      -> 30% credit
Day 14: Brand Search -> 40% credit
```

| Pros | Cons |
|------|------|
| Recognizes recency effect | Still under-credits awareness |
| Better than last-click for long cycles | Arbitrary half-life parameter |
| Intuitive logic | Penalizes early touchpoints that may be essential |

**Best for**: Products with 2-4 week consideration cycles.

### Position-Based (U-Shaped) Attribution

**How it works**: 40% to first touch, 40% to last touch, 20% split among middle touchpoints.

```
First touch (FB Ad)     -> 40% credit
Middle (Google Display)  -> 10% credit
Middle (Email)          -> 10% credit
Last touch (Brand Search) -> 40% credit
```

| Pros | Cons |
|------|------|
| Values both discovery and closing | Arbitrary weight distribution |
| Better for full-funnel analysis | Middle touches may be undervalued |
| Balanced view | Still relatively simplistic |

**Best for**: Advertisers investing in both prospecting and retargeting.

### W-Shaped Attribution

**How it works**: 30% to first touch, 30% to lead creation, 30% to opportunity creation, 10% split among rest.

**Best for**: B2B with defined lead-to-opportunity pipeline.

---

## 4. Data-Driven Attribution (DDA)

### How It Works

Machine learning analyzes all conversion paths (converting and non-converting) to determine the actual contribution of each touchpoint based on its impact on conversion probability.

### Google's Data-Driven Attribution

**Available in**: Google Ads, GA4

**Requirements**:
- Google Ads: 600 conversions in 30 days (for Search); 3,000 clicks and 300 conversions for other campaign types
- GA4: Sufficient data volume (Google doesn't publish exact thresholds)

**How Google DDA works**:
1. Collects all conversion paths (converting + non-converting)
2. Uses Shapley value game theory to calculate each touchpoint's marginal contribution
3. Compares paths with and without each touchpoint
4. Assigns fractional credit based on actual contribution

**Advantages over rule-based**:
- Based on your actual data, not arbitrary rules
- Adapts as user behavior changes
- Accounts for ad interaction order, timing, creative, and device
- Better budget allocation signals

**Limitations**:
- Black box (limited transparency into how credit is assigned)
- Requires sufficient data volume
- Only considers Google touchpoints (within Google Ads)
- GA4 DDA considers all channels but still has data gaps

### Meta's Attribution

Meta uses its own modeled attribution:
- **Default**: 7-day click, 1-day view
- **Aggregated Event Measurement (AEM)**: For iOS 14+ users, modeled using statistical inference
- **Conversion lift studies**: Available for measuring incrementality

Meta's attribution is self-reported and tends to favor Meta channels. Cross-reference with GA4 or third-party tools.

---

## 5. Marketing Mix Modeling (MMM)

### What It Is

MMM uses statistical regression to determine how different marketing channels (and external factors) drive a business outcome, using aggregate (not user-level) data.

```
Revenue = f(TV spend, Meta spend, Google spend, Email, Seasonality, Promotions, Economy, ...)
```

### How MMM Differs from MTA

| Aspect | MTA | MMM |
|--------|-----|-----|
| Data level | Individual user paths | Aggregate (weekly/monthly) |
| Privacy requirements | Needs user-level tracking | No user-level data needed |
| Channels covered | Digital only (tracked) | All channels (TV, radio, OOH, digital) |
| Time horizon | Real-time/daily | Historical (1-3 years) |
| Refresh frequency | Continuous | Monthly/quarterly |
| Accounts for external factors | No | Yes (seasonality, economy, competition) |
| Granularity | Campaign/ad level | Channel level |
| Implementation cost | Low-medium | Medium-high |

### Open-Source MMM Tools

| Tool | Developer | Language | Notes |
|------|-----------|----------|-------|
| **Meridian** | Google | Python | Google's open-source MMM; successor to LightweightMMM |
| **Robyn** | Meta | R | Meta's open-source MMM; well-documented |
| **PyMC-Marketing** | PyMC Labs | Python | Bayesian approach; flexible |
| **Orbit** | Uber | Python | Bayesian time series |

### Minimum Data Requirements for MMM

- 2-3 years of weekly data (recommended)
- At least 1 year minimum
- Spend data by channel per week
- Revenue/conversion data per week
- External factors (seasonality, promotions, competitor activity)
- Sufficient variation in spend (if you never change Meta spend, the model cannot measure its effect)

### When to Use MMM

- Spending $500K+/year across multiple channels
- Need to measure offline channels (TV, radio, OOH)
- Privacy restrictions limit user-level tracking
- Want to understand optimal budget allocation across channels
- Need to account for external factors in performance

---

## 6. Incrementality Testing

### What It Measures

Incrementality measures the true causal impact of advertising: "What conversions would NOT have happened without this ad?"

### Common Methods

**Geo-Based Lift Tests**:
1. Split regions into test (ads on) and control (ads off)
2. Run for 2-4 weeks
3. Compare conversion rates between test and control
4. Calculate incremental lift

**Conversion Lift (Platform-Native)**:
- Meta: Conversion Lift study (randomized holdout)
- Google: Brand Lift, Search Lift, Conversion Lift
- TikTok: Brand Lift studies

**Ghost Ads / PSA Tests**:
1. Show real ads to test group
2. Show public service announcements to control group
3. Compare conversion rates
4. Most accurate method for true incrementality

### Incrementality Formula

```
Incrementality = (Test Conversions - Control Conversions) / Test Conversions

iROAS = Incremental Revenue / Ad Spend
```

**Example**:
- Test group (saw ads): 1,000 conversions
- Control group (no ads): 700 conversions
- Incremental conversions: 300
- Incrementality: 30% (only 30% of conversions were truly caused by ads)
- If ad spend was $10,000 and incremental revenue was $15,000: iROAS = 1.5x

---

## 7. Practical Attribution Framework

### Recommended Multi-Model Approach

No single model tells the complete truth. Use multiple models together:

| Decision | Model to Use | Why |
|----------|-------------|-----|
| Daily optimization | Platform-native (DDA or default) | Fastest signal; campaign-level granularity |
| Weekly reporting | GA4 DDA + platform data | Cross-channel view with granularity |
| Monthly budget allocation | MMM or incrementality tests | Measures true channel contribution |
| Quarterly strategy | MMM + incrementality | Accounts for cannibalization and saturation |
| Annual planning | MMM | Long-term trends, saturation curves, optimal budget split |

### Cross-Platform Reconciliation

Platforms will always over-report (each claims credit for overlapping conversions):

| Source | Typical Over-Reporting |
|--------|----------------------|
| Meta Ads Manager | 10-30% vs. GA4 |
| Google Ads | 5-15% vs. GA4 |
| TikTok Ads Manager | 15-40% vs. GA4 |
| GA4 (last-click) | Baseline (tends to under-credit view-through) |

**Reconciliation approach**:
1. Use GA4 as the neutral baseline
2. Apply a "trust discount" to each platform's self-reported data
3. Use incrementality tests to calibrate the discount factors
4. Rebuild budget allocation based on calibrated data

---

## 8. Attribution Window Reference

### Default Attribution Windows

| Platform | Click Window | View Window |
|----------|-------------|-------------|
| Meta | 7 days | 1 day |
| Google Ads | 30 days | N/A (no view-through for Search) |
| Google Display | 30 days | N/A |
| TikTok | 7 days | 1 day |
| LinkedIn | 30 days | 7 days |
| Pinterest | 30 days | 1 day |

### Choosing Attribution Windows

| Business Type | Recommended Click | Recommended View | Reasoning |
|--------------|-------------------|------------------|-----------|
| E-commerce (<$50 AOV) | 7 days | 1 day | Short consideration; impulse purchases |
| E-commerce (>$200 AOV) | 14-28 days | 1 day | Longer research phase |
| SaaS (free trial) | 30 days | 1 day | Trial period + evaluation |
| B2B (enterprise) | 90 days | N/A | Long sales cycle |
| Lead gen (local services) | 7-14 days | 1 day | Medium consideration |
| Info products / courses | 7-14 days | 1 day | Launch urgency drives shorter cycles |

---

## 9. Common Attribution Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| Relying solely on platform self-reporting | Over-spend on claimed "winners" | Use GA4 + incrementality as calibration |
| Comparing different attribution windows | Apples-to-oranges comparisons | Standardize windows across platforms |
| Ignoring view-through | Under-crediting awareness campaigns | Include 1-day view in reporting |
| Over-trusting last-click | Under-investing in top-of-funnel | Use data-driven or position-based model |
| Not accounting for organic cannibalization | Brand search claims organic conversions | Run brand search incrementality tests |
| Changing models mid-campaign | Data discontinuity | Keep models consistent within measurement periods |

---

*Last updated: March 2026. The attribution landscape is shifting rapidly due to privacy changes. Invest in a multi-model approach that combines platform data, analytics tools, and experimental methods (incrementality testing).*
