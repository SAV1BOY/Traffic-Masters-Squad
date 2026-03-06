# Creative Rotation Script — Automation Script

> Creative rotation and refresh automation for managing ad creative lifecycle and preventing fatigue.

---

## Purpose

Systematically monitor creative performance, detect fatigue, rotate assets, and maintain a healthy creative portfolio that sustains campaign performance over time.

---

## Trigger / Schedule

- **Primary trigger:** Weekly check during optimization routine
- **Alert trigger:** Creative fatigue thresholds breached
- **Scheduled trigger:** Monthly creative refresh cycle
- **Duration:** 30-60 minutes per account
- **Owner:** Creative Strategist Agent
- **Supporting Agents:** Copy Agent, Swipe File Agent, Optimization Agent

---

## Pre-Conditions

- [ ] Creative registry is current
- [ ] Fatigue thresholds configured in config.yaml
- [ ] Performance data available for all active creatives
- [ ] Brand guidelines accessible
- [ ] Creative production capacity confirmed

---

## Step-by-Step Workflow

### Step 1: Creative Health Assessment (15 minutes)

```yaml
action: Evaluate all active creatives against fatigue indicators
for_each_creative:
  metrics:
    - Current CTR vs. peak CTR
    - Current CPA vs. average CPA for that creative
    - Frequency (audience-level)
    - Days running
    - Engagement rate trend (7-day)
  classify:
    healthy:
      criteria: "CTR within 10% of peak, frequency < threshold, CPA stable"
      action: "Continue running"
    watch:
      criteria: "CTR declined 10-20% from peak OR frequency approaching threshold"
      action: "Monitor closely, begin briefing replacements"
    fatigued:
      criteria: "CTR declined > 20% from peak OR frequency > threshold OR CPA > 1.3x average"
      action: "Phase out, introduce replacement"
    retired:
      criteria: "CTR declined > 40% from peak OR CPA > 2x target"
      action: "Pause immediately"
output: Creative health report with classification per asset
```

### Step 2: Rotation Decision (10 minutes)

```yaml
action: Determine rotation actions based on health assessment
decision_matrix:
  all_healthy:
    action: "No rotation needed. Schedule next check."
  some_in_watch:
    action: "Brief new creative variations. Prepare to swap in 1-2 weeks."
  some_fatigued:
    action: "Activate replacement creative. Reduce spend on fatigued assets."
  majority_fatigued:
    action: "Trigger full creative refresh. Brief 5-10 new variations."
  critical_fatigue:
    action: "Pause worst performers immediately. Launch any available replacements."
rotation_rules:
  - Never pause all creatives simultaneously (maintain continuity)
  - Phase in new while phasing out old (overlap period: 3-5 days)
  - Preserve winning elements from top performers in new variations
  - Maintain creative diversity (mix of formats, hooks, angles)
  - Keep at least 3 active creatives per ad set at all times
```

### Step 3: Brief New Creative (15 minutes, if rotation needed)

```yaml
action: Create creative brief for replacement assets
brief_components:
  quantity: "Based on number of fatigued assets to replace + buffer"
  direction:
    - Carry forward winning hooks and angles from current top performers
    - Test new concepts identified from swipe file or competitive analysis
    - Maintain format diversity (video, static, carousel)
    - Address any audience-specific messaging gaps
  specifications:
    - Platform and placement requirements
    - Brand guideline adherence
    - Copy direction (reference phrase libraries)
    - Production timeline
  timeline:
    - Brief submission: Today
    - Draft delivery: [3-5 business days]
    - Review and approval: [1-2 days]
    - Launch: [Within 7 business days]
```

### Step 4: Implement Rotation (10 minutes)

```yaml
action: Execute the creative rotation
steps:
  phase_out:
    - Reduce budget allocation to fatigued creatives (don't pause yet)
    - Set calendar reminder to pause in 3-5 days
    - Document final performance metrics
  phase_in:
    - Activate new creatives alongside existing (not replacing)
    - Ensure new creatives are in appropriate ad sets
    - Verify tracking and UTMs on new assets
    - Monitor initial delivery signals
  complete_rotation:
    - After 3-5 days, pause fully fatigued assets
    - Confirm new creatives are delivering and performing
    - Update creative registry with status changes
```

### Step 5: Update Registries and Documentation (5 minutes)

```yaml
action: Update all tracking systems
updates:
  creative_registry:
    - Update fatigue_status for all assessed creatives
    - Add new creatives with initial data
    - Update retired_date for paused creatives
  decisions_log:
    - Log rotation decision with rationale
    - Document which creatives were paused and why
    - Document which creatives were introduced
  creative_brief:
    - Archive the brief for new creative
    - Track delivery timeline
```

---

## Decision Points

| Condition | Action |
|-----------|--------|
| CTR declined > 20% from peak | Classify as fatigued, begin phase-out |
| Frequency > 3.5 (configurable) | Audience saturation contributing to fatigue |
| No replacement creative available | Prioritize emergency creative production |
| New creative underperforms within 72 hours | Give 7 days minimum before judging |
| All creatives healthy | No rotation needed; schedule next check |

---

## Output / Deliverables

- Creative health report with lifecycle classification
- Rotation action plan (if applicable)
- New creative brief (if rotation needed)
- Updated creative registry
- Updated decisions log
- Optimization log entries

---

## Post-Conditions

- [ ] All creatives assessed and classified
- [ ] Fatigued creatives phased out or scheduled for phase-out
- [ ] New creatives activated (if available)
- [ ] Creative brief submitted for production (if needed)
- [ ] Registries updated
- [ ] Minimum 3 active creatives maintained per ad set
- [ ] Next rotation check scheduled
