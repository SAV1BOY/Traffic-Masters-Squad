# Launch Brief

> **Type**: Template
> **Category**: briefs
> **Used by tasks**: campaign-launch, phased-rollout, scaling-prep
> **Filled by agents**: strategist-agent, media-buyer-agent

## Purpose
Orchestrates a structured campaign launch using the Sobral 8-stage methodology, defining budget, audience, creative, and KPIs per phase with contingency plans for each stage.

## Template

### Launch Type
**Type**: [new product / new market / new channel / relaunch / seasonal]
**Total launch budget**: [amount]
**Total launch timeline**: [start to full scale date]
**Responsible agents**: [list]

### Phase 1 - CBO Testing (Learning)
**Budget**: [daily budget]
**Duration**: [days]
**Audiences**: [broad / interest / LAL - list each]
**Creatives**: [number and types]
**Objective**: Identify winning audience-creative combinations
**KPI targets**: [CPM range, CTR floor, CPA ceiling]
**Exit criteria**: [minimum conversions before moving on]

### Phase 2 - ABO Validation
**Budget**: [daily budget]
**Duration**: [days]
**Audiences**: [winners from Phase 1]
**Creatives**: [winners from Phase 1]
**Objective**: Validate performance at ad-set level
**KPI targets**: [CPA, ROAS thresholds]
**Exit criteria**: [statistical confidence level]

### Phase 3 - Creative Testing
**Budget**: [daily budget]
**Duration**: [days]
**Audiences**: [validated audiences]
**Creatives**: [new variations of winning angles/hooks]
**Objective**: Expand creative winners
**KPI targets**: [CTR, hook rate, hold rate]
**Exit criteria**: [number of winning creatives needed]

### Phase 4 - Audience Expansion
**Budget**: [daily budget]
**Duration**: [days]
**Audiences**: [new LALs, broader interests, open targeting]
**Creatives**: [proven winners]
**Objective**: Find incremental reach at acceptable CPA
**KPI targets**: [CPA within 120% of Phase 2 baseline]
**Exit criteria**: [minimum 2 new audiences performing]

### Phase 5 - Budget Scaling (Vertical)
**Budget**: [increased daily budget, 20% increments]
**Duration**: [days]
**Audiences**: [all validated]
**Creatives**: [all winners]
**Objective**: Increase spend while maintaining efficiency
**KPI targets**: [CPA within 130% of baseline]
**Guardrails**: [max daily increase, rollback triggers]

### Phase 6 - Horizontal Scaling
**Budget**: [total daily across duplicated ad sets]
**Duration**: [ongoing]
**Audiences**: [duplicated winners + new segments]
**Creatives**: [rotated and refreshed]
**Objective**: Scale through duplication and diversification
**KPI targets**: [blended CPA target]

### Phase 7 - Retargeting Build
**Budget**: [percentage of total]
**Duration**: [ongoing]
**Audiences**: [site visitors, engagers, cart abandoners]
**Creatives**: [retargeting-specific: social proof, urgency, new angle]
**KPI targets**: [retargeting CPA, ROAS]

### Phase 8 - Optimization and Maintenance
**Budget**: [steady state daily budget]
**Duration**: [ongoing]
**Routine**: [weekly creative refresh, bi-weekly audience review]
**KPI monitoring**: [daily pacing, weekly performance reviews]
**Creative fatigue threshold**: [frequency cap, declining CTR trigger]

### Timeline Summary
| Phase | Start | End | Daily Budget | Cumulative Spend |
|---|---|---|---|---|
| Phase 1 | [date] | [date] | [amount] | [amount] |
| Phase 2 | [date] | [date] | [amount] | [amount] |
| ... | ... | ... | ... | ... |

### Contingency
**If Phase 1 fails**: [pivot angles, change offer, test new platform]
**If CPA exceeds ceiling by 50%**: [pause, audit funnel, revisit creative]
**If creative fatigue hits early**: [activate backup creative batch]
**Emergency pause criteria**: [conditions that trigger full stop]

## Usage Notes
- This brief is the master launch document; all phase-specific tasks reference it.
- Update phase results in real-time as the launch progresses.
- Conduct a post-mortem after Phase 4 to decide on scaling approach.

## Example
SaaS product launching on Meta with $15k total budget over 6 weeks, starting with $100/day CBO testing across 5 interest audiences and 6 creatives.

## Related
- launch-traffic-plan.md
- campaign-brief.md
- scaling-plan-template.md
