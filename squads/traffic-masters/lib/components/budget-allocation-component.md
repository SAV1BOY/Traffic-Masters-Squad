# Budget Allocation Component

## Purpose
Framework for distributing budget across platforms, campaigns, and funnel stages.

## Allocation Frameworks

### 70-20-10 Rule
- **70% Proven:** Campaigns and creatives with demonstrated performance
- **20% Promising:** Tests showing early positive signals
- **10% Experimental:** New ideas, platforms, or approaches

### By Funnel Stage
| Stage | Recommended % | Rationale |
|-------|--------------|-----------|
| Prospecting (TOFU) | 60-70% | Volume and scale |
| Consideration (MOFU) | 15-20% | Nurture and educate |
| Conversion (BOFU) | 10-20% | Close and convert |
| Retention | 5-10% | Loyalty and LTV |

### By Platform
- Allocate based on marginal CPA (next dollar efficiency)
- Minimum viable spend per platform to exit learning phase
- Cap platform concentration at 70% to manage risk

## Component Fields
- `budget_id`: Identifier
- `total_budget`: Available amount
- `period`: Timeframe
- `allocation_method`: Rule used for distribution
- `platform_split`: Amounts by platform
- `funnel_split`: Amounts by funnel stage
- `reserve`: Emergency / opportunity fund (5-10%)

## Reallocation Triggers
1. Platform CPA exceeds guardrail for 7+ days
2. New platform test shows 20%+ better efficiency
3. Seasonal demand shift requires adjustment
4. Creative fatigue on primary platform

## Review Cadence
- Daily: Pacing check
- Weekly: Minor reallocation (up to 10% shift)
- Monthly: Major reallocation review
