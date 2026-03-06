# Scaling Plan Template

> **Type**: Template
> **Category**: plans
> **Used by tasks**: campaign-scaling, budget-increase, growth-planning
> **Filled by agents**: media-buyer-agent, strategist-agent

## Purpose
Documents the plan for scaling proven campaigns from current performance to higher spend levels, defining the scaling method, budget increase schedule, guardrails, rollback triggers, and creative pipeline needed to support growth.

## Template

### Plan Metadata
**Plan name**: [campaign or account scaling plan]
**Campaign(s) to scale**: [list campaigns]
**Platform(s)**: [Meta / Google / YouTube / TikTok]
**Current daily spend**: [amount]
**Target daily spend**: [amount]
**Timeline**: [start date to target date]
**Owner**: [person or agent]

### Current Performance Baseline
| Metric | Current Value | Date Range | Trend |
|---|---|---|---|
| Daily spend | [amount] | [last 7/14/30 days] | [stable/increasing/decreasing] |
| CPA | [amount] | [range] | [trend] |
| ROAS | [ratio] | [range] | [trend] |
| CTR | [percentage] | [range] | [trend] |
| CVR | [percentage] | [range] | [trend] |
| CPM | [amount] | [range] | [trend] |
| Frequency | [number] | [range] | [trend] |
| Daily conversions | [number] | [range] | [trend] |

**Stability assessment**: [Is performance stable enough to scale? Yes/No with reasoning]

### Scaling Method
**Primary method**: [Vertical / Horizontal / Mixed]

#### Vertical Scaling
**Approach**: Increase budget on existing winning ad sets.
**Budget increase schedule**:
| Day | Current Budget | New Budget | Increase % |
|---|---|---|---|
| Day 1 | [amount] | [amount] | 20% |
| Day 4 | [amount] | [amount] | 20% |
| Day 7 | [amount] | [amount] | 20% |
| Day 10 | [amount] | [amount] | 20% |
| Day 14 | [amount] | [amount] | 20% |
**Rule**: Never increase budget by more than 20% per increment.
**Wait period**: Minimum 3 days between increases to exit learning phase.

#### Horizontal Scaling
**Approach**: Duplicate winning ad sets to new audiences or structures.
**Duplication plan**:
| Original Ad Set | New Ad Set | Audience Change | Budget |
|---|---|---|---|
| [winner 1] | [duplicate name] | [new LAL / broader interest / new geo] | [amount] |
| [winner 1] | [duplicate name] | [different audience] | [amount] |
| [winner 2] | [duplicate name] | [new audience] | [amount] |
**New audiences to test**: [list audiences not yet tested]
**New campaign structures**: [CBO vs ABO, Advantage+ campaigns]

#### Mixed Scaling
**Vertical targets**: [which campaigns get budget increases]
**Horizontal targets**: [which campaigns get duplicated]
**New channel expansion**: [add TikTok, YouTube, etc.]

### Budget Increase Schedule
| Week | Daily Budget | Weekly Spend | Cumulative Spend | Notes |
|---|---|---|---|---|
| Week 1 | [amount] | [amount] | [amount] | Baseline hold |
| Week 2 | [amount] | [amount] | [amount] | First vertical increase |
| Week 3 | [amount] | [amount] | [amount] | Horizontal expansion |
| Week 4 | [amount] | [amount] | [amount] | Combined scaling |

### Guardrails
| Metric | Green (Continue) | Yellow (Monitor) | Red (Pause/Rollback) |
|---|---|---|---|
| CPA | Below [X] | [X] to [Y] | Above [Y] |
| ROAS | Above [X] | [X] to [Y] | Below [Y] |
| Frequency | Below [X] | [X] to [Y] | Above [Y] |
| CPM | Below [X] | [X] to [Y] | Above [Y] |
| CTR | Above [X]% | [X]% to [Y]% | Below [Y]% |

**Monitoring cadence**: [check metrics every 24 hours during scaling]

### Rollback Triggers
**Trigger 1**: CPA exceeds [X]% above baseline for 3 consecutive days
- **Action**: Reduce budget to last stable level
**Trigger 2**: ROAS drops below [X] for 48 hours
- **Action**: Pause most recent scaling action
**Trigger 3**: Creative frequency exceeds [X] across primary audience
- **Action**: Pause and refresh creative, then resume
**Trigger 4**: CPM spikes [X]% without corresponding performance improvement
- **Action**: Investigate audience saturation, test new audiences

### Creative Needs
**Current creative count**: [winning creatives available]
**Creatives needed for scaling**: [estimate - typically 2-3x current at 2x spend]
**Creative pipeline**:
| Week | New Creatives Needed | Format | Status |
|---|---|---|---|
| Week 1 | [count] | [format] | [planned/in-production/ready] |
| Week 2 | [count] | [format] | [status] |
| Week 3 | [count] | [format] | [status] |
| Week 4 | [count] | [format] | [status] |
**Notes**: Creative fatigue is the number one scaling killer. Pipeline must stay ahead of spend.

### Risk Assessment
**Primary risk**: [creative fatigue / audience saturation / CPM inflation / tracking loss]
**Mitigation**: [creative pipeline, audience expansion, channel diversification]
**Contingency budget**: [amount held in reserve for unexpected performance drops]

## Usage Notes
- Do not scale campaigns that have not achieved stable performance for at least 7 days.
- Scale gradually; aggressive scaling resets learning phases and destabilizes algorithms.
- Review scaling plan weekly and adjust based on real performance data.

## Example
Meta campaign at $200/day with $35 CPA. Scaling to $500/day over 4 weeks using mixed method: vertical 20% increases every 3 days on primary ad set, plus horizontal duplication to 3 new LAL audiences. 8 new creatives in pipeline.

## Related
- media-plan-template.md
- launch-brief.md
- creative-production-plan.md
