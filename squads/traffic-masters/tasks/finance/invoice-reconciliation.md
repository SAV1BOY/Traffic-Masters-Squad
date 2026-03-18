# Invoice Reconciliation

> **Type**: Task
> **Category**: finance
> **Agents**: Fiscal
> **Frameworks**: Financial Reconciliation Framework, Platform Billing Audit
> **Checklists**: invoice-reconciliation-checklist
> **Output template**: templates/reconciliation-report.md

## ROUTING (from config.yaml)

> **Config key**: `routing.invoice-reconciliation`
> **Agents**: [fiscal](../../agents/fiscal.md)
> **Frameworks**: `governance-layer`
> **Checklists**: `financial-reconciliation-quality`, `finance/invoice-vs-platform-audit`
> **Templates**: `finance/invoice-reconciliation-template`
> **Registry**: `data/registries/decisions-log`
> **Escalation**: Traffic Chief if quality gate fails 2x → see `config.yaml > rework_loop`
> **Rework**: Max 3 iterations per gate → team lead → Traffic Chief


## Objective
Reconcile advertising invoices and billing statements against platform-reported spend and internal budget tracking to ensure billing accuracy, catch discrepancies, and maintain clean financial records.

## Inputs
- Platform invoices and billing statements: Meta, Google, TikTok, LinkedIn, etc.
- Platform dashboard spend reports for the billing period
- Internal budget tracking spreadsheet with daily actuals
- Credit card or payment method statements
- Currency exchange rates (if applicable for international spend)
- Tax documentation: IOF, ISS, withholding tax records

## Steps
1. Export billing data from each platform for the reconciliation period
2. Pull corresponding invoices or billing statements from each platform
3. Compare platform-reported spend against invoice amounts per platform
4. Check for billing adjustments, credits, or refunds applied during the period
5. Compare platform invoices against credit card or bank statements
6. Reconcile internal budget tracking totals against platform-reported actuals
7. Identify and investigate any discrepancies exceeding the tolerance threshold (typically 1-2%)
8. Document currency conversion differences for international platform billing
9. Verify tax charges: are the correct tax rates applied per jurisdiction
10. Check for any unauthorized charges or unexpected billing line items
11. Calculate total actual media cost including fees, taxes, and currency adjustments
12. File reconciled records and update the financial tracking system

## Output
Reconciliation report containing: platform-by-platform billing comparison, discrepancy log with explanations, tax verification, total media cost calculation, credit/refund tracking, and filed reconciliation records.

## Quality Gate
- Invoice reconciliation checklist confirms all platforms and payment methods reconciled
- All discrepancies above tolerance threshold investigated and resolved
- Fiscal signs off on the reconciliation as accurate and complete

## Duration
1-3 hours monthly depending on number of platforms and billing complexity
