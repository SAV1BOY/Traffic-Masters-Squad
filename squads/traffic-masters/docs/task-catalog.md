# Task Catalog — Traffic Masters Squad

> Complete catalog of all defined task types with descriptions, routing to agents, inputs, outputs, and priority levels.

---

## Task Index

| # | Task | Category | Primary Agent | Priority |
|---|------|----------|---------------|----------|
| 1 | Full Account Audit | Diagnostics | Diagnostics | High |
| 2 | Campaign Strategy Development | Strategy | Strategy | High |
| 3 | Campaign Launch | Execution | Launch | High |
| 4 | Weekly Optimization Cycle | Optimization | Optimization | Medium |
| 5 | Performance Report Generation | Reporting | Reporting | Medium |
| 6 | Creative Performance Review | Creative | Creative Strategist | Medium |
| 7 | Budget Reallocation | Budget | Budget | Medium |
| 8 | Audience Analysis & Refresh | Audience | Audience | Medium |
| 9 | Tracking Audit | Measurement | Tracking | High |
| 10 | A/B Test Design | Testing | Experimentation | Medium |
| 11 | A/B Test Analysis | Testing | Experimentation | Medium |
| 12 | Competitive Analysis | Intelligence | Intelligence | Low |
| 13 | Scaling Assessment | Growth | Scaling | Medium |
| 14 | Compliance Review | Governance | Compliance | High |
| 15 | Ad Copy Creation | Creative | Copy | Medium |
| 16 | Creative Brief Development | Creative | Creative Strategist | Medium |
| 17 | Performance Diagnosis | Diagnostics | Diagnostics | High |
| 18 | Cross-Squad Coordination | Integration | Integration | Medium |
| 19 | Swipe File Update | Resources | Swipe File | Low |
| 20 | New Account Onboarding | Onboarding | Diagnostics + Strategy | High |

---

## Task Details

### 1. Full Account Audit

**Category:** Diagnostics
**Primary Agent:** Diagnostics Agent
**Supporting Agents:** Tracking Agent, Strategy Agent
**Priority:** High
**Estimated Duration:** 2-4 hours

**Trigger Conditions:**
- New account onboarding
- Quarterly health review schedule
- Significant performance decline (>25% in primary KPI)
- Post-platform-update assessment

**Inputs Required:**
- Platform account access (read-only minimum)
- 30-90 days of historical performance data
- Current KPI targets and business goals
- Previous audit reports (if available)

**Outputs Delivered:**
- Account audit report (using Account Audit Report template)
- Prioritized findings with severity classification
- Recommended action plan with timeline
- Baseline metric documentation

**Quality Gate:** All checklist items in the Account Audit Checklist completed

---

### 2. Campaign Strategy Development

**Category:** Strategy
**Primary Agent:** Strategy Agent
**Supporting Agents:** Budget Agent, Audience Agent, Intelligence Agent
**Priority:** High
**Estimated Duration:** 4-8 hours

**Trigger Conditions:**
- New campaign initiative requested
- Business goal change
- Major market or competitive shift
- Quarterly strategy refresh

**Inputs Required:**
- Business objectives and KPI targets
- Budget parameters
- Audience information and customer data
- Competitive context
- Historical performance data

**Outputs Delivered:**
- Campaign brief (using Campaign Brief template)
- Media plan with channel mix
- KPI framework with targets
- Campaign architecture diagram
- Timeline and milestones

**Quality Gate:** Strategy aligned with business goals, budget feasibility confirmed, audience viability validated

---

### 3. Campaign Launch

**Category:** Execution
**Primary Agent:** Launch Agent
**Supporting Agents:** Tracking Agent, Compliance Agent
**Priority:** High
**Estimated Duration:** 1-3 hours

**Trigger Conditions:**
- Approved campaign strategy ready for execution
- All creative assets and copy approved
- Tracking verified

**Inputs Required:**
- Approved campaign brief
- Final creative assets
- Audience definitions
- Budget allocation
- Tracking specifications

**Outputs Delivered:**
- Configured and activated campaigns
- Launch confirmation document
- Post-launch monitoring plan
- Updated campaign registry

**Quality Gate:** Pre-Launch Checklist 100% complete

---

### 4. Weekly Optimization Cycle

**Category:** Optimization
**Primary Agent:** Optimization Agent
**Supporting Agents:** Creative Strategist Agent, Budget Agent
**Priority:** Medium
**Estimated Duration:** 1-2 hours per account

**Trigger Conditions:**
- Weekly schedule (every Monday recommended)
- Mid-week trigger if performance alert fires

**Inputs Required:**
- 7-day performance data
- KPI targets
- Active test status
- Current campaign registry state

**Outputs Delivered:**
- Optimization actions log
- Updated campaign settings
- Performance improvement documentation
- Flagged issues for escalation

**Quality Gate:** Weekly Optimization Checklist completed

---

### 5. Performance Report Generation

**Category:** Reporting
**Primary Agent:** Reporting Agent
**Supporting Agents:** Diagnostics Agent
**Priority:** Medium
**Estimated Duration:** 1-3 hours

**Trigger Conditions:**
- Scheduled reporting cadence (weekly/monthly/quarterly)
- Ad-hoc request from stakeholder

**Inputs Required:**
- Performance data for reporting period
- KPI targets and benchmarks
- Previous period report (for comparisons)
- Reporting template

**Outputs Delivered:**
- Formatted performance report
- Executive summary
- Data appendix
- Recommendations section

**Quality Gate:** Reporting Quality Checklist completed, all data verified

---

### 6-20: Additional Task Summaries

| Task | Trigger | Key Input | Key Output |
|------|---------|-----------|------------|
| **6. Creative Performance Review** | Monthly or when fatigue detected | Creative performance data, fatigue thresholds | Creative report, rotation plan, new brief |
| **7. Budget Reallocation** | Monthly review or efficiency opportunity | Performance by campaign, marginal analysis | Reallocation plan, updated budgets |
| **8. Audience Analysis & Refresh** | Monthly or audience fatigue | Audience performance, overlap data | Audience report, refresh recommendations |
| **9. Tracking Audit** | Onboarding, discrepancies, quarterly | Tracking config, platform vs. analytics data | Audit report, fix recommendations |
| **10. A/B Test Design** | Hypothesis identified | Hypothesis, baseline data, constraints | Test plan, sample size, duration |
| **11. A/B Test Analysis** | Test duration/sample complete | Test data, significance thresholds | Results report, winner declaration, learnings |
| **12. Competitive Analysis** | Quarterly or competitive shift | Competitor data, market trends | Competitive report, opportunity brief |
| **13. Scaling Assessment** | Growth goal or strong performance | Performance data, creative inventory | Readiness score, scaling plan |
| **14. Compliance Review** | Pre-launch for regulated industries | Ad copy/creative, policy docs | Compliance verdict, required changes |
| **15. Ad Copy Creation** | New campaign or creative refresh | Creative brief, brand voice, audience | Ad copy sets, headline variants, CTAs |
| **16. Creative Brief Development** | New creative needed | Campaign brief, audience data, strategy | Completed creative brief |
| **17. Performance Diagnosis** | Anomaly or decline detected | Performance data, change log, tracking data | Root cause analysis, fix plan |
| **18. Cross-Squad Coordination** | Multi-squad project | Cross-squad requirements, shared assets | Coordination plan, handoff docs |
| **19. Swipe File Update** | Monthly curation cycle | Ad libraries, competitor feeds | Updated swipe files, trend notes |
| **20. New Account Onboarding** | New client or account | Access credentials, business info, goals | Audit, strategy, tracking setup, launch plan |

---

## Task Routing Decision Tree

```
Is this a new account?
  YES --> Task 20: New Account Onboarding
  NO  --> Continue

Is there a performance problem?
  YES --> Is it sudden (< 3 days)?
          YES --> Task 17: Performance Diagnosis
          NO  --> Task 1: Full Account Audit
  NO  --> Continue

Is this a scheduled activity?
  YES --> Match to cadence:
          Daily  --> Task 4 (partial)
          Weekly --> Task 4: Weekly Optimization
          Monthly --> Task 5: Report + Task 6: Creative Review + Task 7: Budget
          Quarterly --> Task 1: Audit + Task 12: Competitive
  NO  --> Continue

Is this a new initiative?
  YES --> Task 2: Strategy --> Task 3: Launch
  NO  --> Match to specific need (copy, testing, scaling, etc.)
```

---

## Priority Definitions

| Priority | Response Time | Description |
|----------|-------------|-------------|
| Critical | Immediate (< 1 hour) | Active revenue loss, broken tracking, account suspension |
| High | Same day (< 8 hours) | Significant performance impact, launch-blocking issues |
| Medium | Within 2 business days | Optimization opportunities, scheduled deliverables |
| Low | Within 1 week | Research, curation, non-urgent improvements |
