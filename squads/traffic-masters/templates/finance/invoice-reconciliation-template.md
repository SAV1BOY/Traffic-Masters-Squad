# Invoice Reconciliation Template

> **Type**: Template
> **Category**: finance
> **Used by tasks**: financial-reconciliation, spend-tracking, accounting
> **Filled by agents**: finance-agent, media-buyer-agent

## Purpose
Tracks and reconciles actual ad platform invoices against platform-reported spend, identifying discrepancies, credits, refunds, and taxes to ensure accurate financial records and budget tracking.

## Template

### Reconciliation Header
**Period**: [month/year]
**Prepared by**: [person or agent]
**Date prepared**: [date]
**Currency**: [USD / EUR / GBP]
**Status**: [in-progress / complete / pending-review]

### Platform Reconciliation

#### Meta Ads
**Account ID**: [ID]
**Account name**: [name]
| Line Item | Amount |
|---|---|
| Invoice amount (from Meta billing) | $[X] |
| Platform reported spend (from Ads Manager) | $[X] |
| Delta (invoice - reported) | $[X] |
| Credits applied | $[X] |
| Refunds received | $[X] |
| Taxes (VAT/GST/Sales tax) | $[X] |
| Net amount charged | $[X] |
**Notes**: [Explanation of any delta, pending credits, billing issues]
**Status**: [reconciled / discrepancy-under-review / resolved]

#### Google Ads
**Account ID**: [ID]
**Account name**: [name]
| Line Item | Amount |
|---|---|
| Invoice amount (from Google billing) | $[X] |
| Platform reported spend (from Google Ads) | $[X] |
| Delta (invoice - reported) | $[X] |
| Credits applied | $[X] |
| Refunds received | $[X] |
| Taxes (VAT/GST/Sales tax) | $[X] |
| Net amount charged | $[X] |
**Notes**: [Explanation]
**Status**: [status]

#### TikTok Ads
**Account ID**: [ID]
**Account name**: [name]
| Line Item | Amount |
|---|---|
| Invoice amount | $[X] |
| Platform reported spend | $[X] |
| Delta | $[X] |
| Credits applied | $[X] |
| Refunds received | $[X] |
| Taxes | $[X] |
| Net amount charged | $[X] |
**Notes**: [Explanation]
**Status**: [status]

#### LinkedIn Ads
**Account ID**: [ID]
| Line Item | Amount |
|---|---|
| Invoice amount | $[X] |
| Platform reported spend | $[X] |
| Delta | $[X] |
| Credits / Refunds | $[X] |
| Taxes | $[X] |
| Net amount charged | $[X] |
**Notes**: [Explanation]
**Status**: [status]

#### Other Platforms
**Platform**: [name]
**Account ID**: [ID]
| Line Item | Amount |
|---|---|
| Invoice amount | $[X] |
| Platform reported spend | $[X] |
| Delta | $[X] |
| Credits / Refunds | $[X] |
| Taxes | $[X] |
| Net amount charged | $[X] |
**Notes**: [Explanation]
**Status**: [status]

### Summary Table
| Platform | Invoice | Reported Spend | Delta | Credits | Taxes | Net Charged | Status |
|---|---|---|---|---|---|---|---|
| Meta | $[X] | $[X] | $[X] | $[X] | $[X] | $[X] | [status] |
| Google | $[X] | $[X] | $[X] | $[X] | $[X] | $[X] | [status] |
| TikTok | $[X] | $[X] | $[X] | $[X] | $[X] | $[X] | [status] |
| LinkedIn | $[X] | $[X] | $[X] | $[X] | $[X] | $[X] | [status] |
| Other | $[X] | $[X] | $[X] | $[X] | $[X] | $[X] | [status] |
| **Total** | **$[X]** | **$[X]** | **$[X]** | **$[X]** | **$[X]** | **$[X]** | |

### Budget vs. Actual
| Category | Approved Budget | Actual Spend | Variance | Variance % |
|---|---|---|---|---|
| Meta Ads | $[X] | $[X] | $[X] | [+/- %] |
| Google Ads | $[X] | $[X] | $[X] | [+/- %] |
| TikTok Ads | $[X] | $[X] | $[X] | [+/- %] |
| Creative production | $[X] | $[X] | $[X] | [+/- %] |
| Tools/software | $[X] | $[X] | $[X] | [+/- %] |
| **Total** | **$[X]** | **$[X]** | **$[X]** | **[%]** |

### Discrepancy Log
| Date Identified | Platform | Amount | Description | Resolution | Status |
|---|---|---|---|---|---|
| [date] | [platform] | $[X] | [description of discrepancy] | [how resolved] | [open/resolved] |
| [date] | [platform] | $[X] | [description] | [resolution] | [status] |

### Pending Items
| Item | Platform | Amount | Expected Resolution Date | Owner |
|---|---|---|---|---|
| [Pending credit] | [platform] | $[X] | [date] | [owner] |
| [Disputed charge] | [platform] | $[X] | [date] | [owner] |

### Sign-Off
**Prepared by**: [name, date]
**Reviewed by**: [name, date]
**Approved by**: [name, date]

## Usage Notes
- Complete reconciliation within 10 business days of month end.
- Small deltas (under 2%) between invoice and reported spend are normal due to timing.
- Flag any delta exceeding 5% for investigation.
- Keep copies of all invoices in the shared finance folder.

## Example
March reconciliation: Meta invoiced $31,450 vs. $31,200 reported spend ($250 delta from timezone difference). Google invoiced $15,800 with $500 credit applied for invalid clicks. Total net charged across platforms: $52,100 vs. $55,000 budget (5.3% under budget).

## Related
- budget-approval-template.md
- cost-center-mapping-template.md
- media-plan-template.md
