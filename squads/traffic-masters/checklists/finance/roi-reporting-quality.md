# ROI and Financial Reporting Quality Gate

> Quality gate for ROI calculation, financial performance reporting, and business impact analysis. Must pass before financial reports are delivered to stakeholders.

## Section 1: Revenue Attribution
- [ ] Revenue data source is documented and verified (e-commerce platform, CRM, ERP, or client-provided data)
- [ ] Revenue attribution model is defined: last-click, first-click, data-driven, or custom weighted model
- [ ] Revenue is attributed to the correct campaigns and platforms based on the agreed attribution model
- [ ] Revenue includes only conversions within the campaign attribution window (no stale or misattributed revenue)
- [ ] Assisted revenue and direct revenue are reported separately for multi-touch attribution visibility

## Section 2: Cost Tracking Accuracy
- [ ] Media spend includes all ad platform costs (no missing platforms or campaigns)
- [ ] Agency fees, production costs, and tool costs are included in total investment calculation (if reporting total ROI vs. media-only ROAS)
- [ ] Cost data is reconciled against platform billing (see invoice-reconciliation-quality.md)
- [ ] Cost allocation to campaigns/channels is accurate (no pooled costs misassigned)
- [ ] Currency is consistent across all cost and revenue calculations

## Section 3: ROI and ROAS Calculations
- [ ] ROAS formula is correctly applied: Revenue / Ad Spend (not inverted or including non-media costs unless specified)
- [ ] ROI formula is correctly applied: (Revenue - Total Investment) / Total Investment x 100
- [ ] Blended ROAS (all platforms combined) and platform-specific ROAS are both reported
- [ ] CPA (Cost Per Acquisition) is calculated per platform, campaign, and funnel stage
- [ ] CAC (Customer Acquisition Cost) includes all costs, not just media spend, for holistic business reporting
- [ ] LTV:CAC ratio is calculated when customer lifetime value data is available

## Section 4: Report Structure and Presentation
- [ ] Executive summary opens with key financial KPIs: total spend, total revenue, ROAS, ROI, CPA
- [ ] Performance is compared to targets set in the media plan (actual vs. goal with variance)
- [ ] Time-over-time trends are shown: WoW, MoM, QoQ, YoY as appropriate
- [ ] Platform-level breakdown shows contribution of each channel to total performance
- [ ] Funnel-stage breakdown shows prospecting vs. retargeting vs. retention economics

## Section 5: Insights and Recommendations
- [ ] Budget reallocation recommendations are backed by financial data (shift spend to highest ROAS channels)
- [ ] Underperforming campaigns are identified with specific financial impact (wasted spend quantified)
- [ ] Scaling opportunities are identified with projected financial impact (if we increase budget by X, expected revenue lift is Y)
- [ ] Report includes confidence level in the data (known tracking gaps, attribution limitations documented)
- [ ] Next period financial targets are proposed based on current trends and business goals

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: finance-agent + analytics-agent
- **Escalation**: Revenue attribution errors or incorrect ROI calculations are hard blocks; report must be corrected before delivery to stakeholders
