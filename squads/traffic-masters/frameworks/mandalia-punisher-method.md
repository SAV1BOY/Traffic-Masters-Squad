# Punisher Method

> **Author**: Depesh Mandalia
> **Domain**: Campaign Optimization and Budget Reallocation
> **Used by agents**: media-buyer, performance-analyst, automation-engineer
> **Checklists**: daily-review-checklist, optimization-checklist

## Overview

The Punisher Method is Depesh Mandalia's ruthless optimization framework for cutting underperformers and reallocating budget to winners. It removes emotion from optimization decisions by establishing clear thresholds before launch and enforcing them without exception. The name reflects the mindset: underperformers are punished (cut), winners are rewarded (more budget). No mercy, no hope-based optimization.

## When to Use

- Daily campaign review and optimization routine
- When account performance is declining due to spend on underperformers
- After launching new campaigns that need rapid optimization
- When media buyers are holding onto losing ad sets for emotional reasons
- Establishing optimization SOPs for a team

## The Framework

### Step 1: Define Thresholds Before Launch
1. Set CPA threshold (maximum acceptable cost per acquisition)
2. Set ROAS threshold (minimum acceptable return on ad spend)
3. Set CTR floor (minimum click-through rate to indicate relevance)
4. Set spend threshold (minimum spend before making a judgment)
5. Document thresholds in the campaign brief — they are non-negotiable once set

### Step 2: Daily Review Process
1. Pull performance data for all active ad sets and ads
2. Filter by ad sets that have spent above the minimum spend threshold
3. Compare each ad set against the defined thresholds
4. Categorize each ad set:
   - **Winner**: Meeting or exceeding all thresholds
   - **Watch**: Mixed signals, within acceptable variance (1 threshold missed)
   - **Punish**: Below threshold on 2+ metrics for 3+ consecutive days

### Step 3: Punish Underperformers
1. Any ad set in "Punish" category for 3+ days gets cut immediately
2. Do not reduce budget — turn it off entirely
3. Do not "give it one more day" — the data has spoken
4. Record why it was cut for future learning (which threshold, by how much)
5. Exception: Day 1-2 of a new ad set is learning phase — do not punish yet

### Step 4: Reward Winners
1. Reallocate budget from punished ad sets to winners
2. Apply appropriate scaling recipe (V-Scale for proven winners)
3. Winners that sustain performance get progressively more budget
4. Track winner longevity — even winners eventually fatigue

### Step 5: Manage the Watch List
1. Ad sets on Watch get 48-72 more hours maximum
2. If they improve to Winner status, they stay
3. If they decline to Punish status, they are cut
4. Never let Watch list grow — it becomes a budget drain
5. Maximum 3 items on Watch at any time

### Daily Rhythm
- Morning: Pull data, categorize, execute decisions (30-45 minutes)
- Do not re-check and second-guess during the day
- Next morning: Review impact of yesterday's decisions, repeat

## Key Concepts

- **Pre-defined thresholds eliminate emotion**: You decided what "bad" means before you had skin in the game
- **3-day rule**: One bad day is noise. Three bad days is signal.
- **Learning phase protection**: Never punish an ad set in its first 48 hours
- **Budget reallocation is instant**: Money freed from losers goes to winners immediately
- **No hope-based optimization**: "Maybe it will turn around" is not a strategy
- **Cut fast, scale slow**: Be quick to punish, measured in rewarding

## Decision Rules

- IF CPA exceeds threshold by 50%+ on day 1 THEN watch closely but do not cut yet (learning phase)
- IF CPA exceeds threshold for 3 consecutive days THEN punish immediately
- IF ROAS is below threshold but CPA is acceptable THEN check AOV — the funnel may need work
- IF CTR drops below floor THEN creative fatigue — punish the ad, not necessarily the audience
- IF all ad sets in a campaign are punished THEN the campaign concept is flawed — revisit AC4
- IF a previously punished concept keeps appearing as a test THEN blacklist it permanently

## Common Mistakes

- Not setting thresholds before launch (leads to subjective, inconsistent decisions)
- Punishing on day 1 (algorithm is still in learning phase)
- Setting thresholds too tight (punishing everything, nothing survives)
- Setting thresholds too loose (keeping underperformers too long)
- Reducing budget instead of cutting (slow bleed instead of clean cut)
- Emotional attachment to creative you personally like
- Not reallocating freed budget to winners (the money just sits idle)
- Punishing during platform-wide issues (check for broader outages first)

## Integration

- Depends on: mandalia-graduation-testing (thresholds align with graduation criteria)
- Feeds into: mandalia-scaling-recipes (freed budget feeds winning scaling recipes)
- Connects to: mandalia-ac4 (punished concepts reveal which AC4 lever is weak)
- Connects to: mandalia-4-funnel-system (thresholds differ by funnel stage)

## Output

- Daily optimization log: what was punished, what was rewarded, budget reallocations
- Updated campaign performance dashboard showing active vs. punished ad sets
- Threshold documentation per campaign
- Weekly summary: total spend saved from punished underperformers, reinvestment results
