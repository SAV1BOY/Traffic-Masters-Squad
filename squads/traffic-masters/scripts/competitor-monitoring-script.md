# Competitor Monitoring Script — Automation Script

> Competitor ad monitoring automation for tracking competitive activity and identifying opportunities.

---

## Purpose

Systematically monitor competitor advertising activity across platforms to identify strategic threats, creative inspiration, messaging trends, and opportunities for differentiation.

---

## Trigger / Schedule

- **Scheduled trigger:** Monthly (comprehensive review)
- **Supplementary:** Weekly quick scan during optimization routine
- **Event trigger:** New competitor entry, competitor campaign surge, market shift
- **Duration:** 45-90 minutes per competitive set
- **Owner:** Intelligence Agent
- **Supporting Agents:** Creative Strategist Agent, Strategy Agent

---

## Pre-Conditions

- [ ] Competitor list defined and prioritized (Tier 1: direct, Tier 2: adjacent)
- [ ] Access to ad transparency tools (Meta Ad Library, Google Ads Transparency Center, TikTok Ad Library)
- [ ] Previous competitive analysis available for comparison
- [ ] Swipe file directory accessible for saving examples

---

## Step-by-Step Workflow

### Step 1: Ad Library Scan (20 minutes)

```yaml
action: Review competitor ads across platform ad libraries
platforms:
  meta_ad_library:
    url: "facebook.com/ads/library"
    for_each_competitor:
      - Search by page name / advertiser name
      - Filter by country, platform, media type
      - Note: active ads count, date range, formats used
  google_ads_transparency:
    url: "adstransparency.google.com"
    for_each_competitor:
      - Search by advertiser name
      - Review search, display, and video ads
      - Note: volume, recency, format distribution
  tiktok_ad_library:
    url: "library.tiktok.com"
    for_each_competitor:
      - Search by advertiser name
      - Review video ads and engagement metrics
      - Note: creative approaches and trends
data_to_capture:
  per_competitor:
    - Total number of active ads
    - Platforms being used
    - Ad formats used (video, static, carousel, etc.)
    - Estimated spend level (low/medium/high based on volume)
    - Date range of activity (new vs. long-running)
```

### Step 2: Messaging Analysis (15 minutes)

```yaml
action: Analyze competitor messaging and positioning
for_each_competitor:
  analyze:
    hooks:
      - What types of hooks are they using? (question, statistic, story, etc.)
      - What pain points are they addressing?
      - What desires are they tapping into?
    value_propositions:
      - What is their primary claim?
      - How do they differentiate from alternatives?
      - What proof do they offer?
    offers:
      - What offers are they running? (discount, trial, demo, lead magnet)
      - How aggressive is their pricing/offer?
      - Are they running limited-time promotions?
    ctas:
      - What CTAs are they using?
      - What funnel stage do their ads target?
    tone:
      - Professional vs. casual
      - Feature-focused vs. benefit-focused
      - Brand-heavy vs. performance-focused
output: Messaging comparison matrix
```

### Step 3: Creative Analysis (15 minutes)

```yaml
action: Analyze competitor creative approaches
for_each_competitor:
  analyze:
    formats:
      - Video vs. static vs. carousel distribution
      - Video length and style (UGC, polished, demo, testimonial)
      - Static design approach (photography, illustration, text-heavy)
    visual_patterns:
      - Color schemes and branding prominence
      - Use of faces/people vs. product shots
      - Text overlay usage and density
    production_quality:
      - High production vs. authentic/raw
      - Branded vs. native/organic-looking
    volume_and_velocity:
      - How many new ads per month?
      - How quickly do they rotate creative?
      - What is their typical ad lifespan?
  save:
    - Screenshot or bookmark top examples for swipe file
    - Categorize by format, hook type, and angle
output: Creative trend report with saved examples
```

### Step 4: Opportunity Identification (10 minutes)

```yaml
action: Identify strategic opportunities based on competitive analysis
opportunities:
  messaging_gaps:
    - Pain points competitors are NOT addressing
    - Value propositions they are NOT making
    - Audiences they appear to NOT be targeting
  creative_opportunities:
    - Formats competitors are not using
    - Hook types that are underrepresented
    - Visual styles that would differentiate
  tactical_opportunities:
    - Platforms where competitors have low presence
    - Seasonal or event-based gaps
    - Offer structures competitors have not tried
  defensive_actions:
    - Messaging competitors are using that directly challenges our positioning
    - Claims competitors make that we need to counter
    - Market share threats that require response
output: Opportunity brief with prioritized recommendations
```

### Step 5: Trend Tracking (10 minutes)

```yaml
action: Compare current competitive landscape to previous analysis
track:
  changes:
    - New competitors entering the space
    - Competitors increasing/decreasing ad volume
    - Messaging pivots or new positioning
    - New ad formats or creative approaches
    - Offer changes (more/less aggressive)
  trends:
    - Industry-wide creative trends
    - Platform-specific trends
    - Seasonal patterns in competitive activity
    - Emerging competitor strategies
output: Trend comparison document (current vs. previous period)
```

### Step 6: Documentation and Distribution (10 minutes)

```yaml
action: Compile findings and share with relevant agents
outputs:
  competitive_analysis_report:
    - Competitor activity summary
    - Messaging comparison matrix
    - Creative trend report
    - Opportunity brief
    - Trend comparison
  swipe_file_updates:
    - Add notable competitor creative examples to swipe file
    - Tag by platform, format, hook, angle, competitor
  strategic_recommendations:
    - Share relevant findings with Strategy Agent
    - Brief Creative Strategist on creative trends
    - Alert on any urgent competitive threats
distribution:
  - Share report with Strategy Agent and Creative Strategist Agent
  - Update competitive section of the intelligence registry
  - Flag urgent items for immediate strategy discussion
```

---

## Decision Points

| Condition | Action |
|-----------|--------|
| New competitor with aggressive spend | Alert Strategy Agent, deep-dive analysis |
| Competitor using messaging that directly counters ours | Develop counter-positioning, test new messaging |
| Competitor creative significantly outperforming ours | Analyze approach, brief creative variations inspired by (not copied from) the approach |
| Competitor withdrawn from a platform/channel | Opportunity to capture share, increase presence |
| Industry-wide creative trend emerging | Test the trend before it saturates |

---

## Output / Deliverables

- Monthly competitive analysis report
- Messaging comparison matrix
- Creative trend report with swipe file additions
- Opportunity brief with prioritized recommendations
- Updated competitive intelligence registry

---

## Post-Conditions

- [ ] All Tier 1 competitors reviewed across active platforms
- [ ] Messaging and creative analysis completed
- [ ] Swipe file updated with notable examples
- [ ] Opportunities identified and prioritized
- [ ] Findings shared with Strategy and Creative Strategist agents
- [ ] Trends compared to previous period
- [ ] Next monitoring cycle scheduled
