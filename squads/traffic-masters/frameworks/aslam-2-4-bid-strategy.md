# 2-4 Bid Strategy Framework
> **Author**: Kasim Aslam / Google Ads Bidding
> **Domain**: Google Ads, Bid Management, Auction Strategy
> **Used by agents**: google-ads-agent, media-buyer-agent, optimization-agent

## Overview
A bid-setting methodology for Manual CPC: start at 2x Google's suggested CPC, go up
to 4x if needed to win auctions, then systematically reduce. The philosophy is win
the auction first, optimize cost second. Under-bidding means no data. No data means
no optimization. You cannot improve what you cannot measure.

## When to Use
- Setting initial Manual CPC bids for new campaigns or keywords
- When impressions or clicks are too low to generate meaningful data
- Re-entering competitive auctions after a pause
- When suggested bids are not producing sufficient impression share

## The Framework
### Step 1: Start at 2x Suggested CPC
- Google provides an estimated first-page CPC for each keyword
- Set your initial bid at 2x that estimate
- Purpose: Ensure you win enough auctions to gather data quickly
- Duration: Run for 3-5 days at this level
- Monitor: Impression share, click volume, average position

### Step 2: Evaluate at 2x
- IF impression share > 50% and clicks are flowing → stay at 2x
- IF impression share < 30% → move to Step 3
- IF CTR is healthy (>2% search) → bids are competitive enough
- Collect at least 100 clicks before making bid changes

### Step 3: Increase to 4x if Needed
- If 2x is not winning enough auctions, increase to 4x suggested CPC
- Purpose: Dominate the auction temporarily to gather maximum data
- Duration: Run for 3-5 days at this level
- This is a data-gathering investment, not the long-term bid

### Step 4: Reduce Systematically
- Once you have 200+ clicks and conversion data, begin reducing bids
- Reduce by 10-15% increments every 3-5 days
- Monitor: Does conversion volume hold as you reduce bids?
- Find the sweet spot: lowest CPC that maintains conversion volume
- Stop reducing when conversion volume starts to decline

### Step 5: Stabilize and Optimize
- Set bids at the optimized level from Step 4
- Adjust by keyword, ad group, device, time of day, location
- Use bid adjustments for high-performing segments
- Consider transition to automated bidding with this data (see Manual CPC First)

## Key Concepts
- Under-bidding is more expensive than over-bidding (opportunity cost of no data)
- The 2-4x range ensures you enter auctions competitively
- This is a temporary investment phase, not a permanent cost structure
- Data from high bids reveals which keywords and audiences actually convert
- Reducing bids with data is optimization; low bids without data is guessing

## Decision Rules
- IF no impressions at 2x → check keyword quality score and ad relevance first
- IF 4x still produces low impression share → the keyword may be too competitive
- IF CPC at 2x is already within target CPA → no need to go to 4x
- IF reducing bids causes volume to drop sharply → you hit the floor, go back up
- IF budget is very limited → apply 2-4x to top 5 keywords only

## Common Mistakes
- Bidding at suggested CPC and wondering why there is no traffic
- Going straight to 4x without trying 2x first
- Staying at 4x too long without beginning the reduction process
- Reducing too aggressively (>20% at once) and losing auction position
- Applying this to automated bidding campaigns (it is for Manual CPC only)

## Integration
- Feeds into: Aslam Manual CPC First (2-4x is the Phase 1 bid-setting method)
- Pairs with: Aslam 4 Core Campaign Types (apply per campaign type)
- Complements: Aslam You vs. Google (win auctions on your terms)
- Output flows to: Bid optimization data, automated bidding transition

## Output
- Initial bid recommendations at 2x suggested CPC per keyword
- Escalation plan to 4x with triggers and timeline
- Systematic reduction schedule with performance monitoring checkpoints
- Optimized bid levels based on actual conversion data
