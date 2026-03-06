# Campaign Launch Script — Automation Script

> Step-by-step campaign launch automation from final approval through activation and initial monitoring.

---

## Purpose

Execute a structured campaign launch process that ensures every setting is correct, tracking is verified, and monitoring is in place before activation. Prevents launch errors that waste budget or damage performance.

---

## Trigger / Schedule

- **Trigger:** Campaign strategy approved, creative assets finalized, tracking verified
- **Duration:** 1-3 hours per campaign
- **Owner:** Launch Agent
- **Supporting Agents:** Tracking Agent, Compliance Agent, Optimization Agent

---

## Pre-Conditions

- [ ] Campaign brief approved by Strategy Agent
- [ ] Creative assets produced, reviewed, and approved
- [ ] Ad copy finalized and proofread
- [ ] Audience segments built and verified
- [ ] Budget allocation confirmed
- [ ] Landing pages live and tested
- [ ] Tracking implementation verified by Tracking Agent
- [ ] Compliance review passed (if applicable)

---

## Step-by-Step Workflow

### Step 1: Campaign Configuration (20 minutes)

```yaml
action: Set up campaign in ad platform
settings:
  campaign_level:
    - Campaign name (per naming convention)
    - Campaign objective (matching strategy)
    - Budget type and amount (daily/lifetime)
    - Campaign spending limit (safety net)
    - Bid strategy selection
    - Start date and end date
    - Special ad categories (if applicable)
  ad_set_level:
    for_each_ad_set:
      - Ad set name (per naming convention)
      - Audience targeting (per audience spec)
      - Geographic targeting
      - Demographic filters (age, gender)
      - Placement selection (automatic or manual)
      - Scheduling / dayparting (if applicable)
      - Frequency cap (if applicable)
      - Exclusions applied
      - Budget (if ad set budget, not campaign budget)
      - Bid amount (if manual/cap bidding)
  ad_level:
    for_each_ad:
      - Ad name (per naming convention)
      - Creative asset uploaded and verified
      - Headline, primary text, description filled
      - CTA button selected
      - Destination URL set
      - UTM parameters appended
      - Display link customized (if applicable)
      - Tracking pixel selected
      - Conversion event selected
```

### Step 2: Pre-Launch Verification (15 minutes)

```yaml
action: Run Pre-Launch Checklist
verify:
  settings:
    - [ ] Campaign objective matches strategy brief
    - [ ] Budget and bid strategy are correct
    - [ ] Start/end dates are correct
    - [ ] Spending limits set as safety net
  targeting:
    - [ ] Audiences match strategy specification
    - [ ] Exclusions are applied (converters, employees, etc.)
    - [ ] Geographic targeting is correct
    - [ ] Placements are appropriate
  creative:
    - [ ] All ads display correctly in preview
    - [ ] Mobile and desktop previews reviewed
    - [ ] Stories/Reels placement preview reviewed (if applicable)
    - [ ] Copy is error-free
    - [ ] CTA is appropriate
  tracking:
    - [ ] Destination URLs work (200 status, correct page)
    - [ ] UTM parameters are correctly formatted
    - [ ] Conversion pixel fires on destination page
    - [ ] Conversion event type is correct
    - [ ] Attribution window is configured per strategy
  compliance:
    - [ ] Ad copy passes platform policy review
    - [ ] Creative meets platform specifications
    - [ ] Industry-specific compliance met (if applicable)
decision:
  all_checks_pass:
    yes: "Proceed to Step 3"
    no: "Fix all failures before proceeding"
```

### Step 3: Registry Updates (5 minutes)

```yaml
action: Update all registries
updates:
  - Add campaign to campaigns registry (CMP-XXX)
  - Add creatives to creative registry (CRE-XXX)
  - Verify audience entries exist in audience registry
  - Log launch decision in decisions log (DEC-XXX)
  - Record UTM-to-campaign mapping
```

### Step 4: Stakeholder Notification (5 minutes)

```yaml
action: Notify stakeholders of impending launch
notification:
  recipients: "Account manager, client (if applicable), team"
  content:
    - Campaign name and objective
    - Target audience summary
    - Budget and timeline
    - KPI targets
    - Expected launch time
    - Monitoring plan summary
```

### Step 5: Campaign Activation (5 minutes)

```yaml
action: Set campaigns to active
activation:
  - Turn on all campaigns in the planned sequence
  - Verify delivery status changes to "Active" or "In Review"
  - Note activation timestamp
  - Confirm spend begins (for immediate-start campaigns)
```

### Step 6: Post-Launch Monitoring Setup (10 minutes)

```yaml
action: Configure monitoring for first 72 hours
monitoring:
  hour_4:
    check: "Ads delivering, impressions recording, no disapprovals"
  hour_12:
    check: "Spend pacing reasonable, clicks recording"
  hour_24:
    check: "Full day metrics, CPC/CTR in expected range, conversions recording"
  day_2:
    check: "Performance trends, any anomalies, tracking verification"
  day_3:
    check: "Stable delivery, metrics within expected ranges"
alerts:
  - Set budget pacing alerts
  - Set CPA/ROAS threshold alerts
  - Set delivery status change alerts
```

### Step 7: Launch Confirmation Document (5 minutes)

```yaml
action: Complete campaign launch document
document:
  - Campaign ID and name
  - Platform and account
  - Objective and KPI targets
  - Budget and bid strategy
  - Audience summary
  - Creative summary
  - Tracking confirmation
  - Launch timestamp
  - Monitoring plan
  - First review date
```

---

## Decision Points

| Condition | Action |
|-----------|--------|
| Pre-launch check fails | Do not launch; fix the issue first |
| Ad disapproved during review | Review policy violation, fix, resubmit |
| No delivery after 4 hours | Investigate targeting, bid, audience size |
| Spend pacing too fast | Verify budget settings, consider daily cap |
| Tracking not recording | Pause campaign, fix tracking, relaunch |

---

## Output / Deliverables

- Active campaign(s) delivering in ad platform
- Completed Pre-Launch Checklist
- Campaign launch confirmation document
- Updated campaign, creative, and audience registries
- Post-launch monitoring schedule
- Stakeholder notification

---

## Post-Conditions

- [ ] All campaigns activated and delivering
- [ ] No ad disapprovals (or disapprovals addressed)
- [ ] Tracking verified on live traffic
- [ ] Registries updated
- [ ] Monitoring schedule active
- [ ] Stakeholders notified
- [ ] 72-hour monitoring plan in place
