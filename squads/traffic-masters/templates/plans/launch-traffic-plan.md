# Launch Traffic Plan

> **Type**: Template
> **Category**: plans
> **Used by tasks**: campaign-launch, phased-rollout, new-product-launch
> **Filled by agents**: strategist-agent, media-buyer-agent

## Purpose
Operationalizes the Sobral 8-stage launch methodology into a detailed traffic plan with specific budgets, audiences, creatives, KPIs, and contingencies per stage, serving as the execution roadmap for campaign launches.

## Template

### Plan Metadata
**Plan name**: [launch name]
**Product / offer**: [what is being launched]
**Total launch budget**: [amount]
**Launch start date**: [date]
**Estimated full-scale date**: [date]
**Platform(s)**: [Meta / Google / YouTube / TikTok]
**Owner**: [person or agent]

### Stage 1 - CBO Testing
**Budget**: [daily: amount, total: amount]
**Duration**: [5-7 days]
**Audience(s)**:
- [Audience A: broad / interest / LAL - details]
- [Audience B: details]
- [Audience C: details]
**Creative(s)**: [3-6 creatives across 2-3 angles]
**Campaign structure**: CBO with [X] ad sets
**KPI targets**: CPM < [X], CTR > [X]%, CPA < [X]
**Decision criteria**: Advance audiences and creatives with CPA within [X]% of target
**Contingency**: If no winners, test new angles before new audiences

### Stage 2 - ABO Validation
**Budget**: [daily: amount, total: amount]
**Duration**: [5-7 days]
**Audience(s)**: [Winners from Stage 1]
**Creative(s)**: [Winners from Stage 1]
**Campaign structure**: ABO with dedicated budgets per ad set
**KPI targets**: CPA < [X], CVR > [X]%, at least [X] conversions per ad set
**Decision criteria**: Confirm CPA holds under isolated budgets
**Contingency**: If CPA rises in ABO, review audience overlap and creative fatigue

### Stage 3 - Creative Expansion
**Budget**: [daily: amount, total: amount]
**Duration**: [7-10 days]
**Audience(s)**: [Validated audiences from Stage 2]
**Creative(s)**:
- [New hooks on winning angles]
- [New formats: carousel, static if video won, or vice versa]
- [New UGC if applicable]
**KPI targets**: At least [X] new winning creatives identified
**Decision criteria**: New creatives must meet or beat Stage 2 CPA
**Contingency**: If all new creatives lose, iterate on winning elements only

### Stage 4 - Audience Expansion
**Budget**: [daily: amount, total: amount]
**Duration**: [7-10 days]
**Audience(s)**:
- [New LAL percentages: 2%, 3%, 5%]
- [New interest groups]
- [Broad / open targeting]
- [New geographies]
**Creative(s)**: [Proven winners from Stages 2-3]
**KPI targets**: CPA within [120%] of Stage 2 baseline
**Decision criteria**: At least 2 new audiences performing acceptably
**Contingency**: If new audiences fail, focus on proven audiences and scale vertically

### Stage 5 - Vertical Scaling
**Budget**: [increasing daily budget, 20% increments every 3 days]
**Duration**: [14 days]
**Audience(s)**: [All validated audiences]
**Creative(s)**: [All winning creatives]
**KPI targets**: CPA within [130%] of baseline during scaling
**Scaling schedule**:
| Day | Daily Budget | Notes |
|---|---|---|
| Day 1-3 | [amount] | First increase |
| Day 4-6 | [amount] | Second increase |
| Day 7-9 | [amount] | Third increase |
| Day 10-14 | [amount] | Stabilize and monitor |
**Contingency**: If CPA spikes, hold at last stable budget for 5 days

### Stage 6 - Horizontal Scaling
**Budget**: [total across duplicated campaigns]
**Duration**: [ongoing]
**Audience(s)**: [Duplicated winning ad sets targeting new segments]
**Creative(s)**: [Winning creatives rotated across new structures]
**KPI targets**: Blended CPA across all campaigns within target
**Contingency**: Consolidate underperformers and reallocate budget to winners

### Stage 7 - Retargeting Build
**Budget**: [15-25% of total active spend]
**Duration**: [ongoing]
**Audience(s)**: [1-3d visitors, 4-7d visitors, 8-14d visitors, 15-30d visitors, cart abandoners, video viewers, engagers]
**Creative(s)**: [Window-specific creatives per retargeting-ad-template.md]
**KPI targets**: Retargeting CPA [50-70%] of prospecting CPA
**Contingency**: If retargeting underperforms, check pixel fires and audience sizes

### Stage 8 - Optimization and Maintenance
**Budget**: [steady-state daily budget]
**Duration**: [ongoing]
**Routine tasks**:
- Weekly: Refresh 2-3 creatives, review top/bottom performers
- Bi-weekly: Audience review, exclusion update, frequency check
- Monthly: Full performance review, strategy adjustment
**KPI monitoring**: Daily pacing report, weekly performance report
**Creative fatigue threshold**: Pause when frequency > [X] or CTR drops [X]%
**Contingency**: Maintain 2-week creative pipeline at all times

### KPIs Per Stage Summary
| Stage | Primary KPI | Target | Budget |
|---|---|---|---|
| Stage 1 | CPA | < [X] | [amount] |
| Stage 2 | CPA + Volume | < [X], [Y]+ conv | [amount] |
| Stage 3 | New winners | [X]+ creatives | [amount] |
| Stage 4 | New audiences | [X]+ performing | [amount] |
| Stage 5 | CPA at scale | < [130%] baseline | [amount] |
| Stage 6 | Blended CPA | < [target] | [amount] |
| Stage 7 | Retargeting CPA | < [70%] pros CPA | [amount] |
| Stage 8 | Stability | All KPIs in range | [amount] |

## Usage Notes
- Do not skip stages; each builds on validated learnings from the previous.
- Stages 1-4 are learning phases; do not scale prematurely.
- Document learnings from each stage in the learnings-log-template.md.

## Example
DTC brand launching new product on Meta with $20k budget over 8 weeks. Stage 1: $100/day testing 5 audiences and 6 creatives. Progresses through validation, expansion, and scaling to $500/day by Stage 5.

## Related
- launch-brief.md
- scaling-plan-template.md
- creative-production-plan.md
