# Spend Reconciliation Template

## Reconciliation Metadata

| Field | Value |
|---|---|
| **Reconciliation Period** | `{{START_DATE}}` to `{{END_DATE}}` |
| **Prepared By** | `{{PREPARER_NAME}}` |
| **Client / Account** | `{{CLIENT_NAME}}` |
| **Currency** | `{{CURRENCY}}` |
| **Date Prepared** | `{{DATE}}` |
| **Status** | `{{DRAFT / IN REVIEW / RECONCILED / DISPUTED}}` |

---

## Summary

| Category | Platform-Reported Spend | Invoice Amount | Variance ($) | Variance (%) | Status |
|---|---|---|---|---|---|
| Meta Ads | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% | `{{MATCHED/DISCREPANCY}}` |
| Google Ads | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% | `{{}}` |
| TikTok Ads | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% | `{{}}` |
| YouTube Ads | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% | `{{}}` |
| LinkedIn Ads | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% | `{{}}` |
| Other Platforms | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% | `{{}}` |
| **Subtotal: Media** | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% | `{{}}` |
| Creative Production | -- | $`{{}}` | -- | -- | `{{}}` |
| Agency Fees | -- | $`{{}}` | -- | -- | `{{}}` |
| Tools / Software | -- | $`{{}}` | -- | -- | `{{}}` |
| **Grand Total** | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% | `{{}}` |

---

## Platform-Level Reconciliation Detail

### Meta Ads

| Account | Account ID | Platform Spend | Invoice Amount | Variance | Notes |
|---|---|---|---|---|---|
| `{{ACCOUNT_1}}` | `{{ID}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}` |
| `{{ACCOUNT_2}}` | `{{ID}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}` |
| **Meta Total** | -- | $`{{}}` | $`{{}}` | $`{{}}` | -- |

### Google Ads

| Account | Account ID | Platform Spend | Invoice Amount | Variance | Notes |
|---|---|---|---|---|---|
| `{{ACCOUNT_1}}` | `{{ID}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}` |
| **Google Total** | -- | $`{{}}` | $`{{}}` | $`{{}}` | -- |

### TikTok Ads

| Account | Account ID | Platform Spend | Invoice Amount | Variance | Notes |
|---|---|---|---|---|---|
| `{{ACCOUNT_1}}` | `{{ID}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}` |
| **TikTok Total** | -- | $`{{}}` | $`{{}}` | $`{{}}` | -- |

---

## Variance Analysis

### Discrepancies Identified

| Platform | Variance | Likely Cause | Resolution | Owner | Status |
|---|---|---|---|---|---|
| `{{}}` | $`{{}}` | `{{CURRENCY_CONVERSION / TIMING / CREDITS / TAX / REFUND / ERROR}}` | `{{}}` | `{{}}` | `{{RESOLVED/PENDING/ESCALATED}}` |

### Common Variance Causes

| Cause | Description | Typical Impact |
|---|---|---|
| **Currency Conversion** | Exchange rate differences between platform billing and invoice | 1-3% variance |
| **Billing Cycle Mismatch** | Platform billing date differs from calendar month close | Variable |
| **Ad Credits Applied** | Promotional credits applied but not reflected in invoice | Reduces invoice |
| **Tax / VAT** | Tax included in invoice but not in platform dashboard | Increases invoice |
| **Refunds / Adjustments** | Platform-issued refunds for invalid traffic | Reduces spend |
| **Rounding** | Small rounding differences across line items | < $1 typically |

---

## Budget vs. Actual vs. Invoice

| Channel | Approved Budget | Platform Spend | Invoice Amount | vs. Budget ($) | vs. Budget (%) |
|---|---|---|---|---|---|
| Meta Ads | $`{{}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| Google Ads | $`{{}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| TikTok Ads | $`{{}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| Other | $`{{}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |
| **Total** | $`{{}}` | $`{{}}` | $`{{}}` | $`{{}}` | `{{}}`% |

---

## Invoice Checklist

| Check | Status | Notes |
|---|---|---|
| All invoices received | `{{YES/NO}}` | `{{}}` |
| Invoice amounts match platform spend | `{{YES/NO}}` | `{{}}` |
| Correct billing entity on invoices | `{{YES/NO}}` | `{{}}` |
| Tax / VAT correctly applied | `{{YES/NO}}` | `{{}}` |
| Credits and refunds accounted for | `{{YES/NO}}` | `{{}}` |
| Currency conversion verified | `{{YES/NO}}` | `{{}}` |
| Payment terms confirmed | `{{YES/NO}}` | `{{}}` |
| PO numbers correct | `{{YES/NO}}` | `{{}}` |

---

## Payment Schedule

| Invoice | Vendor | Amount | Due Date | Payment Status | Payment Date |
|---|---|---|---|---|---|
| `{{INVOICE_NUM}}` | `{{}}` | $`{{}}` | `{{}}` | `{{PAID/PENDING/OVERDUE}}` | `{{}}` |

---

## Adjustments and Credits

| Type | Platform | Amount | Reason | Applied Date | Reference |
|---|---|---|---|---|---|
| Credit | `{{}}` | $`{{}}` | `{{}}` | `{{}}` | `{{}}` |
| Refund | `{{}}` | $`{{}}` | `{{}}` | `{{}}` | `{{}}` |
| Adjustment | `{{}}` | $`{{}}` | `{{}}` | `{{}}` | `{{}}` |

---

## Sign-Off

| Role | Name | Signature | Date |
|---|---|---|---|
| Preparer | `{{}}` | __________ | `{{}}` |
| Reviewer | `{{}}` | __________ | `{{}}` |
| Approver | `{{}}` | __________ | `{{}}` |

---

## Notes

`{{ADDITIONAL_NOTES}}`

---

*Reconciliation prepared on `{{DATE}}`. All amounts in `{{CURRENCY}}`. Exchange rates as of `{{RATE_DATE}}`. Discrepancies exceeding `{{THRESHOLD}}`% flagged for review.*
