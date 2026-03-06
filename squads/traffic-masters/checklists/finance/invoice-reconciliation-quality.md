# Invoice and Spend Reconciliation Quality Gate

> Quality gate for invoice processing and media spend reconciliation across all platforms. Must pass before invoices are approved for payment or client billing.

## Section 1: Platform Spend Verification
- [ ] Actual spend per platform is exported from the ad platform's billing section (not from the campaign dashboard, which may differ)
- [ ] Spend data covers the exact billing period (matching invoice dates, not campaign flight dates if different)
- [ ] Currency conversions are applied using the correct exchange rate (platform rate vs. bank rate documented)
- [ ] Ad platform spend is reconciled against the approved media plan budget (variance documented)
- [ ] Any overspend or underspend exceeding 5% of planned budget is explained with documented reasons

## Section 2: Invoice Validation
- [ ] Invoice amounts match the ad platform billing statements to the cent
- [ ] Invoice dates, billing periods, and payment terms are correct
- [ ] Tax amounts (VAT, ISS, IOF for Brazil) are calculated correctly per local regulations
- [ ] Agency management fee is calculated correctly based on the contracted percentage or flat fee
- [ ] Invoice line items are detailed enough for client transparency (platform, campaign type, period, amount)

## Section 3: Cross-Platform Reconciliation
- [ ] Total media spend across all platforms is summed and compared to the total approved budget
- [ ] Spend breakdown by platform matches the allocation plan (or deviations are documented and approved)
- [ ] Refunds, credits, or adjustments from ad platforms are tracked and applied to the reconciliation
- [ ] Discrepancies between ad platform charges and credit card/bank statements are investigated and resolved
- [ ] Reconciliation spreadsheet is maintained with monthly records for audit trail

## Section 4: Client Billing Accuracy
- [ ] Client invoice includes all media spend with platform-level breakdown
- [ ] Markup or management fees are applied per the contract terms
- [ ] Proof of spend (platform billing screenshots or exports) is available upon client request
- [ ] Client billing currency and exchange rates are applied consistently per the contract
- [ ] Payment schedule is adhered to (net 15, net 30, or as contracted)

## Section 5: Documentation and Compliance
- [ ] All invoices are stored in the designated financial system with proper categorization
- [ ] Reconciliation report is reviewed and signed off by the finance lead
- [ ] Discrepancies above $100 or 2% are escalated and resolved before invoice approval
- [ ] Audit trail exists for all budget changes, reallocations, and spend adjustments
- [ ] Monthly reconciliation is completed within 5 business days of the billing period close
- [ ] Supporting documents (platform exports, bank statements, exchange rate records) are archived

## Approval
- **Minimum pass rate**: 19/23 items (83%)
- **Reviewer**: finance-agent + account-manager-agent
- **Escalation**: Unreconciled discrepancies above 5% or missing tax documentation are hard blocks; invoice is not approved for payment until resolved
