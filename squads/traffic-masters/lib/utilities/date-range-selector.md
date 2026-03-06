# Date Range Selector Utility

## Purpose
Standard date range definitions for consistent reporting and analysis across paid traffic campaigns. Eliminates ambiguity in period comparisons.

---

## Standard Date Ranges

### Daily Ranges

| Range Name | Definition | Use Case |
|---|---|---|
| **Today** | Current calendar day (midnight to now, account timezone) | Real-time monitoring |
| **Yesterday** | Previous complete calendar day | Daily performance report |
| **Last 3 Days** | Yesterday + 2 prior days | Short-term trend check |
| **Last 7 Days** | Yesterday + 6 prior days (7 complete days) | Weekly trend analysis |
| **Last 14 Days** | Yesterday + 13 prior days | Two-week performance review |
| **Last 30 Days** | Yesterday + 29 prior days | Monthly-equivalent rolling window |

**Important:** "Last X Days" should always use COMPLETE days (exclude today's partial data for accuracy).

### Weekly Ranges

| Range Name | Definition | Use Case |
|---|---|---|
| **This Week** | Monday 00:00 to now (current partial week) | In-progress week monitoring |
| **Last Week** | Previous Monday 00:00 to Sunday 23:59 | Weekly performance report |
| **Last 2 Weeks** | 2 most recent complete Mon-Sun weeks | Bi-weekly comparison |
| **Last 4 Weeks** | 4 most recent complete Mon-Sun weeks | Monthly-equivalent weekly view |

**Note:** Weeks run Monday through Sunday unless otherwise specified by client preference.

### Monthly Ranges

| Range Name | Definition | Use Case |
|---|---|---|
| **This Month (MTD)** | 1st of current month to yesterday | Month-to-date pacing |
| **Last Month** | 1st to last day of previous calendar month | Monthly performance report |
| **Last 3 Months** | 3 most recent complete calendar months | Quarterly trend |
| **Last 6 Months** | 6 most recent complete calendar months | Half-year trend |
| **Last 12 Months** | 12 most recent complete calendar months | Annual trend |

### Quarterly Ranges

| Range Name | Definition | Use Case |
|---|---|---|
| **This Quarter (QTD)** | Start of current quarter to yesterday | Quarter-to-date pacing |
| **Last Quarter** | Previous complete calendar quarter | Quarterly report |
| **Year over Year Quarter** | Same quarter in the previous year | YoY quarterly comparison |

**Quarter Definitions:**
- Q1: January 1 - March 31
- Q2: April 1 - June 30
- Q3: July 1 - September 30
- Q4: October 1 - December 31

### Year Ranges

| Range Name | Definition | Use Case |
|---|---|---|
| **YTD (Year to Date)** | January 1 to yesterday | Annual pacing |
| **Last Year** | January 1 to December 31 of previous year | Annual review |
| **Rolling 12 Months** | Last 365 complete days | Non-calendar annual view |

---

## Comparison Periods

### Standard Comparisons

| Primary Period | Compare To | Label | Purpose |
|---|---|---|---|
| Yesterday | Day before | DoD (Day over Day) | Daily fluctuation |
| Yesterday | Same day last week | vs. Same Day LW | Day-of-week normalized |
| Last Week | Week before | WoW (Week over Week) | Weekly trend |
| Last Week | Same week last month | vs. Same Week LM | Month-normalized weekly |
| Last Month | Month before | MoM (Month over Month) | Monthly trend |
| Last Month | Same month last year | YoY (Year over Year) | Seasonal comparison |
| Last Quarter | Quarter before | QoQ (Quarter over Quarter) | Quarterly trend |
| Last Quarter | Same quarter last year | YoY Quarter | Annual seasonal comparison |

### How to Handle Unequal Period Lengths

| Situation | Solution |
|---|---|
| Comparing months with different days (28 vs. 31) | Use daily averages instead of totals |
| Comparing weeks with holidays | Note the holiday; show with and without holiday days |
| Comparing periods with different business days | Normalize by business day count |
| Partial period (MTD) vs. full prior month | Project current month based on pacing, or compare same # of days |

### Same-Days Comparison
When comparing MTD to previous month, use the same number of elapsed days:

```
This Month (MTD): March 1-15 (15 days elapsed)
Compare to: February 1-15 (same 15 days of previous month)
NOT: Full February (28 days)
```

---

## Attribution Windows and Delays

### Platform-Specific Attribution Delays

| Platform | Typical Attribution Delay | Recommendation |
|---|---|---|
| Meta Ads | 24-72 hours for complete attribution | Wait 48 hours before finalizing data |
| Google Ads | 24-48 hours | Wait 24 hours |
| TikTok Ads | 24-48 hours | Wait 48 hours |
| GA4 | 24-48 hours for processing | Wait 48 hours |

### Reporting Date vs. Conversion Date
- **Reporting Date:** The date the ad was shown/clicked (used by most platforms)
- **Conversion Date:** The date the conversion actually occurred
- **Impact:** A click on Day 1 that converts on Day 5 is reported as a Day 1 conversion in most platforms

### Best Practice
- **Daily reports:** Pull data for yesterday (not today) to allow attribution to settle
- **Weekly reports:** Pull Monday for last Mon-Sun; allow 24-48 hours buffer
- **Monthly reports:** Pull on the 2nd or 3rd of the following month

---

## Timezone Handling

### Default Timezone
All date ranges should be calculated in the **ad account timezone** unless otherwise specified.

### Multi-Timezone Accounts
If managing accounts across timezones:
1. Choose one "reporting timezone" as the standard
2. Document which timezone is used in every report
3. Note that platform data may be in a different timezone than the reporting timezone
4. GA4 data is in the property's configured timezone

---

## Special Periods

### Seasonal and Event Periods

| Period | Typical Dates | Impact |
|---|---|---|
| **Black Friday / Cyber Monday** | Last Friday of November + following Monday | Highest volume, lowest organic CPA |
| **Holiday Season** | November 15 - December 31 | High CPM, high competition |
| **Post-Holiday Slump** | January 1-15 | Low conversion rates, buyer fatigue |
| **Tax Season (US)** | February - April 15 | Relevant for financial services |
| **Back to School** | July 15 - September 15 | Relevant for education, retail |
| **Summer Slowdown** | June - August | Lower B2B engagement |

### Handling Seasonal Comparisons
- Compare to the same seasonal period last year (not the prior month)
- Note if major dates shifted (e.g., Black Friday date changes yearly)
- Use indexed comparison: performance relative to seasonal average

---

## Report Cadence Quick Reference

| Report | Date Range | Comparison | Pull Date | Due Date |
|---|---|---|---|---|
| Daily | Yesterday | Previous day + same day LW | Day of (after 10 AM) | Same day by noon |
| Weekly | Last Mon-Sun | Previous week + 4-week trend | Monday | Monday by EOD |
| Monthly | Last calendar month | Previous month + YoY | 2nd of month | 3rd business day |
| Quarterly | Last calendar quarter | Previous quarter + YoY | 2nd of new quarter | 5th business day |
