# Budget Reallocation Script — Automation Script

> Budget reallocation decision tree automation for optimizing spend distribution across campaigns and channels.

---

## Purpose

Systematically evaluate campaign-level efficiency and reallocate budget from underperformers to top performers, maximizing overall account performance within the total budget constraint.

---

## Trigger / Schedule

- **Primary trigger:** Weekly optimization cycle (Step 2)
- **Alert trigger:** Budget pacing anomaly or significant efficiency change
- **Scheduled trigger:** Monthly budget review
- **Duration:** 20-40 minutes per account
- **Owner:** Budget Agent
- **Supporting Agents:** Optimization Agent, Strategy Agent

---

## Pre-Conditions

- [ ] At least 7 days of performance data since last reallocation
- [ ] All campaigns have exited learning phase (or learning phase is documented)
- [ ] KPI targets current in config.yaml
- [ ] Total budget for the period confirmed
- [ ] Previous reallocation results reviewed

---

## Step-by-Step Workflow

### Step 1: Performance Ranking (10 minutes)

```yaml
action: Rank all active campaigns by marginal efficiency
for_each_campaign:
  calculate:
    - Current CPA (or inverse ROAS)
    - 7-day trend (improving, stable, declining)
    - Budget utilization percentage
    - Marginal CPA at current spend level
    - Headroom assessment (can it absorb more spend?)
  classify:
    tier_1_star:
      criteria: "CPA < 0.8x target AND stable/improving AND budget constrained"
      label: "Strong candidate for budget increase"
    tier_2_solid:
      criteria: "CPA within 0.8x-1.1x target AND stable"
      label: "Maintain current budget"
    tier_3_watch:
      criteria: "CPA within 1.1x-1.3x target OR declining trend"
      label: "Monitor; potential source for reallocation"
    tier_4_underperform:
      criteria: "CPA > 1.3x target for 7+ days"
      label: "Reduce budget; reallocate to Tier 1"
    tier_5_critical:
      criteria: "CPA > 2x target for 7+ days"
      label: "Significant reduction or pause"
output: Ranked campaign list with tier classification
```

### Step 2: Reallocation Decision Tree (10 minutes)

```yaml
action: Apply decision tree to determine reallocation
decision_tree:
  step_1:
    question: "Are there Tier 1 (star) campaigns that are budget-constrained?"
    yes: "Proceed to identify reallocation sources"
    no: "No reallocation needed. Maintain current allocation."

  step_2:
    question: "Are there Tier 4-5 campaigns to reduce?"
    yes: "Calculate available budget from reductions"
    no: "Consider increasing total budget (escalate to stakeholder)"

  step_3:
    question: "Does the available amount from reductions cover Tier 1 needs?"
    yes: "Execute reallocation"
    no: "Prioritize Tier 1 campaigns by marginal CPA. Allocate best-first."

reallocation_rules:
  - Maximum single campaign increase: 30% (to avoid learning phase reset)
  - Maximum single campaign decrease: 50% (to allow gradual wind-down)
  - Minimum campaign budget: platform minimum or $10/day (whichever is higher)
  - Reallocation must net to zero (total budget stays the same unless approved)
  - Learning phase campaigns: do not adjust
  - Test campaigns: do not adjust (protect test integrity)
```

### Step 3: Impact Projection (5 minutes)

```yaml
action: Project the impact of proposed reallocation
calculate:
  for_each_change:
    - Campaign being increased: projected additional conversions based on marginal CPA
    - Campaign being decreased: projected conversion loss based on current CPA
    - Net impact: total projected gain minus total projected loss
    - Projected blended CPA change
  validation:
    - Net impact must be positive (more total conversions at same or lower blended CPA)
    - If net impact is negative or neutral, reconsider the reallocation
output: Reallocation proposal with projected impact
```

### Step 4: Approval Check (5 minutes)

```yaml
action: Determine if approval is required
rules:
  auto_approve:
    criteria: "Individual change < $[config threshold] AND total reallocation < [config threshold]"
    action: "Proceed to implementation"
  requires_approval:
    criteria: "Individual change > $[config threshold] OR total reallocation > [config threshold]"
    action: "Submit proposal to Account Manager / Stakeholder for approval"
  always_approve:
    criteria: "Total budget change (increase/decrease) of any amount"
    action: "Always requires stakeholder approval"
```

### Step 5: Implementation (5 minutes)

```yaml
action: Execute approved reallocation
steps:
  - Apply budget changes in ad platform
  - Stagger changes if multiple campaigns (don't change all at once)
  - Verify new budget amounts are reflected
  - Set monitoring checkpoints for next 3-7 days
  - Update campaign registry with new budget amounts
documentation:
  decisions_log:
    - Decision ID
    - Date
    - Type: budget_change
    - Description: specific amounts moved between campaigns
    - Rationale: tier classification and projected impact
    - Status: implemented
    - Review date: [7 days from implementation]
```

### Step 6: Post-Reallocation Monitoring (ongoing)

```yaml
action: Monitor impact of reallocation
checkpoints:
  day_3:
    check: "Are increased campaigns spending the additional budget?"
    check: "Are decreased campaigns maintaining conversion volume?"
  day_7:
    check: "Has blended CPA improved as projected?"
    check: "Are any campaigns in unintended learning phase?"
    decision:
      improved: "Document success, consider further optimization"
      no_change: "Allow more time, check at day 14"
      worsened: "Evaluate if reallocation should be reversed"
```

---

## Decision Points

| Condition | Action |
|-----------|--------|
| Star campaign budget-constrained | Increase budget from underperformers |
| No clear underperformers to reduce | Maintain allocation or request total budget increase |
| Reallocation nets negative projected impact | Do not execute; maintain current allocation |
| Campaign enters learning phase after change | Allow learning to complete before further changes |
| Reallocation worsens performance after 7 days | Revert change and investigate root cause |

---

## Output / Deliverables

- Campaign efficiency ranking with tier classification
- Reallocation proposal with projected impact
- Updated budget allocations in ad platform
- Decisions log entry
- Updated campaign registry
- Monitoring schedule for post-reallocation period

---

## Post-Conditions

- [ ] All campaigns ranked and classified
- [ ] Reallocation executed (or decision to maintain documented)
- [ ] Budget changes verified in platform
- [ ] Registries and logs updated
- [ ] Monitoring checkpoints scheduled
- [ ] Net projected impact is positive
