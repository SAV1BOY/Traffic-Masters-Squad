# Manual CPC First Framework
> **Author**: Kasim Aslam / Google Ads Bidding Strategy
> **Domain**: Google Ads, Bid Management, Automation Readiness
> **Used by agents**: google-ads-agent, media-buyer-agent, optimization-agent

## Overview
A phased bidding strategy that starts with Manual CPC to gather conversion data before
transitioning to automated bidding. The core rule: never automate without data. Google's
automated bidding strategies (tCPA, tROAS, Maximize Conversions) need 30-50 conversions
to function properly. Starting automated is like asking GPS to navigate without a map.

## When to Use
- Launching any new Google Ads campaign
- Resetting bidding strategy after poor automated performance
- Entering a new market or targeting a new audience
- When automated bidding is producing erratic or expensive results

## The Framework
### Phase 1: Manual CPC (Weeks 1-4)
- Set bids manually for each keyword or ad group
- Goal: Gather 30-50 conversions with reliable tracking
- Start bids at estimated first-page CPC
- Adjust bids based on search term quality and conversion data
- Monitor: CTR, CPC, conversion rate, cost per conversion
- Duration: Until 30-50 conversions are recorded (minimum 2 weeks)

### Phase 2: Data Review (Week 4-5)
- Analyze conversion data: which keywords, audiences, times convert best
- Verify tracking accuracy: compare Google conversions to CRM data
- Calculate actual CPA and ROAS from real business data
- Determine target CPA or ROAS for automated bidding
- Decision: Is there enough quality data to automate?

### Phase 3: Automated Transition (Week 5+)
- Switch to tCPA or tROAS based on business model
- Set targets based on Phase 1 actual performance (not aspirational)
- Start with targets 10-20% higher than actual CPA (give algorithm room)
- Monitor closely for 2 weeks — do not make changes during learning phase
- If performance degrades after 2 weeks, revert to Manual CPC

## Key Concepts
- 30-50 conversions is the minimum data threshold for automation
- Never set aspirational targets — use real data from Phase 1
- The learning phase (first 2 weeks of automation) will be volatile
- Manual CPC is not inferior — it is the foundation for smart automation
- Some accounts perform best staying on Manual CPC permanently
- Enhanced CPC (eCPC) is a middle ground but still needs data

## Decision Rules
- IF conversions < 30 → stay on Manual CPC, do not automate
- IF conversion tracking is unreliable → fix tracking before automating
- IF tCPA is producing CPAs 2x above target after 2 weeks → revert
- IF account is low volume (<100 clicks/week) → consider staying manual
- IF business model is ROAS-driven → use tROAS; if lead-gen → use tCPA
- IF performance is stable on Manual CPC → do not fix what is not broken

## Common Mistakes
- Starting a new campaign on Maximize Conversions with zero data
- Setting tCPA targets based on wishes instead of actual Phase 1 data
- Making changes during the 2-week automated learning phase
- Switching from Manual to automated and back repeatedly (algorithm whiplash)
- Ignoring the data review phase and jumping straight to automation
- Using Maximize Clicks thinking it will lead to conversions

## Integration
- Feeds into: Aslam 2-4 Bid Strategy (Manual CPC bid-setting methodology)
- Pairs with: Aslam You vs. Google (resist Google's push to automate early)
- Complements: Aslam 4 Core Campaign Types (apply per campaign type)
- Source data: Tracking Stack Standard (conversion data accuracy)

## Output
- A phase-by-phase bidding transition plan with timelines
- Manual CPC bid recommendations per keyword or ad group
- Automation readiness checklist (data thresholds, tracking verification)
- Reversion protocol if automated bidding underperforms
