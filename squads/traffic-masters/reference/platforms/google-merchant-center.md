# Google Merchant Center
> **Platform**: Google Merchant Center + Shopping Ads
> **Last Updated**: 2026-03

## Overview
Google Merchant Center manages product data feeds for Shopping ads, free listings, and Performance Max product campaigns.

## Product Feed Requirements
- **Required fields**: id, title, description, link, image_link, price, availability, brand, gtin/mpn, condition
- **Recommended fields**: sale_price, product_type, google_product_category, custom_labels, shipping, tax
- **Title**: Max 150 chars. Include brand, product type, key attributes (color, size)
- **Description**: Max 5,000 chars. Natural language, relevant keywords

## Feed Formats
- XML (recommended), TXT (tab-delimited), Google Sheets, Content API

## Shopping Campaign Types
- Standard Shopping: manual bidding, product group targeting
- Performance Max: AI-driven, all Google surfaces (Search, Shopping, Display, YouTube, Gmail, Discover)
- Free Listings: organic product visibility in Shopping tab

## Custom Labels
- custom_label_0 through custom_label_4 for segmentation
- Common uses: margin tier, bestseller flag, seasonal, price range, new arrival

## Key Best Practices
- Optimize product titles with search-relevant terms
- High-quality images with white background (primary), lifestyle (additional)
- Keep feed updated daily for price and availability accuracy
- Use custom labels to segment products by business priority
- Monitor disapprovals daily and fix immediately
- Supplemental feeds for bulk attribute updates without touching primary feed
- GTIN/EAN required for most products — missing GTINs reduce visibility
