# Channel Diversification

> **Type**: Task
> **Category**: scaling
> **Agents**: Traffic Chief, Pittman
> **Frameworks**: Channel Expansion Framework, Portfolio Diversification Model
> **Checklists**: channel-diversification-checklist
> **Output template**: templates/channel-expansion-plan.md

## ROUTING (from config.yaml)

> **Config key**: `routing.channel-diversification`
> **Agents**: [traffic-chief](../../agents/traffic-chief.md), [molly-pittman](../../agents/molly-pittman.md)
> **Frameworks**: `pittman-traffic-engine-9-steps`, `omnichannel-media-strategy`
> **Checklists**: `cross-platform-consistency-quality`
> **Templates**: `plans/media-plan-template`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Diversify the advertising portfolio into new channels to reduce platform dependency risk, access new audiences, and find incremental growth opportunities beyond the primary acquisition channels.

## Inputs
- Current channel performance and concentration analysis
- Platform feasibility assessment for untapped channels
- Budget available for new channel testing
- Creative assets adaptable to new platforms
- ICP presence data across potential channels
- Competitive intelligence on channel usage

## Steps
1. Assess current channel concentration: what percentage of spend and revenue comes from each platform
2. Identify concentration risk: if primary channel performance drops 30%, what is the business impact
3. Evaluate candidate channels from the platform feasibility assessment
4. Prioritize channels by: audience overlap (low is better), creative adaptability, expected CPA, learning curve
5. Design minimum viable test for each candidate channel: budget, duration, creative, targeting
6. Adapt existing creative assets for new platform requirements and native styles
7. Set up tracking and attribution for new channels
8. Define success criteria: what performance level justifies ongoing investment
9. Launch pilot campaigns on top two candidate channels
10. Run pilots for minimum 2-4 weeks with sufficient budget for statistical significance
11. Evaluate pilot results against success criteria and incremental lift analysis
12. Graduate successful pilots to ongoing channels with dedicated budget allocation

## Output
Channel expansion plan containing: concentration risk assessment, candidate channel evaluations, pilot test designs, adapted creative plans, success criteria, pilot timeline, and graduation framework.

## Quality Gate
- Channel diversification checklist confirms concentration risk quantified
- Pilot designs include proper tracking and incrementality measurement
- Pittman validates new channels align with customer journey and offer strategy

## Duration
3-4 hours for assessment and planning; pilots run 2-4 weeks with weekly reviews
