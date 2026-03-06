# Timezone Reference

## Purpose
Timezone reference for global campaign scheduling, reporting alignment, and cross-market coordination in paid traffic operations.

---

## Major Advertising Timezones

### Americas

| Timezone | Abbreviation | UTC Offset | Major Markets | DST? |
|---|---|---|---|---|
| Eastern Time | ET (EST/EDT) | UTC-5 / UTC-4 | New York, Miami, Toronto, Bogota | Yes |
| Central Time | CT (CST/CDT) | UTC-6 / UTC-5 | Chicago, Dallas, Mexico City | Yes |
| Mountain Time | MT (MST/MDT) | UTC-7 / UTC-6 | Denver, Phoenix (no DST) | Varies |
| Pacific Time | PT (PST/PDT) | UTC-8 / UTC-7 | Los Angeles, San Francisco, Vancouver | Yes |
| Alaska Time | AKT | UTC-9 / UTC-8 | Anchorage | Yes |
| Hawaii Time | HST | UTC-10 | Honolulu | No |
| Brasilia Time | BRT | UTC-3 | Sao Paulo, Rio de Janeiro | No |
| Argentina Time | ART | UTC-3 | Buenos Aires | No |
| Colombia Time | COT | UTC-5 | Bogota | No |

### Europe

| Timezone | Abbreviation | UTC Offset | Major Markets | DST? |
|---|---|---|---|---|
| Greenwich Mean Time | GMT/WET | UTC+0 / UTC+1 | London, Dublin, Lisbon | Yes (BST/WEST) |
| Central European Time | CET | UTC+1 / UTC+2 | Berlin, Paris, Madrid, Amsterdam, Rome | Yes (CEST) |
| Eastern European Time | EET | UTC+2 / UTC+3 | Helsinki, Athens, Bucharest | Yes (EEST) |
| Moscow Time | MSK | UTC+3 | Moscow, Istanbul | No |

### Asia Pacific

| Timezone | Abbreviation | UTC Offset | Major Markets | DST? |
|---|---|---|---|---|
| Gulf Standard Time | GST | UTC+4 | Dubai, Abu Dhabi | No |
| India Standard Time | IST | UTC+5:30 | Mumbai, Delhi, Bangalore | No |
| Indochina Time | ICT | UTC+7 | Bangkok, Ho Chi Minh City | No |
| China Standard Time | CST | UTC+8 | Beijing, Shanghai, Hong Kong, Singapore, Taipei | No |
| Japan Standard Time | JST | UTC+9 | Tokyo, Osaka | No |
| Korea Standard Time | KST | UTC+9 | Seoul | No |
| Australian Eastern | AEST | UTC+10 / UTC+11 | Sydney, Melbourne | Yes (AEDT) |
| New Zealand | NZST | UTC+12 / UTC+13 | Auckland, Wellington | Yes (NZDT) |

### Middle East and Africa

| Timezone | Abbreviation | UTC Offset | Major Markets | DST? |
|---|---|---|---|---|
| Israel Time | IST | UTC+2 / UTC+3 | Tel Aviv | Yes |
| South Africa Time | SAST | UTC+2 | Johannesburg, Cape Town | No |
| East Africa Time | EAT | UTC+3 | Nairobi | No |
| Arabian Standard Time | AST | UTC+3 | Riyadh | No |

---

## Platform Default Timezones

| Platform | Default Timezone | Can Be Changed? | Notes |
|---|---|---|---|
| **Meta Ads** | Set at ad account creation | No (after creation) | Must match Business Manager timezone |
| **Google Ads** | Set at account creation | No | Uses local timezone of account country |
| **TikTok Ads** | Set at account creation | No | Typically UTC or local market |
| **LinkedIn Ads** | UTC | No | All reporting in UTC |
| **Google Analytics 4** | Set in property settings | Yes | Can be changed anytime |
| **Pinterest Ads** | Account timezone | No | Set at creation |

---

## Time Overlap Matrix (Business Hours)

For coordinating across markets. Business hours defined as 9:00 AM - 6:00 PM local.

### US East to Major Markets

| Your Time (ET) | London (GMT/BST) | Berlin (CET/CEST) | Dubai (GST) | India (IST) | Sydney (AEST/AEDT) | Tokyo (JST) |
|---|---|---|---|---|---|---|
| 8:00 AM | 1:00 PM | 2:00 PM | 5:00 PM | 6:30 PM | 11:00 PM* | 10:00 PM |
| 9:00 AM | 2:00 PM | 3:00 PM | 6:00 PM | 7:30 PM | 12:00 AM* | 11:00 PM |
| 12:00 PM | 5:00 PM | 6:00 PM | 9:00 PM | 10:30 PM | 3:00 AM* | 2:00 AM |
| 3:00 PM | 8:00 PM | 9:00 PM | 12:00 AM | 1:30 AM | 6:00 AM* | 5:00 AM |
| 6:00 PM | 11:00 PM | 12:00 AM | 3:00 AM | 4:30 AM | 9:00 AM* | 8:00 AM |

*Next day. Times approximate; vary during DST transitions.

### Overlap Windows (Standard Time)

| Market Pair | Overlap Hours | Best Meeting Window |
|---|---|---|
| US East + UK | 5 hours (9 AM - 2 PM ET) | 10:00 AM - 12:00 PM ET |
| US East + Central Europe | 4 hours (9 AM - 1 PM ET) | 10:00 AM - 12:00 PM ET |
| US West + UK | 2 hours (9 AM - 11 AM PT) | 9:00 AM - 10:00 AM PT |
| US East + India | 0.5 hours (8:00 AM - 8:30 AM ET) | 8:00 AM ET / 6:30 PM IST |
| US East + Australia | 0 hours (no direct overlap) | Early AM ET / Evening AEST |
| UK + India | 3.5 hours (9 AM - 12:30 PM GMT) | 10:00 AM - 12:00 PM GMT |
| UK + Australia | 1-2 hours (8 AM - 10 AM GMT) | 8:00 AM - 9:00 AM GMT |

---

## Campaign Scheduling Considerations

### Ad Scheduling / Dayparting

| Market | Peak Engagement Hours | Off-Peak Hours | Notes |
|---|---|---|---|
| US (B2C) | 10 AM - 9 PM local | 12 AM - 6 AM | Weekend evenings can be strong |
| US (B2B) | 8 AM - 6 PM local (weekdays) | Weekends, evenings | Tuesday-Thursday often strongest |
| UK (B2C) | 9 AM - 9 PM local | 12 AM - 7 AM | Sunday evening can be strong |
| Europe (B2B) | 9 AM - 5 PM local (weekdays) | Weekends | August = vacation season |
| Australia | 9 AM - 9 PM local | 12 AM - 6 AM | Similar to US pattern |
| Brazil | 10 AM - 10 PM local | 1 AM - 7 AM | Strong evening engagement |
| India | 10 AM - 11 PM local | 1 AM - 7 AM | Very long engagement window |

### Global Campaign Launch Timing

When launching campaigns across multiple markets simultaneously:

1. **Option A: Staggered Launch** -- Launch each market at 9:00 AM local time
   - Pro: Each market starts at optimal time
   - Con: Monitoring extends over many hours

2. **Option B: Simultaneous Launch** -- Launch all markets at a single UTC time
   - Pro: Simpler to monitor
   - Con: Some markets launch at off-peak hours

3. **Recommended Approach:** Staggered launch for always-on campaigns, simultaneous launch for time-sensitive promotions (sales, events).

---

## Reporting Timezone Alignment

### Single-Market Reporting
Report in the ad account timezone. No conversion needed.

### Multi-Market Reporting
1. Choose a single reporting timezone (typically ET or UTC)
2. Note that daily data splits may differ from platform to platform
3. "Yesterday" in ET is different from "yesterday" in AEST
4. For global rollups, use UTC to avoid ambiguity

### DST Transition Handling
- During spring/fall DST transitions, one day will have 23 or 25 hours
- This creates apparent dips or spikes in daily metrics -- note in reports
- Meta and Google handle this automatically in their reporting
- US DST: Second Sunday in March (spring forward), First Sunday in November (fall back)
- EU DST: Last Sunday in March (spring forward), Last Sunday in October (fall back)
- Australia DST: First Sunday in October (spring forward), First Sunday in April (fall back)

---

## Quick Conversion Tool

### UTC Offset Quick Reference

To convert any time to another timezone:
```
Target Time = Source Time + (Target UTC Offset - Source UTC Offset)
```

**Example:** 3:00 PM ET (UTC-5) to CET (UTC+1):
```
3:00 PM + (1 - (-5)) = 3:00 PM + 6 = 9:00 PM CET
```
