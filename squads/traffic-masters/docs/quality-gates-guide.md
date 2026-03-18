# Quality Gates Guide

> Guide to understanding and using quality gates throughout the Traffic Masters Squad system.

---

## What Are Quality Gates?

Quality gates are checkpoints within workflows and tasks that must be passed before work can advance to the next stage. They ensure:

- **Consistency** — Every campaign, report, and optimization meets the same standard
- **Accuracy** — Data, settings, and outputs are verified before action
- **Compliance** — Work adheres to brand, platform, and regulatory requirements
- **Risk reduction** — Errors are caught before they impact performance or client relationships

---

## Quality Gate Types

### 1. Checklist Gates
A predefined list of items that must all be verified before proceeding.

**How they work:** Each item is checked off. All items must be complete. Any incomplete item blocks progression.

**Examples:**
- Pre-Launch Checklist (blocks campaign activation)
- Reporting Quality Checklist (blocks report delivery)
- Tracking Audit Checklist (blocks account sign-off)

### 2. Threshold Gates
Quantitative thresholds that must be met or not exceeded.

**How they work:** A metric is compared against a defined threshold. If the metric falls outside acceptable range, the gate blocks.

**Examples:**
- Minimum conversion volume for scaling (50 conversions in 7 days)
- Maximum CPA degradation during scaling (15%)
- Minimum statistical significance for test results (95%)
- Budget utilization range (85-105%)

### 3. Approval Gates
Require explicit approval from a designated role or agent before proceeding.

**How they work:** Work is reviewed by the approver. Approver can approve, reject, or request changes.

**Examples:**
- Creative approval before launch
- Budget change approval above threshold
- Strategy approval before execution
- Report approval before client delivery

### 4. Validation Gates
Automated checks that verify data integrity, configuration accuracy, or system readiness.

**How they work:** System runs validation logic. Pass/fail result determines progression.

**Examples:**
- Tracking pixel firing verification
- UTM parameter format validation
- Naming convention compliance check
- Registry cross-reference validation

---

## Quality Gates by Workflow Stage

### Pre-Planning
| Gate | Type | Criteria | Owner |
|------|------|----------|-------|
| Business goal clarity | Approval | Goals are specific, measurable, and documented | traffic-chief |
| Budget confirmation | Threshold | Budget is confirmed and within feasible range | fiscal |
| Platform access | Validation | All required platform accounts are accessible | traffic-chief |

### Strategy & Planning
| Gate | Type | Criteria | Owner |
|------|------|----------|-------|
| Strategy approval | Approval | Strategy document approved by stakeholder | traffic-chief |
| KPI feasibility | Threshold | Targets are achievable based on benchmarks | traffic-chief |
| Audience viability | Threshold | Target audiences meet minimum size requirements | depesh-mandalia |

### Creative Development
| Gate | Type | Criteria | Owner |
|------|------|----------|-------|
| Creative brief approval | Approval | Brief approved by ad-midas | ad-midas |
| Brand compliance | Checklist | Creative meets all brand guidelines | ad-midas |
| Platform specs | Validation | Assets meet platform technical requirements | media-buyer |
| Copy proofread | Checklist | Copy is error-free and approved | Cross-squad (Copy Squad) |
| Compliance review | Checklist | Ads comply with platform and regulatory policies | ads-analyst |

### Pre-Launch
| Gate | Type | Criteria | Owner |
|------|------|----------|-------|
| Pre-Launch Checklist | Checklist | All 20+ items verified | media-buyer |
| Tracking verification | Validation | Pixel/events firing correctly | pixel-specialist |
| UTM validation | Validation | All UTMs follow convention and resolve correctly | pixel-specialist |
| Settings review | Checklist | Bid, budget, targeting, scheduling all correct | media-buyer |

### Post-Launch (72-Hour)
| Gate | Type | Criteria | Owner |
|------|------|----------|-------|
| Delivery confirmation | Threshold | Impressions within expected range within 4 hours | performance-analyst |
| Tracking confirmation | Validation | Conversions being recorded | pixel-specialist |
| Spend pacing | Threshold | Spend within 80-120% of expected daily rate | performance-analyst |
| No policy violations | Validation | Zero ad disapprovals | ads-analyst |

### Optimization
| Gate | Type | Criteria | Owner |
|------|------|----------|-------|
| Learning phase protection | Threshold | No changes during active learning phase | performance-analyst |
| Minimum data requirement | Threshold | At least 7 days of data before optimization | performance-analyst |
| Change limit | Threshold | Maximum changes per cycle not exceeded | performance-analyst |

### Scaling
| Gate | Type | Criteria | Owner |
|------|------|----------|-------|
| Scaling readiness | Checklist | All readiness criteria met | scale-optimizer |
| Performance stability | Threshold | CPA/ROAS stable within 15% for 14+ days | scale-optimizer |
| Creative depth | Threshold | Minimum 3 active winning creatives | ad-midas |
| Budget increment limit | Threshold | Increase does not exceed 30% per phase | fiscal |

### Reporting
| Gate | Type | Criteria | Owner |
|------|------|----------|-------|
| Data accuracy | Validation | All data points verified against source | performance-analyst |
| Calculation verification | Validation | Percentages and derived metrics recalculated | performance-analyst |
| Completeness | Checklist | All required sections populated | performance-analyst |
| Review approval | Approval | Internal review completed | traffic-chief |

### Testing
| Gate | Type | Criteria | Owner |
|------|------|----------|-------|
| Hypothesis clarity | Checklist | Hypothesis is specific and testable | performance-analyst |
| Test isolation | Validation | Only one variable differs between variants | performance-analyst |
| Sample size minimum | Threshold | Minimum sample size reached before analysis | performance-analyst |
| Significance threshold | Threshold | 95% statistical significance before declaring winner | performance-analyst |

---

## Gate Failure Handling

### When a Gate Fails

1. **Stop** — Do not proceed past the failed gate
2. **Identify** — Determine which specific criteria were not met
3. **Remediate** — Fix the issue or obtain the missing requirement
4. **Re-evaluate** — Run the gate check again
5. **Document** — Log the failure and resolution in the decisions log

### Override Policy

Gates can be overridden only under these conditions:
- **Approval override:** A designated authority explicitly approves the override
- **Documentation:** The override reason is documented in the decisions log
- **Risk acceptance:** The risk of proceeding without the gate is acknowledged
- **Time-limited:** Override does not set a permanent precedent

**Gates that cannot be overridden:**
- Tracking verification (data integrity is non-negotiable)
- Legal/regulatory compliance
- Budget authorization above defined thresholds

---

## Implementing New Quality Gates

When adding a new quality gate:

1. **Define the gate** — Name, type, specific criteria, threshold values
2. **Assign ownership** — Which agent is responsible for evaluation
3. **Define the trigger** — When does this gate activate in the workflow
4. **Document failure handling** — What happens if the gate fails
5. **Set override policy** — Can it be overridden, and by whom
6. **Add to workflow documentation** — Update the relevant workflow with the new gate
7. **Communicate** — Ensure all agents and team members are aware

---

## Quality Gate Review Schedule

| Review | Frequency | Purpose |
|--------|-----------|---------|
| Threshold calibration | Quarterly | Adjust thresholds based on performance trends |
| Gate effectiveness | Quarterly | Assess whether gates are catching real issues |
| False positive review | Monthly | Identify gates that block unnecessarily |
| New gate assessment | As needed | Evaluate if new gates are needed based on incidents |
| Override audit | Quarterly | Review all overrides for patterns and policy compliance |
