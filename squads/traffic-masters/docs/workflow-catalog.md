# Workflow Catalog — Traffic Masters Squad

> Complete catalog of all multi-step workflows with triggers, agent sequences, decision points, and outputs.

---

## Workflow Index

| # | Workflow | Category | Trigger | Agents Involved |
|---|----------|----------|---------|----------------|
| 1 | New Campaign Launch | Execution | Business request for new campaign | Strategy, Audience, Creative Strategist, Copy, Launch, Tracking |
| 2 | Daily Monitoring | Operations | Every business day, morning | Optimization, Diagnostics |
| 3 | Weekly Optimization | Operations | Every Monday | Optimization, Budget, Creative Strategist, Reporting |
| 4 | Monthly Review & Report | Operations | First week of each month | Reporting, Diagnostics, Strategy |
| 5 | Performance Recovery | Reactive | KPI drops >20% for 3+ days | Diagnostics, Optimization, Creative Strategist, Tracking |
| 6 | Creative Refresh | Creative | Fatigue indicators triggered | Creative Strategist, Copy, Swipe File, Launch |
| 7 | Scaling Initiative | Growth | Performance targets met + growth budget | Scaling, Budget, Audience, Creative Strategist |
| 8 | Account Onboarding | Setup | New client / account | Diagnostics, Tracking, Strategy, Audience, Launch |
| 9 | A/B Test Lifecycle | Testing | Hypothesis approved | Experimentation, relevant domain agent, Reporting |
| 10 | Quarterly Strategy Review | Strategy | End of quarter | Strategy, Intelligence, Reporting, Budget |
| 11 | Budget Planning Cycle | Budget | Start of quarter or fiscal period | Budget, Strategy, Reporting |
| 12 | Cross-Squad Campaign | Coordination | Multi-squad project initiated | Integration, Strategy, Creative Strategist, Copy |

---

## 1. New Campaign Launch Workflow

**Trigger:** Business request for a new campaign or initiative
**Duration:** 5-10 business days (planning through launch)
**Owner:** Strategy Agent (planning phase), Launch Agent (execution phase)

### Steps

```
Step 1: INTAKE
  Agent: Strategy
  Action: Receive and document business requirements
  Input: Business goals, budget, timeline, audience
  Output: Intake brief
  Decision: Sufficient information? YES -> Step 2 | NO -> Request more info

Step 2: STRATEGY DEVELOPMENT
  Agent: Strategy + Budget + Intelligence
  Action: Develop campaign strategy and media plan
  Input: Intake brief, historical data, competitive context
  Output: Campaign brief, media plan, KPI framework
  Decision: Strategy approved? YES -> Step 3 | NO -> Revise

Step 3: AUDIENCE BUILDING
  Agent: Audience
  Action: Define and build audience segments
  Input: Campaign brief, customer data
  Output: Audience definitions, targeting specs
  Decision: Audiences viable? YES -> Step 4 | NO -> Revise strategy

Step 4: CREATIVE DEVELOPMENT
  Agent: Creative Strategist + Copy
  Action: Develop creative brief and produce ad copy/assets
  Input: Campaign brief, audience profiles, brand guidelines
  Output: Creative brief, ad copy, creative assets
  Decision: Creative approved? YES -> Step 5 | NO -> Revise

Step 5: TRACKING SETUP
  Agent: Tracking
  Action: Verify tracking and configure measurement
  Input: Destination URLs, conversion events, UTM plan
  Output: Verified tracking, UTM documentation
  Decision: Tracking verified? YES -> Step 6 | NO -> Fix tracking

Step 6: COMPLIANCE REVIEW (if applicable)
  Agent: Compliance
  Action: Review ads for policy compliance
  Input: Final ad copy and creative
  Output: Compliance approval or required changes
  Decision: Compliant? YES -> Step 7 | NO -> Revise creative/copy

Step 7: CAMPAIGN SETUP & LAUNCH
  Agent: Launch
  Action: Configure and activate campaigns
  Input: All approved assets, settings, tracking
  Output: Live campaigns, launch confirmation
  Gate: Pre-Launch Checklist 100% complete

Step 8: POST-LAUNCH MONITORING
  Agent: Optimization
  Action: Monitor first 72 hours
  Input: Live performance data
  Output: Monitoring report, any emergency adjustments
  Transition: Enter Daily Monitoring workflow
```

---

## 2. Daily Monitoring Workflow

**Trigger:** Every business day, morning (within 1 hour of business start)
**Duration:** 30-60 minutes per account
**Owner:** Optimization Agent

### Steps

```
Step 1: DASHBOARD REVIEW
  Action: Review all active campaigns for anomalies
  Check: Spend pacing, CPA/ROAS vs. target, delivery status
  Decision: Anomalies detected? YES -> Step 2 | NO -> Step 3

Step 2: ANOMALY INVESTIGATION
  Action: Investigate flagged metrics
  Check: Root cause identification
  Decision: Critical issue? YES -> Trigger Performance Recovery workflow
                           NO -> Log finding, address in weekly cycle

Step 3: QUICK WINS
  Action: Implement any obvious, low-risk optimizations
  Examples: Pause underperforming ads, adjust dayparting, refresh exclusions
  Output: Actions logged in optimization log

Step 4: STATUS UPDATE
  Action: Update daily status notes
  Output: Daily status summary (internal)
```

---

## 3. Weekly Optimization Workflow

**Trigger:** Every Monday (or first business day of the week)
**Duration:** 1-2 hours per account
**Owner:** Optimization Agent

### Steps

```
Step 1: PERFORMANCE REVIEW
  Agent: Optimization
  Action: Review 7-day performance against targets
  Output: Performance summary with flagged items

Step 2: CAMPAIGN OPTIMIZATION
  Agent: Optimization
  Action: Adjust bids, budgets, placements, scheduling
  Gate: Weekly Optimization Checklist

Step 3: CREATIVE ASSESSMENT
  Agent: Creative Strategist
  Action: Check creative health indicators
  Decision: Fatigue detected? YES -> Trigger Creative Refresh workflow
                              NO -> Continue

Step 4: AUDIENCE REVIEW
  Agent: Audience (if needed)
  Action: Check frequency, saturation, overlap
  Decision: Audience issues? YES -> Plan audience changes
                             NO -> Continue

Step 5: BUDGET CHECK
  Agent: Budget
  Action: Review pacing, efficiency, reallocation opportunities
  Decision: Reallocation needed? YES -> Implement with Budget Change Checklist
                                 NO -> Continue

Step 6: DOCUMENTATION
  Agent: Optimization
  Action: Log all actions, update registries
  Output: Weekly optimization log entry
```

---

## 4. Monthly Review & Report Workflow

**Trigger:** First week of each month
**Duration:** 3-5 hours per account
**Owner:** Reporting Agent

### Steps

```
Step 1: DATA COMPILATION
  Agent: Reporting
  Action: Gather and validate all performance data for the month
  Output: Verified data set

Step 2: PERFORMANCE ANALYSIS
  Agent: Reporting + Diagnostics
  Action: Analyze trends, comparisons, winners/losers
  Output: Analysis document

Step 3: REPORT GENERATION
  Agent: Reporting
  Action: Produce monthly report using template
  Gate: Reporting Quality Checklist
  Output: Draft report

Step 4: RECOMMENDATIONS DEVELOPMENT
  Agent: Strategy + Optimization
  Action: Develop recommendations for next month
  Output: Prioritized recommendation list

Step 5: REVIEW & APPROVAL
  Action: Internal review of report and recommendations
  Decision: Approved? YES -> Step 6 | NO -> Revise

Step 6: DELIVERY
  Action: Deliver report to stakeholders
  Output: Final monthly report
```

---

## 5. Performance Recovery Workflow

**Trigger:** Primary KPI drops >20% for 3+ consecutive days
**Duration:** 1-3 days (diagnosis through resolution)
**Owner:** Diagnostics Agent
**Priority:** High

### Steps

```
Step 1: ALERT & TRIAGE
  Agent: Diagnostics
  Action: Confirm anomaly, classify severity
  Decision: Critical (active revenue loss) -> Fast-track to Step 3
            High (significant decline) -> Step 2

Step 2: IMPACT ASSESSMENT
  Agent: Diagnostics
  Action: Quantify impact (lost revenue, wasted spend, volume decline)
  Output: Impact report

Step 3: ROOT CAUSE DIAGNOSIS
  Agent: Diagnostics + Tracking
  Action: Systematic diagnosis using Performance Diagnosis Framework
  Output: Root cause analysis with confidence level
  Decision: Root cause identified? YES -> Step 4 | NO -> Expand investigation

Step 4: REMEDIATION PLAN
  Agent: Optimization + relevant specialist agent
  Action: Develop and implement fix
  Output: Remediation plan with expected recovery timeline

Step 5: MONITORING
  Agent: Optimization
  Action: Monitor recovery over 3-7 days
  Decision: Recovered? YES -> Document learnings | NO -> Escalate

Step 6: POST-MORTEM
  Agent: Diagnostics
  Action: Document root cause, fix, and preventive measures
  Output: Post-mortem report, updated monitoring rules
```

---

## 6-12: Additional Workflows (Condensed)

### 6. Creative Refresh Workflow
**Trigger:** Fatigue indicators hit threshold
```
Review fatigue data -> Brief new creative -> Produce assets -> Approve -> Phase in new / phase out old -> Monitor
```

### 7. Scaling Initiative Workflow
**Trigger:** Scaling readiness confirmed
```
Readiness assessment -> Scaling plan -> Phase 1: Budget increase (20-30%) -> Monitor -> Phase 2: Audience expansion -> Monitor -> Phase 3: New channels -> Evaluate
```

### 8. Account Onboarding Workflow
**Trigger:** New client or account
```
Intake questionnaire -> Access setup -> Tracking audit -> Account audit -> Strategy development -> Initial campaign setup -> Launch -> 30-day review
```

### 9. A/B Test Lifecycle Workflow
**Trigger:** Hypothesis approved for testing
```
Design test plan -> Calculate sample/duration -> Configure test -> Launch -> Monitor progress -> Reach significance -> Analyze results -> Document learnings -> Implement winner
```

### 10. Quarterly Strategy Review Workflow
**Trigger:** End of each quarter
```
Compile quarterly data -> Performance review -> Competitive analysis -> Strategy assessment -> Next quarter planning -> Budget recommendation -> Stakeholder presentation
```

### 11. Budget Planning Cycle Workflow
**Trigger:** Start of fiscal period or quarter
```
Historical analysis -> Efficiency modeling -> Scenario planning -> Draft allocation -> Strategy alignment -> Approval -> Implementation -> Monitoring setup
```

### 12. Cross-Squad Campaign Workflow
**Trigger:** Multi-squad project initiated
```
Requirements gathering -> Squad coordination -> Asset sharing -> Parallel execution -> Quality alignment -> Launch coordination -> Unified reporting
```

---

## Workflow Interaction Map

```
Account Onboarding
        |
        v
Quarterly Strategy Review <----> Budget Planning Cycle
        |
        v
New Campaign Launch
        |
        v
Daily Monitoring <---> Weekly Optimization <---> Monthly Review
        |                      |
        v                      v
Performance Recovery    Creative Refresh
                              |
                              v
                       Scaling Initiative
```

---

## Workflow Governance

1. **Every workflow has a single owner** — One agent is accountable for the workflow completing successfully
2. **Decision points require explicit criteria** — No subjective gates; define thresholds and conditions
3. **All outputs are documented** — Every workflow produces trackable deliverables
4. **Escalation paths are defined** — If a workflow stalls, the escalation route is clear
5. **Workflows are versioned** — Track changes to workflow definitions over time
