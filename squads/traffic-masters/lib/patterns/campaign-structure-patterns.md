# Campaign Structure Patterns

## Purpose
Proven campaign architecture patterns across platforms.

## Pattern 1: Funnel-Based Structure
```
Account
├── Prospecting Campaign (TOFU)
│   ├── Ad Set: Broad
│   ├── Ad Set: Interest 1
│   └── Ad Set: Lookalike 1%
├── Consideration Campaign (MOFU)
│   ├── Ad Set: Site Visitors 7d
│   └── Ad Set: Video Viewers 50%
├── Conversion Campaign (BOFU)
│   ├── Ad Set: ATC 7d
│   └── Ad Set: Leads 14d
└── Retention Campaign
    └── Ad Set: Customers (excl recent)
```

## Pattern 2: CBO Consolidated
- 1 campaign per objective, broad targeting
- Let platform AI optimize across audiences
- Best for: Meta Advantage+, Google PMax

## Pattern 3: Testing Structure
```
Testing Campaign (limited budget)
├── Ad Set: Hook Test (5 hooks, same body)
├── Ad Set: Angle Test (3 angles, same hook)
└── Ad Set: Format Test (video vs static vs carousel)
```

## Pattern 4: Geo/Market Split
- Separate campaigns by country/region
- Allows budget control per market
- Different CPA targets per market

## Selection Guide
| Situation | Pattern |
|-----------|---------|
| New account, small budget | CBO Consolidated |
| Mature account, large budget | Funnel-Based |
| Creative testing phase | Testing Structure |
| Multi-market | Geo Split |

## Anti-Patterns to Avoid
1. Too many ad sets (audience fragmentation)
2. Overlapping audiences without exclusions
3. Mixing objectives in one campaign
4. Testing and scaling in same campaign
