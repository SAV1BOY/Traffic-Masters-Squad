# Sample Size Calculator Guide

## Purpose
Determine the minimum sample size needed for statistically valid ad tests.

## Quick Reference Table

### For Conversion Rate Tests (95% confidence, 80% power)

| Baseline CVR | Minimum Detectable Effect | Sample Size Per Variant |
|-------------|--------------------------|------------------------|
| 1% | 50% relative lift (to 1.5%) | 23,000 |
| 2% | 25% relative lift (to 2.5%) | 12,000 |
| 3% | 20% relative lift (to 3.6%) | 6,500 |
| 5% | 20% relative lift (to 6.0%) | 3,800 |
| 10% | 15% relative lift (to 11.5%) | 2,500 |

### For CPA Tests
- Need minimum 100 conversions per variant (practical minimum)
- Ideal: 300+ conversions per variant for reliable results
- Duration: at least 7 days to account for day-of-week variation

## Key Concepts
- **Confidence Level:** Probability result is not random (target: 95%)
- **Statistical Power:** Probability of detecting a real effect (target: 80%)
- **Minimum Detectable Effect:** Smallest difference you can reliably detect

## Practical Rules of Thumb
1. If spending <$50/day per variant, expect 2-4 weeks to reach significance
2. For most ad tests, aim for 100+ conversions per variant minimum
3. The smaller the expected difference, the larger the sample needed
4. Never call a test early — false positives waste more than patience

## Tools
- Google Optimize sample size calculator
- Evan Miller's A/B test calculator (evanmiller.org)
- Optimizely's Stats Engine documentation

## When to Bend the Rules
- Very high CPA ($500+): Accept 30-50 conversions per variant
- Time-sensitive: Accept 90% confidence instead of 95%
- Large effect sizes (>50% lift): Smaller samples acceptable
