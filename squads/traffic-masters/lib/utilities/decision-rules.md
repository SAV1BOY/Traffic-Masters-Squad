# Decision Rules

## Purpose
Pre-defined rules for common optimization decisions to ensure consistency.

## Creative Decisions

| Condition | Rule | Action |
|-----------|------|--------|
| Creative CPA > 1.5x target, 100+ spend | Kill | Pause creative |
| Creative CPA < target, 50+ conversions | Scale | Increase budget 20% |
| CTR < 0.5% after 5,000 impressions | Kill | Pause creative |
| Frequency > 3.0 in 7 days | Refresh | Rotate or replace |
| Hook rate < 15% (video) | Iterate | New hook, same body |

## Budget Decisions

| Condition | Rule | Action |
|-----------|------|--------|
| Spend pacing < 85% | Investigate | Check for delivery issues |
| Spend pacing > 115% | Cap | Set daily budget limit |
| Platform CPA > 1.3x target for 7 days | Reallocate | Shift 20% to better platform |
| Marginal CPA > 1.5x average | Hold | Stop scaling, optimize first |

## Audience Decisions

| Condition | Rule | Action |
|-----------|------|--------|
| Audience size < 10,000 | Expand | Broaden targeting or merge |
| Audience overlap > 30% | Consolidate | Merge overlapping audiences |
| Lookalike exhaustion (CPA rising) | Expand | Test higher % or new seed |
| Retargeting pool growing | Allocate | Increase retargeting budget |

## Campaign Decisions

| Condition | Rule | Action |
|-----------|------|--------|
| Campaign in learning phase | Wait | No changes for 7 days |
| Campaign stable for 14+ days | Test | Introduce new variable |
| Campaign CPA > 2x target for 5 days | Pause | Review and restructure |
| Seasonal event approaching | Prepare | Build audiences 30 days prior |

## Override Protocol
- Any rule can be overridden with documented rationale
- Log overrides in decisions-log.yaml
