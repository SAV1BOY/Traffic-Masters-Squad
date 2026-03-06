# Swipe File Update Script — Automation Script

> Swipe file curation and update automation for maintaining a fresh library of creative inspiration.

---

## Purpose

Systematically curate, organize, and refresh the ad swipe file collection to provide ongoing creative inspiration, trend awareness, and competitive intelligence for the creative development process.

---

## Trigger / Schedule

- **Scheduled trigger:** Monthly (comprehensive update)
- **Supplementary:** Weekly quick additions during competitor monitoring
- **Event trigger:** New campaign planning, creative refresh needed, new platform onboarded
- **Duration:** 45-75 minutes per update cycle
- **Owner:** Swipe File Agent
- **Supporting Agents:** Intelligence Agent, Creative Strategist Agent

---

## Pre-Conditions

- [ ] Access to ad transparency tools (Meta Ad Library, Google Ads Transparency, TikTok Ad Library)
- [ ] Access to swipe file directory structure
- [ ] Previous swipe file inventory reviewed
- [ ] Current creative needs understood (upcoming campaigns, refresh requirements)
- [ ] Competitor list current

---

## Step-by-Step Workflow

### Step 1: Source Identification and Scanning (20 minutes)

```yaml
action: Scan primary sources for notable ad examples
sources:
  ad_libraries:
    - Meta Ad Library (facebook.com/ads/library)
    - Google Ads Transparency Center
    - TikTok Creative Center / Ad Library
    - LinkedIn Ad Library
  industry_resources:
    - Foreplay.co or similar ad inspiration tools
    - AdEspresso Ad Gallery
    - Moat / competitive intelligence tools
    - Industry newsletters and publications
  organic_discovery:
    - Ads served to team members' personal feeds
    - Screenshots shared by team or clients
    - Conference presentations and case studies
    - Social media marketing communities
  competitor_feeds:
    - Tier 1 competitor active ads
    - Adjacent industry advertisers
    - Best-in-class advertisers outside category

scanning_criteria:
  save_if:
    - Hook is notably effective or creative
    - Visual approach is distinctive or trending
    - Copy technique is worth studying
    - Format usage is innovative
    - Offer structure is compelling
    - Landing page experience is notable
    - Ad-to-landing-page message match is exemplary
  quantity_target: "15-25 new examples per monthly cycle"
```

### Step 2: Capture and Categorize (15 minutes)

```yaml
action: Save and organize selected examples
capture_method:
  - Screenshot the ad (full ad unit including copy)
  - Save the URL / link (if available)
  - Note the platform and date observed
  - Record any available performance indicators

categorization_taxonomy:
  by_platform:
    directories: "swipe/meta/, swipe/google/, swipe/tiktok/, swipe/youtube/, swipe/linkedin/"
  by_format:
    tags: "video, static, carousel, collection, stories, ugc, text"
  by_hook_type:
    tags: "question, statistic, story, bold-claim, contrast, testimonial, demo, problem"
  by_angle:
    tags: "pain, desire, proof, authority, urgency, curiosity, social-proof"
  by_funnel_stage:
    tags: "tofu, mofu, bofu, retention"
  by_industry:
    tags: "[relevant industry categories]"

file_naming: "[platform]-[format]-[hook]-[angle]-[YYYY-MM-DD].[ext]"
example: "meta-video-question-pain-2026-03-06.png"
```

### Step 3: Analysis and Annotation (15 minutes)

```yaml
action: Annotate selected examples with analysis notes
for_each_saved_example:
  document:
    source:
      advertiser: "[Brand/Company name]"
      platform: "[Platform]"
      date_captured: "[YYYY-MM-DD]"
      estimated_run_duration: "[If visible in ad library]"
    creative_analysis:
      hook: "What makes the opening effective?"
      visual: "What visual approach is used and why it works"
      copy: "Key copy techniques worth noting"
      cta: "CTA approach and placement"
      format: "Why this format works for this message"
    strategic_analysis:
      target_audience: "Who appears to be the intended audience?"
      funnel_stage: "What stage of the journey does this target?"
      differentiation: "What makes this ad stand out from competitors?"
    applicability:
      relevant_to: "[Which of our campaigns/clients could use this approach?]"
      adaptation_notes: "How would we adapt this for our context?"
      priority: "high | medium | low (based on relevance and timeliness)"
```

### Step 4: Trend Identification (10 minutes)

```yaml
action: Identify patterns and trends across the swipe file collection
analysis:
  format_trends:
    - Which formats are appearing most frequently?
    - Any new formats or platform features being adopted?
    - Shift in video length or style preferences?
  creative_trends:
    - Emerging visual styles (colors, typography, imagery)
    - Popular hook types this period
    - Copy length and style trends
    - UGC vs. polished production balance
  messaging_trends:
    - Common pain points being addressed
    - Popular offer structures
    - CTA evolution
    - Tone shifts (more casual, more direct, etc.)
  platform_trends:
    - Platform-specific creative best practices evolving
    - New ad formats or placements gaining traction
    - Algorithm-favored content types
output: Monthly trend summary with implications for our creative strategy
```

### Step 5: Curation and Cleanup (10 minutes)

```yaml
action: Maintain swipe file quality and freshness
cleanup:
  remove:
    - Examples older than 12 months (unless timeless/classic)
    - Duplicate or near-duplicate examples
    - Examples from brands that are no longer relevant
    - Low-quality captures (blurry screenshots, incomplete)
  reorganize:
    - Ensure all examples are in correct category directories
    - Verify tagging is accurate and complete
    - Check for miscategorized entries
  highlight:
    - Star/flag top 5 examples from this update cycle
    - Create "Editor's Picks" or "Must-See" section for the month
    - Note which examples directly inspired recent campaign creative

inventory_update:
  total_examples: "[Count]"
  new_this_month: "[Count]"
  removed_this_month: "[Count]"
  by_platform: "[Breakdown]"
  by_format: "[Breakdown]"
```

### Step 6: Distribution and Documentation (5 minutes)

```yaml
action: Share updates with relevant agents and team
distribution:
  creative_strategist:
    content: "Top examples, trend summary, adaptation recommendations"
    purpose: "Inspire upcoming creative briefs"
  copy_agent:
    content: "Notable copy examples, hook techniques, CTA approaches"
    purpose: "Inform ad copy creation"
  strategy_agent:
    content: "Competitive creative trends, market shifts"
    purpose: "Inform strategic decisions"
  team_wide:
    content: "Monthly 'Editor's Picks' highlights"
    purpose: "Keep the team inspired and aware of trends"

documentation:
  - Update swipe file inventory log
  - Add trend summary to intelligence registry
  - Note any direct applications to current campaigns
  - Schedule next update cycle
```

---

## Decision Points

| Condition | Action |
|-----------|--------|
| Swipe file has < 50 relevant examples | Prioritize aggressive sourcing |
| Major creative trend identified | Fast-track to Creative Strategist for testing |
| Competitor creative outperforming ours | Deep analysis and adaptation brief |
| Swipe file > 500 examples | Aggressive cleanup, archive older entries |
| New platform added to media mix | Create dedicated swipe file section, source examples |

---

## Output / Deliverables

- Updated swipe file with 15-25 new examples
- Annotated analysis for each new entry
- Monthly trend summary
- Editor's Picks highlights
- Updated inventory log
- Distribution to relevant agents

---

## Post-Conditions

- [ ] Swipe file refreshed with new examples
- [ ] All entries categorized, tagged, and annotated
- [ ] Outdated entries removed or archived
- [ ] Trend summary compiled
- [ ] Highlights distributed to creative team
- [ ] Inventory log updated
- [ ] Next update cycle scheduled
