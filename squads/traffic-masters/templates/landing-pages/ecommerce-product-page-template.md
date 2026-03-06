# Ecommerce Product Page Template

> **Type**: Template
> **Category**: landing-pages
> **Used by tasks**: product-page-optimization, ecommerce-funnel, conversion-rate-optimization
> **Filled by agents**: copywriter-agent, funnel-builder-agent, cro-agent

## Purpose
Structures an ecommerce product page with all essential conversion elements, ensuring paid traffic landing on this page finds the information, proof, and urgency needed to add to cart and purchase.

## Template

### Page Metadata
**Product URL**: [slug]
**Product category**: [category]
**Traffic sources**: [Meta / Google Shopping / Google Search / TikTok / organic]
**Target conversion rate**: [add-to-cart rate and purchase rate]
**Mobile-first**: [yes - design for mobile first]

### Section 1: Product Images
**Hero image**: [Main product shot on clean background]
**Image 2**: [Product in use / lifestyle context]
**Image 3**: [Close-up detail / texture / quality indicator]
**Image 4**: [Scale reference / dimensions visualization]
**Image 5**: [Before/after or comparison if applicable]
**Image 6**: [Packaging or what arrives]
**Video**: [Product demo or UGC review, 15-30 seconds]
**Image specs**: Minimum 1000x1000, zoomable, consistent lighting
**Notes**: First image is most important; it appears in ads and search results.

### Section 2: Title and Price
**Product title**: "[Brand + Product Name + Key Differentiator, under 80 characters]"
**Price display**: [$XX.XX]
**Compare-at price**: [$XX.XX if on sale, with strikethrough]
**Savings display**: [Save $X or Save X%]
**Payment options**: [Afterpay / Klarna / installments available badge]
**Rating summary**: [X.X stars from X reviews - clickable to reviews section]
**Availability**: [In stock / Low stock / Ships in X days]

### Section 3: Description
**Short description**: "[2-3 sentences above the fold summarizing what the product does and who it's for]"
**Expanded description**: "[Longer copy below the fold with full story, usage instructions, and brand narrative]"
**Tone**: [Match brand voice - authoritative / playful / minimal / detailed]
**Notes**: Short description must sell; expanded description must inform.

### Section 4: Features and Benefits
**Format**: Two-column or icon-based grid
| Feature | Benefit |
|---|---|
| [Technical feature 1] | [What it means for the customer] |
| [Technical feature 2] | [What it means for the customer] |
| [Technical feature 3] | [What it means for the customer] |
| [Technical feature 4] | [What it means for the customer] |
**Ingredient / material list**: [if applicable]
**Certifications**: [organic, cruelty-free, FDA, ISO, etc.]
**Notes**: Always translate features into benefits. "What" it is matters less than "why" it matters.

### Section 5: Reviews
**Section headline**: "What our customers say"
**Review display**: [star rating + text + name + verified badge]
**Review count**: [total reviews shown]
**Sort options**: [most recent / highest rated / most helpful]
**Photo reviews**: [prioritize reviews with customer photos]
**Review highlights**: [pull out key themes: quality, results, shipping speed]
**Rating breakdown**: [5-star bar chart: X% 5-star, X% 4-star, etc.]
**Notes**: Showcase 3-5 top reviews prominently, then allow browsing the rest.

### Section 6: FAQ
**Q1**: "[Shipping question - How fast does it ship?]"
**A1**: "[Answer with specific timeline]"
**Q2**: "[Return question - What if it doesn't work for me?]"
**A2**: "[Answer with guarantee details]"
**Q3**: "[Usage question - How do I use it?]"
**A3**: "[Answer with simple instructions]"
**Q4**: "[Comparison question - How is this different from [competitor]?]"
**A4**: "[Answer with key differentiator]"
**Q5**: "[Ingredient/material question]"
**A5**: "[Answer with specifics and sourcing details]"

### Section 7: Add to Cart
**Variant selector**: [size / color / flavor / quantity]
**Quantity selector**: [default to 1]
**Add to Cart button**: [Large, high-contrast, sticky on mobile]
**Button text**: [Add to Cart / Add to Bag / Buy Now]
**Trust badges below button**: [Secure checkout, free shipping threshold, money-back guarantee]
**Shipping info**: [Free shipping over $X / Estimated delivery date]
**Guarantee**: [30-day money back / satisfaction guaranteed]

### Section 8: Cross-sells
**Section headline**: "Frequently bought together" or "Complete the set"
**Product 1**: [Complementary product with image, name, price]
**Product 2**: [Complementary product]
**Product 3**: [Complementary product]
**Bundle offer**: [Save X% when you buy together]
**Notes**: Cross-sells should be genuinely complementary, not random.

### Tracking Requirements
**Events**: ViewContent (page load), AddToCart (button click), InitiateCheckout, Purchase
**Enhanced ecommerce**: [product ID, name, price, category, variant in data layer]
**Pixel**: [Meta, Google, TikTok product catalog events]
**GA4**: [view_item, add_to_cart, begin_checkout, purchase with item parameters]

## Usage Notes
- Page speed is critical for ecommerce; optimize images and minimize scripts.
- A/B test the hero image, price presentation, and CTA button copy first.
- Ensure product schema markup is implemented for rich search results.

## Example
A DTC skincare brand product page: 6 product images including lifestyle and texture shots, $39.99 price with Afterpay option, 4.8-star rating from 1,247 reviews, ingredient list with certifications, sticky Add to Cart on mobile.

## Related
- thank-you-page-template.md
- tracking-brief.md
- event-map-template.md
