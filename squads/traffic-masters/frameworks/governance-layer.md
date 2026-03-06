# Governance Layer

> **Type**: Stack Layer
> **Domain**: Oversight — Compliance, Financial Control, Quality Assurance
> **Used by agents**: Traffic Chief, Fiscal, Ads Analyst, Performance Analyst

## Overview

The Governance Layer provides strategic oversight across the entire traffic operation. While other layers execute, this layer ensures compliance, financial accuracy, quality standards, and cross-functional alignment. Governance prevents the operational drift that leads to policy violations, budget overruns, attribution errors, and strategic misalignment. This is an ongoing layer that operates in parallel with all other layers.

## When to Use

- Continuously — governance runs in perpetuity for all active operations
- Weekly compliance spot checks
- Monthly financial reconciliation
- Quarterly strategic audits
- Annual reviews and planning
- Any time a compliance or financial discrepancy is identified

## The Framework

### Governance Domains

#### 1. Compliance Oversight
**Owner**: Ads Analyst, Traffic Chief
**Cadence**: Weekly spot checks, monthly full review

**Activities**:
- Verify all active ads comply with current platform policies.
- Review landing pages for policy compliance (claims, disclosures, user experience).
- Monitor ad rejection rates — flag accounts exceeding 10% rejection rate.
- Track platform policy updates and communicate changes to all agents.
- Verify proper disclosures on sponsored content and influencer partnerships.
- Audit targeting practices for discriminatory advertising compliance (housing, employment, credit).

**Compliance Scorecard**:
| Metric | Green | Yellow | Red |
|--------|-------|--------|-----|
| Ad rejection rate | < 5% | 5-10% | > 10% |
| Policy warnings | 0 in 30 days | 1 in 30 days | 2+ in 30 days |
| Account restrictions | None | Warning received | Restricted/banned |
| LP compliance | All pages compliant | Minor issues found | Major violations |
| Disclosure compliance | All proper | Missing on some | Missing on many |

**Remediation Protocol**:
- Yellow: Document, fix within 48 hours, add to training queue.
- Red: Immediate pause of non-compliant elements. Traffic Chief notified. Post-mortem within 24 hours. Preventive measures documented.

#### 2. Financial Reconciliation
**Owner**: Fiscal, Traffic Chief
**Cadence**: Monthly reconciliation, quarterly deep audit

**Activities**:
- Reconcile platform-reported spend vs invoiced amounts vs client budget.
- Verify billing accuracy across all ad accounts.
- Track actual vs planned budget allocation per channel and campaign.
- Monitor fee structures and management costs against agreements.
- Flag any discrepancies exceeding 2% of monthly spend.
- Ensure all payment methods are current and credit limits are adequate.

**Financial Controls**:
| Control | Description | Check Frequency |
|---------|------------|-----------------|
| Spend vs Budget | Actual spend within 5% of planned budget | Weekly |
| Platform vs Invoice | Platform-reported matches invoice | Monthly |
| Fee Accuracy | Management fees calculated correctly | Monthly |
| Payment Status | All payment methods active, no declined charges | Weekly |
| Credit Limits | Sufficient headroom for upcoming spend | Monthly |
| Tax Documentation | Proper tax treatment of ad spend by jurisdiction | Quarterly |

**Discrepancy Resolution**:
1. Identify the discrepancy source (platform error, billing delay, budget overspend).
2. Document with evidence (screenshots, reports, invoice copies).
3. Resolve with platform support or client finance team within 5 business days.
4. Implement preventive measure to avoid recurrence.
5. Log in governance audit trail.

#### 3. Quality Audits
**Owner**: Performance Analyst, Traffic Chief
**Cadence**: Monthly spot audits, quarterly comprehensive

**Audit Areas**:
- **Account Structure Audit**: Does the account follow framework standards? Naming conventions, campaign organization, audience segmentation.
- **Tracking Audit**: Is all tracking firing correctly? Monthly verification per `tracking-layer.md`.
- **Creative Audit**: Is creative production meeting velocity targets? Quality standards maintained?
- **Audience Audit**: Are audiences fresh? Overlap managed? Exclusions in place?
- **Performance Audit**: Are optimization actions being taken? Daily logs maintained? Decisions documented?

**Audit Scoring**:
- Each audit area scored 1-5 (1 = critical issues, 5 = exemplary).
- Overall account health score = average of all areas.
- Any area scoring 2 or below triggers immediate remediation plan.
- Target: all areas at 3+ (meets standard) with a trajectory toward 4+ (exceeds).

#### 4. Cross-Squad Synchronization
**Owner**: Traffic Chief
**Cadence**: Bi-weekly sync meetings

**Activities**:
- Align with other squads (Content, Design, Development, Sales) on shared objectives.
- Coordinate campaign launches with product launches, content calendar, and promotional schedule.
- Share performance insights that inform other squads' strategies.
- Receive inputs from other squads that affect traffic strategy (product changes, pricing updates, content updates).
- Resolve cross-functional blockers (landing page changes, creative asset requests, technical fixes).

**Sync Agenda**:
1. Traffic performance summary (5 min)
2. Cross-squad dependencies and blockers (10 min)
3. Upcoming initiatives requiring coordination (10 min)
4. Resource requests (5 min)
5. Action items and owners (5 min)

#### 5. Quarterly Strategic Review
**Owner**: Traffic Chief, Performance Analyst
**Cadence**: Every 90 days

**Review Components**:
- **Performance vs Goals**: Did we hit quarterly targets? What drove success or shortfall?
- **Channel Assessment**: Which channels performed? Which should be expanded, maintained, or cut?
- **Creative Performance**: What angles, hooks, and formats won? What patterns emerged?
- **Audience Insights**: What did we learn about the target audience? New segments identified?
- **Competitive Movement**: What changed in the competitive landscape?
- **Budget Efficiency**: How did actual allocation compare to planned? Where was money best spent?
- **Team Performance**: Are agents performing effectively? Training needs identified?
- **Strategy Adjustment**: What changes for next quarter? New experiments? New channels?

**Output**: Quarterly strategic review document with recommendations for next 90 days.

### Governance Calendar

| Frequency | Activity | Owner |
|-----------|----------|-------|
| Daily | Performance monitoring and logging | Performance Analyst |
| Weekly | Compliance spot check, spend vs budget review | Ads Analyst, Fiscal |
| Bi-weekly | Cross-squad sync meeting | Traffic Chief |
| Monthly | Financial reconciliation, quality spot audit, tracking verification | Fiscal, Performance Analyst, Pixel Specialist |
| Quarterly | Comprehensive audit, strategic review, policy update review | Traffic Chief, all agents |
| Annually | Full operational review, contract/agreement review, annual planning | Traffic Chief, Fiscal |

## Key Concepts

- **Governance Is Not Bureaucracy**: It is the immune system of the operation. Without it, small issues become existential threats (account bans, financial losses, strategic drift).
- **Audit Trail**: Every significant decision must be documented. If it is not documented, it did not happen. Audit trails protect the team and inform future decisions.
- **Proactive Over Reactive**: Governance catches issues before they become crises. A monthly tracking audit is cheaper than discovering a 3-month attribution gap.
- **Fiscal Accountability**: The traffic team is a steward of client budget. Every dollar must be accounted for and justified.

## Decision Rules

1. Governance calendar activities are mandatory — they cannot be deprioritized for campaign work.
2. Any Red compliance finding triggers immediate remediation — no delay.
3. Financial discrepancies exceeding 2% of monthly spend must be resolved within 5 business days.
4. Quarterly reviews must produce a written document with actionable recommendations.
5. Cross-squad blockers are escalated within 48 hours if not resolved at sync meeting.
6. All governance findings are archived — they form the institutional knowledge base.

## Common Mistakes

- Treating governance as optional or "when we have time" — it is not.
- Not documenting decisions and actions — memory is unreliable, audit trails are not.
- Ignoring small compliance issues until they trigger account restrictions.
- Skipping financial reconciliation and discovering large discrepancies months later.
- Conducting quarterly reviews as formalities rather than genuine strategic recalibrations.
- Not sharing governance findings with the broader team — lessons must be learned collectively.

## Integration

- Compliance monitoring covers all ads and landing pages from `creative-layer.md` and `media-buying-layer.md`.
- Financial reconciliation uses data from all active campaigns across all account structures.
- Quality audits reference standards from all internal frameworks.
- Cross-squad sync coordinates with `client-ops-handoff.md` for client-facing alignment.
- Quarterly reviews update `strategy-layer.md` for next-period planning.
- Policy updates flow to `policy-risk-classification.md` for classification adjustments.
- Tracking audits follow `tracking-layer.md` QA protocols.

## Output

- Weekly compliance spot check log.
- Monthly financial reconciliation report.
- Monthly quality audit scorecard per account.
- Bi-weekly cross-squad sync meeting notes with action items.
- Quarterly strategic review document with recommendations.
- Annual operational review and planning document.
- Governance incident log (all Yellow/Red findings with resolution).
