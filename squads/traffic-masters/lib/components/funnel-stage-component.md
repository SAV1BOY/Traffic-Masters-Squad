# Funnel Stage Component

## Purpose
Define campaign objectives, metrics, and creative by funnel stage.

## Stage Definitions

### TOFU — Top of Funnel (Awareness / Prospecting)
- **Objective:** Reach new audiences, generate awareness, drive traffic
- **Audiences:** Cold, interest-based, broad, lookalikes
- **Creatives:** Educational, entertaining, brand story, UGC
- **Metrics:** CPM, reach, CTR, hook rate, video views
- **Success:** High volume of qualified traffic at target CPM

### MOFU — Middle of Funnel (Consideration)
- **Objective:** Nurture interest, build trust, educate
- **Audiences:** Warm (site visitors, engagers, video viewers)
- **Creatives:** Testimonials, demos, comparisons, case studies
- **Metrics:** Engagement rate, time on site, micro-conversions
- **Success:** Moving audience toward purchase intent

### BOFU — Bottom of Funnel (Conversion)
- **Objective:** Drive purchases, signups, bookings
- **Audiences:** Hot (ATC, leads, repeat visitors, checkout)
- **Creatives:** Urgency, offers, reminders, social proof
- **Metrics:** CPA, ROAS, conversion rate, AOV
- **Success:** Efficient conversions within CPA target

### Retention — Post-Purchase
- **Objective:** Repeat purchase, upsell, loyalty
- **Audiences:** Customers (segmented by recency and value)
- **Creatives:** New products, loyalty offers, cross-sell
- **Metrics:** Repeat purchase rate, LTV, retention rate
- **Success:** Increasing customer lifetime value

## Component Fields
- `stage`: TOFU | MOFU | BOFU | Retention
- `campaigns`: Associated campaign IDs
- `audiences`: Audience segments for this stage
- `creatives`: Creative types for this stage
- `primary_metric`: Key metric for optimization
- `budget_percentage`: Share of total budget
