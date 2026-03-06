# Cohort Analysis Reference
> **Category**: Analytics Methodology
> **Last Updated**: 2026-03

## Overview
Cohort analysis groups users by shared characteristics (typically acquisition date) and tracks their behavior over time. It reveals retention, LTV, and payback period patterns invisible in aggregate data.

## Key Cohort Types
- **Acquisition Cohort**: Users grouped by when they were acquired (week/month)
- **Behavioral Cohort**: Users grouped by action taken (e.g., watched video, added to cart)
- **Source Cohort**: Users grouped by traffic source (Meta vs Google vs organic)

## Essential Metrics by Cohort
- **Retention Rate**: % of users who return after Day 1, 7, 14, 30
- **LTV by Cohort**: Total revenue per user over time for each cohort
- **Payback Period**: How many days/months until CPA is recovered by revenue
- **Repeat Purchase Rate**: % of first-time buyers who buy again

## How to Build a Cohort Report
1. Define cohort grouping (acquisition week, source, campaign)
2. Define time periods (Day 0, Day 7, Day 14, Day 30, Day 60, Day 90)
3. Define metric to track (revenue, purchases, logins, engagement)
4. Create cohort table: rows = cohorts, columns = time periods
5. Calculate metric at each intersection

## Application to Traffic
- Compare LTV by acquisition source to determine true channel value
- Identify if specific campaigns attract higher-value customers
- Determine payback period to set accurate CPA targets
- Spot quality degradation as campaigns scale (cohort LTV declining)

## Key Takeaways
- Aggregate metrics hide cohort-level truth — always segment
- A campaign with higher CPA may be more profitable if its cohort LTV is higher
- Declining cohort quality is an early warning sign of scaling issues
- Payback period determines how aggressive you can be with CPA targets
- Share cohort data with the team to align on true performance
