# Budget Approval

> **Type**: Task
> **Category**: finance
> **Agents**: Fiscal, Traffic Chief
> **Frameworks**: Budget Approval Workflow, Financial Controls Framework
> **Checklists**: budget-approval-checklist
> **Output template**: templates/approved-budget.md

## ROUTING (from config.yaml)

> **Config key**: `routing.budget-approval`
> **Agents**: [fiscal](../../agents/fiscal.md), [traffic-chief](../../agents/traffic-chief.md)
> **Frameworks**: `governance-layer`, `budget-allocation-model`
> **Checklists**: `finance/budget-approval`
> **Templates**: `finance/budget-approval-template`
> **Registry**: `data/registries/budgets-and-guardrails`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Execute the budget approval process to authorize media spend, ensure financial controls are in place, validate budget alignment with business objectives, and create a documented approval record for financial accountability.

## Inputs
- Budget allocation plan with channel-level detail
- Business revenue targets and growth objectives
- Historical ROAS or CPA data to support projections
- Cash flow constraints and payment terms per platform
- Projected unit economics at proposed spend levels
- Previous period budget performance (actual vs planned)

## Steps
1. Review the proposed budget allocation against business revenue targets
2. Validate projected ROI: does the expected return justify the proposed investment
3. Check cash flow timing: align budget commitments with available cash and billing cycles
4. Verify platform payment methods and credit limits can support proposed spend
5. Review budget increase justification: performance data supporting the scale-up
6. Assess risk: what is the maximum potential loss if campaigns underperform
7. Define budget controls: daily caps, weekly review thresholds, emergency pause triggers
8. Confirm tax implications of media spend: input credits, withholding requirements
9. Set up budget tracking mechanisms: automated alerts at 80% and 100% of monthly budget
10. Document approval with signatures, date, conditions, and review schedule
11. Communicate approved budget to Media Buyer and Performance Analyst
12. Schedule the next budget review based on the approved period

## Output
Approved budget document containing: authorized spend by channel, approval conditions, financial controls, payment method confirmation, risk assessment, tax notes, budget tracking setup, and next review date.

## Quality Gate
- Budget approval checklist confirms all financial controls documented
- Projected ROI validated against historical performance data
- Fiscal and Traffic Chief both sign off on the approval

## Duration
1-2 hours for review and approval process
