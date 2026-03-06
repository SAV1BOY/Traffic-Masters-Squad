# Build UTM Links — Script Guide

## Purpose
Generate properly formatted UTM-tagged URLs for campaign tracking.

## UTM Parameters

| Parameter | Description | Example |
|-----------|-------------|---------|
| utm_source | Traffic source platform | meta, google, tiktok |
| utm_medium | Marketing medium | paid-social, cpc, paid-video |
| utm_campaign | Campaign identifier | meta_conv_us_tofu_freetrial |
| utm_content | Creative identifier | cre-001, ugc-testimonial-v2 |
| utm_term | Keyword or audience | skincare-interest, lal1-purch |

## URL Builder Template
```
{base_url}?utm_source={source}&utm_medium={medium}&utm_campaign={campaign}&utm_content={content}&utm_term={term}
```

## Example
```
https://example.com/offer?utm_source=meta&utm_medium=paid-social&utm_campaign=meta_conv_us_tofu_freetrial_2026q1&utm_content=cre-001&utm_term=lal1-purchasers
```

## Rules
1. All values lowercase
2. Use hyphens for multi-word values (not spaces or underscores)
3. No special characters except hyphens
4. Keep values concise but descriptive
5. utm_source and utm_medium are mandatory
6. utm_campaign should match campaign naming convention

## Validation Checks
- [ ] Base URL is correct and working
- [ ] No duplicate parameters
- [ ] No spaces or special characters
- [ ] UTM values match naming conventions
- [ ] Link resolves to correct landing page
- [ ] Parameters visible in GA4 acquisition reports

## Tools
- Google Campaign URL Builder
- UTM.io for team management
- Custom spreadsheet with concatenation formulas
