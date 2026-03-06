# The Broad Targeting Revolution

## Overview

Between 2019 and 2024, paid media buying underwent a fundamental shift: detailed audience targeting, long considered the primary skill of a media buyer, became less effective than giving algorithms maximum freedom to find converters. Broad targeting, the practice of setting minimal demographic constraints and letting machine learning determine who sees your ads, went from heresy to best practice.

---

## The Old Paradigm: Precision Targeting

### How Media Buyers Operated (2013-2019)
1. Research and build detailed audience personas
2. Translate personas into platform targeting (interests, behaviors, demographics, lookalikes)
3. Create separate ad sets for each audience segment
4. Test audiences against each other
5. Scale winning audiences, kill losers
6. Layer exclusions to prevent overlap
7. Manually manage frequency across segments

### Why Precision Targeting Made Sense
- Ad platforms had limited machine learning capability
- Algorithms needed human guidance to find the right audience
- Data was abundant (pre-iOS 14.5, pre-cookie restrictions)
- Smaller data sets per audience meant manual segmentation helped the algorithm
- The media buyer's targeting skill was a genuine competitive advantage

---

## The Shift to Broad

### Key Catalysts

**1. Platform Machine Learning Maturity (2018-2020)**
Meta and Google's algorithms became sophisticated enough to identify converters from broad audiences. With sufficient conversion data (50+ per week per ad set), the algorithms consistently outperformed human audience selection.

**2. iOS 14.5 Signal Loss (2021)**
When Apple restricted cross-app tracking:
- Detailed audience segments shrank (less data to build audiences from)
- Lookalike quality degraded (smaller, less precise seed audiences)
- The algorithm had to work with less granular signals
- Broader targeting gave the algorithm more options to find available signals
- Narrow audiences became even narrower, limiting optimization potential

**3. Empirical Evidence (2019-2022)**
Media buyers across the industry reported and documented that:
- Broad campaigns (age + gender + country only) frequently matched or beat targeted campaigns
- Additional targeting restrictions were reducing the algorithm's ability to optimize
- Audience overlap across detailed targeting segments was often 60-80%
- The algorithm was already finding the "right" people within broad pools

**4. Platform Incentive Alignment**
Broad targeting serves platform interests:
- More competition in auctions (all advertisers compete for the same inventory)
- Higher fill rates across inventory
- Less need for granular audience products (simpler platform)
- Faster campaign setup and lower barrier to entry

---

## How Broad Targeting Works

### The Algorithmic Mechanism
When you give a platform a broad audience, conversion goal, and creative:
1. The algorithm serves ads to a small initial sample across the broad audience
2. It observes who engages, clicks, and converts
3. It builds a real-time model of the "ideal converter" based on observed patterns
4. It progressively targets users who match the converter profile
5. As more conversions occur, the model refines continuously
6. The targeting is happening; it is just being done by the algorithm instead of the media buyer

### What Broad Targeting Is NOT
- **Not "no targeting":** The algorithm is targeting aggressively; you just cannot see the targeting criteria
- **Not random:** The algorithm uses thousands of signals (browsing behavior, purchase history, content interaction, device signals) that are far more granular than any interest or behavior category you could select
- **Not abdication of control:** The media buyer controls creative, budget, conversion goals, and bid strategy, all of which shape who the algorithm targets

---

## When Broad Targeting Works Best

| Condition | Why It Helps |
|---|---|
| Sufficient conversion volume (50+/week/ad set) | Algorithm has enough signal to learn |
| Clear conversion event | Algorithm knows what to optimize for |
| Differentiated creative | Creative self-selects the audience |
| Large potential audience | Broad pool gives algorithm room to optimize |
| E-commerce / DTC | Purchase events are clean, abundant signals |
| Multiple creative variants | Different creative reaches different segments within the broad audience |

## When Broad Targeting Underperforms

| Condition | Why It Struggles |
|---|---|
| Very low conversion volume (<10/week) | Insufficient data for algorithm learning |
| Hyper-niche B2B | Target audience too small for broad to find efficiently |
| Geographic restrictions needed | Local businesses cannot target nationally |
| Specific demographic requirements | Age-restricted products, gender-specific items |
| New accounts with no pixel data | Algorithm has no conversion history to learn from |

---

## Implementation Guide

### Step 1: Set the Foundation
- Ensure conversion tracking is accurate and complete (pixel + CAPI/enhanced conversions)
- Verify 50+ conversions per week at the ad set level (or optimize for a higher-volume event)
- Simplify account structure (fewer campaigns, fewer ad sets, larger budgets per ad set)

### Step 2: Test Broad Against Targeted
Run a controlled test:
- Campaign A: Current targeting approach (interests, lookalikes, etc.)
- Campaign B: Broad targeting (country + age range + gender only)
- Same creative, same budget, same optimization goal
- Run for 2-3 weeks minimum (allow learning phase to complete)
- Compare CPA, ROAS, and total conversion volume

### Step 3: Transition Gradually
If broad matches or beats targeted:
- Shift 50% of prospecting budget to broad targeting
- Maintain targeted campaigns at reduced budget as a hedge
- After 4 weeks, if broad continues to perform, shift remaining prospecting to broad
- Keep retargeting as a separate strategy (retargeting is not the same as prospecting targeting)

### Step 4: Invest in Creative Diversity
With broad targeting, creative becomes the primary targeting mechanism:
- Create different creative angles for different audience segments
- The algorithm will naturally show each creative to the audience most responsive to it
- A "new parent" ad shown to a broad audience will be shown predominantly to new parents
- A "fitness enthusiast" ad will find fitness enthusiasts
- This is creative-as-targeting in practice

---

## Impact on the Media Buyer Role

### Skills That Decreased in Value
- Manual audience research and selection
- Audience segment A/B testing
- Lookalike audience creation and management
- Interest-based targeting refinement
- Audience overlap management

### Skills That Increased in Value
- Creative strategy and ideation
- Creative testing methodology
- Data analysis and interpretation
- Conversion tracking and data quality
- Business strategy and unit economics
- Communication and storytelling (to explain the shift to stakeholders)

### The New Media Buyer Skill Stack
1. **Creative strategist:** Developing and testing creative concepts that speak to different audiences
2. **Data architect:** Ensuring conversion data is complete, accurate, and well-structured
3. **Business analyst:** Understanding unit economics, LTV, and incrementality
4. **Platform operator:** Managing campaign structure, budgets, and bid strategies
5. **Measurement expert:** Implementing and interpreting multi-source measurement

---

## Common Objections and Responses

**"Broad targeting wastes budget on irrelevant users."**
The algorithm eliminates irrelevant users faster than you can. Within hours, the algorithm has identified converter profiles and is not showing ads to non-prospects. The "waste" in broad targeting is less than the "waste" in narrow targeting hitting the wrong detailed audience.

**"I know my audience better than the algorithm."**
You know who your customers are. The algorithm knows who your next customers are. Your knowledge of customer demographics does not mean those demographics are the most efficient targeting criteria. The algorithm uses signals you cannot access.

**"Our product is too niche for broad targeting."**
Test it. Many "niche" products have found broad targeting effective because the algorithm discovers adjacent audiences the media buyer would never have considered. If it truly does not work for your product, the test will show that clearly.

**"My client expects to see audience targeting in the account."**
This is a communication challenge, not a strategic one. Explain that the targeting is happening algorithmically, show the creative-as-targeting strategy, and let results speak.

---

## Measurement Considerations

### How to Evaluate Broad Targeting Performance
- Compare total account performance (not just broad campaigns in isolation)
- Track new customer acquisition rate (is broad finding genuinely new customers?)
- Monitor geographic distribution (is spend going to valuable markets?)
- Check frequency metrics (broad should have lower frequency than narrow targeting)
- Evaluate creative-level performance within broad campaigns (which creative is reaching which audience?)

---

*Last updated: 2026-03-06*
*Category: Industry Shifts | Tags: broad targeting, algorithm, machine learning, Meta Ads, audience targeting*
