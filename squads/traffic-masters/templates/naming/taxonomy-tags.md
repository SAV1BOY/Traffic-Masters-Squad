# Taxonomy Tags

> **Type**: Template
> **Category**: naming
> **Used by tasks**: creative-tagging, performance-analysis, reporting
> **Filled by agents**: creative-strategist-agent, analytics-agent

## Purpose
Provides a standardized tagging system for categorizing creatives, campaigns, and content so that performance data can be sliced by angle, hook type, format, audience segment, funnel stage, and platform for meaningful analysis.

## Template

### Tag Categories

#### 1. Angle Tags
**Purpose**: Classify the persuasion approach used in the creative.
| Tag | Description | Example |
|---|---|---|
| `angle:pain` | Highlights a problem or frustration | "Tired of wasting money on ads that don't convert?" |
| `angle:desire` | Appeals to an aspiration or goal | "Imagine scaling to $100k/month" |
| `angle:objection` | Addresses a common hesitation | "Think it's too expensive? Here's the math" |
| `angle:proof` | Leads with evidence or results | "We generated 2,347 leads in 30 days" |
| `angle:curiosity` | Creates intrigue or open loops | "The one thing top brands do differently" |
| `angle:authority` | Leverages expertise or credentials | "As a 10-year media buyer, here's what I know" |
| `angle:urgency` | Creates time pressure | "Only 48 hours left at this price" |
| `angle:social-proof` | Uses others' actions as validation | "Join 10,000+ marketers who switched" |

#### 2. Hook Type Tags
**Purpose**: Classify the opening mechanism of the creative.
| Tag | Description |
|---|---|
| `hook:question` | Opens with a question |
| `hook:bold-claim` | Opens with a provocative statement |
| `hook:stat` | Opens with a data point or number |
| `hook:story` | Opens with a narrative or anecdote |
| `hook:visual-interrupt` | Opens with an unexpected visual |
| `hook:callout` | Opens by calling out the audience directly |
| `hook:contrarian` | Opens by challenging conventional wisdom |
| `hook:listicle` | Opens with a numbered list promise |

#### 3. Format Tags
**Purpose**: Classify the creative format.
| Tag | Description |
|---|---|
| `format:static-image` | Single image ad |
| `format:video-short` | Video under 30 seconds |
| `format:video-mid` | Video 30-60 seconds |
| `format:video-long` | Video over 60 seconds |
| `format:carousel` | Multi-card carousel |
| `format:ugc` | User-generated content style |
| `format:talking-head` | Presenter on camera |
| `format:screen-record` | Screen recording or walkthrough |
| `format:animation` | Motion graphics or animated |
| `format:advertorial` | Native editorial style |

#### 4. Audience Segment Tags
**Purpose**: Classify the target audience segment.
| Tag | Description |
|---|---|
| `audience:cold-broad` | Broad prospecting, no targeting |
| `audience:cold-interest` | Interest-based targeting |
| `audience:cold-lal` | Lookalike audience |
| `audience:warm-engager` | Social engagers or video viewers |
| `audience:warm-visitor` | Website visitors |
| `audience:hot-cart` | Cart abandoners |
| `audience:hot-lead` | Leads not yet converted |
| `audience:customer` | Existing customers |

#### 5. Funnel Stage Tags
**Purpose**: Classify where in the funnel the creative operates.
| Tag | Description |
|---|---|
| `funnel:tofu` | Top of funnel - awareness and discovery |
| `funnel:mofu` | Middle of funnel - consideration and evaluation |
| `funnel:bofu` | Bottom of funnel - decision and purchase |
| `funnel:retention` | Post-purchase retention or upsell |

#### 6. Platform Tags
**Purpose**: Classify the platform the creative is built for.
| Tag | Description |
|---|---|
| `platform:meta` | Meta (Facebook + Instagram) |
| `platform:google` | Google Ads |
| `platform:youtube` | YouTube |
| `platform:tiktok` | TikTok |
| `platform:linkedin` | LinkedIn |

### Tagging Rules
- Every creative must have at least one tag from each category.
- Multiple tags per category are allowed (e.g., `angle:pain` + `angle:proof`).
- Tags are lowercase with colon separator between category and value.
- Add tags at creative upload/launch time, not retroactively.

### Analysis Applications
- **Angle performance**: Compare CPA across angle tags to find what resonates.
- **Hook effectiveness**: Compare hook-rate and CTR by hook type.
- **Format ROI**: Identify which formats drive best ROAS per platform.
- **Audience-creative fit**: Cross-reference audience and angle tags.

## Usage Notes
- Maintain a tagging spreadsheet or use your ad management tool's label feature.
- Review and update the taxonomy quarterly as new patterns emerge.
- Train all team members on consistent tagging before creative launches.

## Example
A UGC video ad on Meta targeting cold lookalike audiences at TOFU using a pain angle with a question hook would be tagged: `angle:pain`, `hook:question`, `format:ugc`, `audience:cold-lal`, `funnel:tofu`, `platform:meta`.

## Related
- campaign-naming-standard.md
- creative-analysis-report.md
- creative-brief.md
