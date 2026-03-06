# Cost Center Mapping Template

> **Type**: Template
> **Category**: finance
> **Used by tasks**: financial-tracking, budget-allocation, accounting-integration
> **Filled by agents**: finance-agent, strategist-agent

## Purpose
Maps every campaign to its corresponding cost center, business unit, and budget owner, ensuring ad spend is correctly attributed in financial systems and UTM parameters align with financial reporting requirements.

## Template

### Mapping Metadata
**Company**: [company name]
**Fiscal year**: [year]
**Last updated**: [date]
**Maintained by**: [person or agent]
**Finance contact**: [person for cost center questions]

### Cost Center Directory
| Cost Center Code | Department / Function | Budget Owner | Annual Budget | Notes |
|---|---|---|---|---|
| [CC-001] | [Marketing - Acquisition] | [owner name] | $[X] | [primary paid media] |
| [CC-002] | [Marketing - Brand] | [owner name] | $[X] | [awareness campaigns] |
| [CC-003] | [Marketing - Retention] | [owner name] | $[X] | [retargeting, email] |
| [CC-004] | [Sales - Lead Gen] | [owner name] | $[X] | [B2B lead campaigns] |
| [CC-005] | [Product - Launch] | [owner name] | $[X] | [new product launches] |
| [CC-006] | [Creative - Production] | [owner name] | $[X] | [creative assets] |
| [CC-007] | [Technology - Tools] | [owner name] | $[X] | [software, analytics] |

### Campaign to Cost Center Mapping
| Campaign Name | Platform | Cost Center | Business Unit | Budget Owner | Monthly Budget | Approval Status |
|---|---|---|---|---|---|---|
| [meta_conv_lal1pct_tofu_202603] | Meta | [CC-001] | [Marketing] | [owner] | $[X] | [approved] |
| [google_search_brand_bofu_202603] | Google | [CC-001] | [Marketing] | [owner] | $[X] | [approved] |
| [meta_conv_rtg_bofu_202603] | Meta | [CC-003] | [Marketing] | [owner] | $[X] | [approved] |
| [linkedin_lead_b2b_tofu_202603] | LinkedIn | [CC-004] | [Sales] | [owner] | $[X] | [approved] |
| [meta_conv_launch_tofu_202603] | Meta | [CC-005] | [Product] | [owner] | $[X] | [approved] |
| [creative_production_march] | N/A | [CC-006] | [Creative] | [owner] | $[X] | [approved] |
| [tools_analytics_q1] | N/A | [CC-007] | [Technology] | [owner] | $[X] | [approved] |

### UTM to Cost Center Mapping
| UTM Campaign Value | Cost Center | Business Unit | Notes |
|---|---|---|---|
| conv-lal1pct-tofu-* | [CC-001] | Marketing - Acquisition | All TOFU prospecting |
| conv-rtg-*-bofu-* | [CC-003] | Marketing - Retention | All retargeting |
| search-brand-*-bofu-* | [CC-001] | Marketing - Acquisition | Brand search |
| lead-*-tofu-* | [CC-004] | Sales - Lead Gen | B2B lead generation |
| launch-*-* | [CC-005] | Product - Launch | Product launches |

**UTM parsing rules**: [How UTM campaign values are parsed to determine cost center assignment]

### Approval Matrix
| Spend Level | Required Approvals |
|---|---|
| Under $1,000/month | Budget owner only |
| $1,000 - $5,000/month | Budget owner + Marketing Director |
| $5,000 - $20,000/month | Budget owner + Marketing Director + Finance |
| Over $20,000/month | Budget owner + Marketing Director + Finance + Executive |

### New Campaign Process
1. Determine the campaign's business objective and funnel stage
2. Identify the appropriate cost center from the directory
3. Confirm budget availability with the budget owner
4. Obtain required approvals per the approval matrix
5. Add the campaign to this mapping document
6. Ensure UTM campaign value follows naming conventions
7. Confirm the mapping in the finance system

### Monthly Reconciliation Checklist
- [ ] All active campaigns are mapped to a cost center
- [ ] No campaign is running without an approved cost center
- [ ] New campaigns added this month are documented
- [ ] Paused or ended campaigns are marked accordingly
- [ ] Total spend per cost center aligns with budget approvals
- [ ] UTM-based attribution matches cost center assignments
- [ ] Discrepancies are flagged and resolved

### Reporting Integration
**ERP/Accounting system**: [system name]
**Export format**: [CSV / API / manual entry]
**Export frequency**: [monthly / weekly]
**Data fields exported**: [campaign name, cost center, spend, platform, date]
**Responsible party**: [who handles the export]

### Change Log
| Date | Change | Reason | Updated By |
|---|---|---|---|
| [date] | [Added CC-005 for product launches] | [New product line] | [name] |
| [date] | [Moved retargeting from CC-001 to CC-003] | [Budget restructure] | [name] |
| [date] | [Updated approval thresholds] | [Finance policy change] | [name] |

## Usage Notes
- Review this mapping monthly as part of the financial reconciliation process.
- Every new campaign must be assigned a cost center before going live.
- When budget owners change, update this document and notify finance.
- Keep this document in a shared location accessible to marketing and finance teams.

## Example
Ecommerce company with 4 cost centers: Acquisition (CC-001, $40k/month), Brand (CC-002, $10k/month), Retention (CC-003, $8k/month), and Creative (CC-006, $5k/month). Each Meta and Google campaign maps to one cost center. UTM campaigns starting with "conv-" map to CC-001, "rtg-" to CC-003.

## Related
- budget-approval-template.md
- invoice-reconciliation-template.md
- campaign-naming-standard.md
- utm-standard.md
