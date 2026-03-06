# Statistical Significance Guide

## Purpose
How to determine if ad test results are statistically significant.

## What Is Statistical Significance?
The probability that the observed difference between variants is real (not due to random chance). We target 95% confidence minimum.

## Quick Decision Framework

| Confidence | Interpretation | Action |
|-----------|---------------|--------|
| <80% | Not significant | Continue test, need more data |
| 80-90% | Directional | Lean toward winner, but not conclusive |
| 90-95% | Approaching significance | Consider implementing if time-constrained |
| 95%+ | Statistically significant | Implement winner with confidence |
| 99%+ | Highly significant | Strong result, high confidence |

## Common Pitfalls

### 1. Peeking Problem
- Checking results daily inflates false positive rate
- Set a check schedule: check only at predetermined intervals
- Or use sequential testing methods

### 2. Multiple Comparisons
- Testing 5 variants simultaneously increases false positive risk
- Apply Bonferroni correction: divide alpha by number of comparisons
- Or use A/B (2 variants) instead of A/B/C/D/E

### 3. Simpson's Paradox
- Aggregate results can hide segment-level differences
- Check results by device, day of week, and audience segment

### 4. Survivorship Bias
- Only analyzing winners ignores important learning from losers
- Document all test results, especially failures

## Practical Checklist
- [ ] Minimum 100 conversions per variant
- [ ] Test ran for at least 7 full days
- [ ] No major external events during test (holidays, outages)
- [ ] Single variable tested (isolated)
- [ ] Confidence level at 95%+
- [ ] Results consistent across segments

## Tools
- ABTestGuide.com/calc
- Neil Patel's A/B testing calculator
- Platform-native experiment tools (Meta Experiments, Google Experiments)
