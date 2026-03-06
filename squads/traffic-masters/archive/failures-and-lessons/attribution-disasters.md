# Attribution Disasters — Lessons Learned

## Purpose
Document attribution failures and measurement mistakes.

## Disaster 1: Double Counting
- **What happened:** Revenue reported 2x actual — each platform took full credit
- **Cause:** No deduplication between Meta and Google attribution
- **Lesson:** Platform-reported conversions will always exceed actual total
- **Prevention:** Use independent attribution tool or blended metrics (MER)

## Disaster 2: Killing a Winner
- **What happened:** Paused YouTube awareness campaign; Google Search CPA rose 40%
- **Cause:** YouTube was driving branded search volume (halo effect)
- **Lesson:** Last-click attribution undervalues upper-funnel channels
- **Prevention:** Incrementality tests before cutting any channel

## Disaster 3: Broken Pixel Went Unnoticed
- **What happened:** Optimizing on bad data for 3 weeks; wasted $30K
- **Cause:** Site update broke purchase event; campaigns optimized on wrong signal
- **Lesson:** Regular tracking QA is non-negotiable
- **Prevention:** Automated event monitoring, weekly QA checks

## Disaster 4: View-Through Inflation
- **What happened:** Claimed 10x ROAS; actual was 2x when view-throughs excluded
- **Cause:** Reporting included 1-day view-through conversions as full credit
- **Lesson:** View-through conversions inflate numbers significantly
- **Prevention:** Report click-through and view-through separately

## Disaster 5: Wrong Conversion Window
- **What happened:** High-ticket B2B product showing 0 conversions
- **Cause:** 7-day attribution window; sales cycle was 30-60 days
- **Lesson:** Attribution window must match the buying cycle
- **Prevention:** Extend attribution windows for long sales cycles; use offline conversion imports

## Key Principles
1. No single attribution model is truth — use triangulation
2. Test incrementality before making channel decisions
3. Automate tracking QA to catch breaks early
4. Match attribution window to sales cycle length
5. Report with intellectual honesty about data limitations
