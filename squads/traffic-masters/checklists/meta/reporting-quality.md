# Meta Reporting and Attribution Quality Gate

> Quality gate for Meta reporting setup and attribution configuration. Must pass before campaign performance reports are delivered to stakeholders.

## Section 1: Attribution Model Configuration
- [ ] Attribution window is documented and consistent across all campaigns (default: 7-day click, 1-day view)
- [ ] Attribution window matches the client's purchase consideration cycle (short for impulse, longer for high-ticket)
- [ ] View-through attribution is included or excluded with documented business justification
- [ ] Cross-device attribution is enabled (Meta default) and understood by the reporting audience
- [ ] Attribution comparison reports have been run to understand impact of different windows

## Section 2: Reporting Columns and Metrics
- [ ] Custom columns in Ads Manager include all KPIs from the media plan (CPA, ROAS, CPM, CTR, Frequency)
- [ ] Cost metrics use the correct denominator (cost per result, not cost per impression, unless intended)
- [ ] Breakdown dimensions are applied appropriately (age, gender, placement, device, time of day)
- [ ] Conversion metrics are filtered by the correct conversion event (Purchase, Lead, etc.)
- [ ] Custom metrics (e.g., Thumb Stop Rate = 3s video views / impressions) are created and validated

## Section 3: Data Accuracy Validation
- [ ] Meta-reported conversions are cross-referenced with backend data (CRM, e-commerce platform) within 10% variance
- [ ] Revenue values in Meta match actual revenue from the source of truth (accounting for returns/cancellations)
- [ ] Discrepancies above 10% are investigated and root cause is documented
- [ ] Pixel/CAPI event counts match between Events Manager and Ads Manager reporting
- [ ] UTM-attributed conversions in GA4 are compared with Meta self-reported data for directional validation

## Section 4: Report Structure and Delivery
- [ ] Reporting template includes: executive summary, KPI dashboard, platform breakdown, and recommendations
- [ ] Reports are segmented by funnel stage (prospecting vs. retargeting vs. retention)
- [ ] Time comparison periods are consistent (WoW, MoM) and account for seasonality
- [ ] Automated report exports are scheduled (weekly or as agreed with the client)
- [ ] Data freshness is noted on reports (Meta data can have 24-72h delay for final numbers)

## Section 5: Insights and Action Items
- [ ] Each report includes at least 3 actionable insights derived from the data
- [ ] Underperforming campaigns/ad sets are flagged with recommended next steps
- [ ] Creative performance ranking is included with fatigue indicators (frequency, CTR trend)
- [ ] Budget reallocation recommendations are data-driven and tied to specific metrics
- [ ] Next reporting period goals and benchmarks are established

## Approval
- **Minimum pass rate**: 19/23 items (83%)
- **Reviewer**: analytics-agent + account-manager-agent
- **Escalation**: If data accuracy validation fails (>10% discrepancy unresolved), reporting is flagged as provisional until investigation is complete
