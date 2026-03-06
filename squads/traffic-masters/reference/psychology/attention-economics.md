# Attention Economics and Ad Viewability

> How the economics of human attention shape ad strategy, creative decisions, and media buying.

---

## 1. The Attention Economy

Attention is the scarcest resource in advertising. Supply is fixed (humans have limited attention), while demand grows (more ads, more platforms, more content).

### Key Statistics
- Average person sees 4,000-10,000 ads per day
- Only 3-5% of ads are consciously noticed
- Average mobile session: 70 seconds before switching
- Video completion rates average 15-25% for in-feed ads
- Banner blindness affects 86% of display ad impressions
- Cost of attention has increased 7-9x in the last two decades

### The Attention Supply Chain

```
Impression (ad served) -> Viewable (screen visible) -> Seen (eyes on ad) ->
Noticed (conscious awareness) -> Attended (processed) -> Remembered (encoded)
```

At each stage, significant attention drops off. Only 5-15% of impressions result in conscious processing.

---

## 2. Viewability Standards

### Industry Definitions (MRC/IAB)

| Format | Viewability Threshold |
|--------|----------------------|
| Display (standard) | 50% of pixels visible for 1+ seconds |
| Display (large: >242,500 px) | 30% of pixels visible for 1+ seconds |
| Video | 50% of pixels visible for 2+ continuous seconds |
| Mobile display | 50% of pixels visible for 1+ seconds |
| Mobile video | 50% of pixels visible for 2+ continuous seconds |

### Platform Viewability Benchmarks

| Platform | Average Viewability Rate |
|----------|------------------------|
| Google Display Network | 50-60% |
| YouTube (in-stream) | 90-95% |
| Facebook/Instagram Feed | 70-80% |
| Programmatic Display | 40-55% |
| Native Advertising | 60-70% |
| Connected TV | 95%+ |

### Beyond Viewability: Attention Metrics

Viewability only measures whether an ad COULD be seen, not whether it WAS seen.

| Metric | What It Measures | How Measured |
|--------|-----------------|--------------|
| **Viewability** | Ad visible on screen | Pixel tracking, intersection observer |
| **Attention time** | How long eyes are on the ad | Eye tracking, probabilistic models |
| **Attention quality** | Depth of cognitive processing | Brain imaging (fMRI), recall tests |
| **Active attention** | User actively looking at ad | Eye tracking |
| **Passive attention** | Ad in peripheral vision | Eye tracking |

---

## 3. Attention-Based Media Buying

### The Attention CPM (aCPM) Framework

Instead of optimizing for CPM (cost per 1,000 impressions), optimize for aCPM (cost per 1,000 attentive seconds).

```
aCPM = CPM / Average Attention Seconds

Example:
Platform A: CPM $10, Average 2 seconds attention -> aCPM = $5 per attentive second
Platform B: CPM $25, Average 10 seconds attention -> aCPM = $2.50 per attentive second

Platform B is more cost-effective despite higher CPM.
```

### Attention by Placement

| Placement | Avg. Attention (seconds) | CPM Range | aCPM |
|-----------|-------------------------|-----------|------|
| YouTube pre-roll (non-skip) | 10-15s | $15-30 | $1-3 |
| YouTube pre-roll (skippable) | 5-8s | $8-15 | $1-3 |
| Instagram Stories | 3-5s | $6-12 | $1.5-4 |
| Facebook Feed (video) | 2-4s | $8-15 | $2-7.5 |
| Facebook Feed (image) | 1-2s | $5-10 | $2.5-10 |
| TikTok In-Feed | 3-6s | $5-10 | $0.8-3.3 |
| Programmatic Display | 0.5-1.5s | $2-5 | $1.3-10 |
| Connected TV | 12-25s | $25-50 | $1-4 |

### Attention Vendors

Companies measuring real attention (not just viewability):
- **Lumen Research**: Eye-tracking panel data
- **Adelaide**: Attention-based media quality scoring (AU metric)
- **Playground XYZ**: Attention measurement platform
- **Amplified Intelligence**: Cross-platform attention data

---

## 4. Designing for Attention

### Attention Hierarchy in Ad Creative

**Level 1: Pre-Attentive Processing (0-200ms)**
- Color, contrast, and motion detected by peripheral vision
- Design elements: High contrast, bold colors, movement
- This determines whether the eye moves to your ad at all

**Level 2: Focal Attention (200ms-2s)**
- Eyes fixate on the ad; brain determines relevance
- Key elements: Face, headline, brand logo
- This determines whether the viewer stops scrolling

**Level 3: Sustained Attention (2-15s)**
- Viewer actively processes the message
- Elements: Body copy, product details, social proof
- This determines whether the message is understood

**Level 4: Deep Processing (15s+)**
- Viewer engages with content, clicks, or takes action
- Elements: Story, demonstration, emotional connection
- This determines whether the ad drives action

### Designing for Each Level

| Level | Design Priority |
|-------|----------------|
| Pre-attentive | High contrast, movement, faces, unexpected elements |
| Focal | Clear headline, brand identification, relevance signal |
| Sustained | Value proposition, benefit, proof points |
| Deep | Story, demonstration, CTA, emotional payoff |

---

## 5. Attention and Ad Format Selection

### Format Attention Comparison

| Format | Attention Capture | Attention Duration | Message Depth |
|--------|------------------|-------------------|---------------|
| Static image | Medium | Low (1-2s) | Low |
| Carousel | Medium-High | Medium (5-15s) | Medium |
| Short video (15s) | High | Medium (5-10s) | Medium |
| Long video (60s+) | High | High (15-30s) | High |
| Stories/Reels | High | Medium (3-8s) | Medium |
| Interactive | Very High | Very High | High |
| Audio (podcast) | Medium | Very High (30-60s) | Very High |
| Connected TV | High | Very High (15-30s) | High |

### Format Selection Guide

| Goal | Best Format | Why |
|------|-------------|-----|
| Brand awareness | Video (15-30s), CTV | High attention, memorable |
| Product consideration | Carousel, long video | Multiple messages, detail |
| Direct response | Static image, short video | Quick message, clear CTA |
| Retargeting | Static image, short video | Familiar audience, reminder |
| Complex product education | Long video, interactive | Sustained attention needed |

---

## 6. Attention Across the Customer Journey

### Attention Budget by Funnel Stage

| Stage | Attention Available | Strategy |
|-------|-------------------|----------|
| **Awareness** | 1-3 seconds | Pattern interrupt; single memorable message; brand imprint |
| **Consideration** | 5-15 seconds | Value proposition; key differentiators; proof |
| **Decision** | 15-60+ seconds | Detailed comparison; testimonials; objection handling |
| **Retention** | 2-5 seconds | Reminder; reward; new value |

### Matching Message to Attention Budget

**1-3 seconds (awareness)**: One benefit, one visual, brand name
- "Save 50% on cloud hosting" + logo + image

**5-15 seconds (consideration)**: Three benefits, proof point, CTA
- Problem statement -> Solution -> Proof -> CTA

**15-60 seconds (decision)**: Full story, multiple proof points, detailed offer
- Hook -> Problem -> Solution -> Demo -> Testimonial -> Offer -> CTA

---

## 7. Attention Optimization Tactics

### Reducing Attention Waste

| Tactic | Impact |
|--------|--------|
| Front-load key message (first 3 seconds) | +30-50% message recall |
| Use captions on video | +25% watch time (sound-off viewers) |
| Remove unnecessary elements | +10-15% focus on key message |
| Use visual hierarchy (size, contrast) | +20% eye tracking on CTA |
| Place brand early in video | +2x brand recall vs. end-only placement |
| Use faces (especially eyes) | +10-30% attention capture |

### Attention vs. Frequency

The relationship between exposure frequency and attention:

| Exposure # | Attention Level | Action |
|-----------|----------------|--------|
| 1st | High (novelty) | Awareness building |
| 2nd-3rd | Medium-high (recognition) | Message reinforcement |
| 4th-6th | Medium (familiarity) | Peak conversion window |
| 7th-10th | Low (habituation) | Rotate creative |
| 10th+ | Very low (fatigue/irritation) | Negative brand impact |

**Optimal frequency**: 3-7 exposures per user per week for most direct response campaigns. Above 10, attention crashes and negative sentiment rises.

---

## 8. Measuring Attention ROI

### Attention-Adjusted Metrics

| Standard Metric | Attention-Adjusted Version |
|----------------|--------------------------|
| CPM | aCPM (cost per 1,000 attentive seconds) |
| Impressions | Attentive impressions (viewable + actively noticed) |
| Reach | Attentive reach (people who actually saw the ad) |
| Frequency | Effective frequency (exposures with meaningful attention) |
| ROAS | Attention-adjusted ROAS (accounting for attention quality) |

### Proxy Metrics When Eye-Tracking Is Unavailable

| Proxy Metric | What It Approximates |
|-------------|---------------------|
| Video view rate (3s+) | Scroll-stop / initial attention |
| ThruPlay rate (15s+) | Sustained attention |
| Average watch time | Attention duration |
| Engagement rate | Active attention |
| Scroll depth (landing page) | On-page attention |
| Time on site | Post-click attention |

---

*Last updated: March 2026. Attention economics is emerging as the most important framework for media planning. As traditional metrics (impressions, CPM) become less meaningful in a privacy-first world, attention-based metrics offer a more accurate picture of advertising effectiveness.*
