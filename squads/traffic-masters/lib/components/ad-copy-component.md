# Ad Copy Component

## Purpose
Standardized structure for ad copy across platforms.

## Copy Structure by Platform

### Meta (Facebook/Instagram)
- **Primary Text:** 1-3 paragraphs (125 char visible, 500+ expanded)
- **Headline:** Up to 40 characters (27 visible)
- **Description:** Up to 30 characters
- **CTA Button:** Predefined options (Learn More, Shop Now, etc.)

### Google Search (RSA)
- **Headlines:** Up to 15, 30 characters each
- **Descriptions:** Up to 4, 90 characters each
- **Display URL Path:** 2 paths, 15 chars each

### TikTok
- **Ad Text:** Up to 100 characters
- **Display Name:** Brand or creator name
- **CTA:** Predefined options

### LinkedIn
- **Introductory Text:** Up to 600 characters
- **Headline:** Up to 200 characters
- **Description:** Up to 300 characters

## Copy Formulas
1. **PAS:** Pain > Agitate > Solution
2. **AIDA:** Attention > Interest > Desire > Action
3. **BAB:** Before > After > Bridge
4. **4P:** Promise > Picture > Proof > Push
5. **SSS:** Star > Story > Solution

## Component Fields
- `copy_id`: Identifier
- `platform`: Target platform
- `formula`: Copy framework used
- `hook`: Opening line
- `body`: Main copy
- `cta`: Call to action
- `character_counts`: Validation against limits
- `compliance_check`: Policy-safe status
