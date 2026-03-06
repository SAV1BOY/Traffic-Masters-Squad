# Budget Allocator — Script Guide

## Purpose
Calculate optimal budget distribution across platforms and campaigns.

## Allocation Methods

### Method 1: 70-20-10 Rule
```
Proven Budget = Total Budget x 0.70
Testing Budget = Total Budget x 0.20
Experimental Budget = Total Budget x 0.10
```

### Method 2: Marginal CPA-Based
1. Rank campaigns by CPA (lowest to highest)
2. Allocate budget to lowest CPA first
3. Continue until marginal CPA exceeds target
4. Remaining budget goes to testing

### Method 3: ROAS-Weighted
```
Platform Weight = Platform ROAS / Sum of All Platform ROAS
Platform Budget = Total Budget x Platform Weight
```

## Example: $30K Monthly Budget

### By 70-20-10
| Bucket | Amount | Allocation |
|--------|--------|-----------|
| Proven | $21,000 | Top Meta + Google campaigns |
| Testing | $6,000 | New creative and audience tests |
| Experimental | $3,000 | TikTok pilot, new angles |

### By ROAS-Weighted
| Platform | ROAS | Weight | Budget |
|----------|------|--------|--------|
| Meta | 3.5x | 47% | $14,100 |
| Google | 4.0x | 53% | $15,900 |

## Guardrails
- No single platform exceeds 70% of total budget
- Testing budget never drops below 15%
- Minimum viable budget per platform maintained
- Reserve 5% for opportunities

## Reallocation Triggers
- Platform CPA exceeds 1.3x target for 7 days
- New platform test outperforms primary by 20%+
- Seasonal demand shift
- Creative fatigue on primary platform
