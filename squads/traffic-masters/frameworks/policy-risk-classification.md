# Policy Risk Classification

> **Type**: Internal
> **Domain**: Compliance — Ad Policy and Risk Management
> **Used by agents**: Ad Midas, Media Buyer, Traffic Chief, Ads Analyst, Creative Analyst

## Overview

A traffic-light classification system for assessing policy risk in ad creative, landing pages, and targeting. Every piece of creative and every claim passes through this filter before production. Platform ad policies are the single biggest existential threat to paid media operations — an account ban can eliminate months of optimization data overnight.

## When to Use

- Creative concept approval before production begins
- Landing page copy review before campaign launch
- New client onboarding — assess offer risk level
- Ad rejection troubleshooting
- Quarterly compliance audit of all active campaigns

## The Framework

### Risk Levels

#### Green — Safe
Low risk of ad rejection or account issues. Standard advertising claims.

**Characteristics**:
- Factual product descriptions
- General benefit statements without specific outcome claims
- Lifestyle imagery without before/after implications
- Testimonials with proper disclaimers
- Educational content
- Standard ecommerce product advertising

**Examples**: "Premium quality materials", "Free shipping on orders over $50", "Trusted by thousands of customers"

#### Yellow — Caution
Moderate risk. May trigger ad review, require additional documentation, or face inconsistent enforcement across reviewers.

**Characteristics**:
- Implied results (before/after visual suggestions)
- Income or financial improvement language
- Weight loss or body transformation references
- Competitive comparison claims
- Urgency/scarcity tactics (false urgency flagged)
- Personal attributes targeting (age, health, financial status)
- Supplement or wellness claims
- Dating or relationship improvement
- Real estate investment messaging

**Required Actions**:
- Second review by Ads Analyst before submission
- Soften language — use "may", "can help", "designed to"
- Add disclaimers where applicable
- Prepare appeal documentation in advance
- Have backup creative versions ready

**Examples**: "Customers report feeling more energized", "Our system is designed to help you save", "Results may vary — see testimonials"

#### Red — High Risk
High probability of ad rejection, account restriction, or ban. Requires Traffic Chief approval and legal review.

**Characteristics**:
- Direct health claims or cure/treatment language
- Guaranteed financial returns or income claims
- Before/after imagery (especially health/body)
- Multilevel marketing or "get rich" messaging
- Political content or social issues
- Alcohol, cannabis, or regulated substances
- Cryptocurrency or speculative investment
- Weapons, adult content, or restricted categories
- Personal data collection beyond platform norms
- Clickbait or misleading landing page disconnects

**Required Actions**:
- Traffic Chief must approve before any production begins
- Legal/compliance review if available
- Platform-specific policy documentation review
- Consider alternative messaging that achieves same goal at Yellow or Green level
- Backup account and creative strategy documented

**Examples**: "Lose 20 pounds in 30 days", "Guaranteed $10K/month", "This cures...", "Doctors hate this trick"

### Platform-Specific Variations

| Risk Area | Meta | Google | YouTube | TikTok |
|-----------|------|--------|---------|--------|
| Health claims | Strict — personal attributes policy | Strict — healthcare cert required | Same as Google | Very strict |
| Financial claims | Strict — requires disclaimers | Requires certification for some categories | Same as Google | Strict |
| Before/after | Restricted — implied only, no direct | Less strict visually, copy still restricted | Same as Google | Strict |
| Supplements | Yellow — requires careful copy | Varies by country/cert | Same as Google | Often rejected |
| Crypto | Requires certification | Requires certification | Same as Google | Largely prohibited |
| Political | Requires authorization | Requires verification | Same as Google | Prohibited |
| Alcohol | Age-gated, geo-restricted | Restricted in many geos | Restricted | Prohibited |
| UGC-style claims | Monitor — platform cracking down on fake UGC | Less scrutinized | Moderate | High scrutiny |

### Review Process

1. **Creative Concept Phase**: Classify risk level using matrix above.
2. **Green**: Proceed to production. Standard QA.
3. **Yellow**: Ads Analyst reviews copy and visuals. Softened language approved. Backup version created. Proceed with caution.
4. **Red**: Traffic Chief approval required. Legal review if available. Alternative Green/Yellow version must be created alongside. Appeal strategy documented before submission.
5. **Post-Launch**: Monitor for rejections within first 24 hours. If rejected, do not resubmit same creative — modify and resubmit or appeal with documentation.

## Key Concepts

- **Policy Drift**: Platforms update policies frequently and enforcement is inconsistent. What was approved last month may be rejected today. Stay current.
- **Account Health Score**: Meta and Google track account-level policy compliance. Repeated Yellow/Red violations degrade overall account health even if individual ads are approved.
- **The Backup Rule**: For every Yellow or Red creative, a Green alternative must exist and be ready to deploy within 24 hours.
- **Appeal Strategy**: Document the policy you believe the ad complies with. Reference specific policy sections. Be factual, not emotional.

## Decision Rules

1. No Red-classified creative enters production without Traffic Chief written approval.
2. Yellow creative must have softened backup version ready before launch.
3. If an account receives 3+ rejections in one week, halt all new submissions and audit.
4. New clients in health, finance, or supplements start with Green creative only for first 30 days.
5. Never argue with a platform reviewer in real-time. Document, modify, appeal formally.
6. Quarterly policy review meeting — all agents review latest platform policy updates.

## Common Mistakes

- Assuming what worked on one platform is safe on another.
- Not reading the actual rejection reason and guessing at the fix.
- Resubmitting rejected creative with minimal changes — triggers repeat flagging.
- Ignoring landing page policy compliance — ads approved but LP triggers account review.
- Using aggressive copy in retargeting that would never pass in prospecting review.
- Not maintaining an appeal documentation library for common rejection types.

## Integration

- Creative concepts from `creative-angle-matrix.md` pass through risk classification before production.
- Hooks in `hook-library-system.md` tagged with risk level.
- Production pipeline in `creative-production-pipeline.md` includes QA step for policy review.
- UGC content in `ugc-creator-framework.md` — creator guidelines include policy constraints.
- Governance oversight in `governance-layer.md` includes compliance audits.

## Output

- Risk classification stamp on every creative brief (Green / Yellow / Red).
- Policy compliance checklist per platform per client.
- Rejection log with reasons, actions taken, and outcomes.
- Quarterly compliance audit report.
- Appeal documentation library organized by rejection type and platform.
