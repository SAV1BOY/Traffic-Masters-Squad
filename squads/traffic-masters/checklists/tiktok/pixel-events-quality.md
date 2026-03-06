# TikTok Pixel Event Configuration Quality Gate

> Quality gate for TikTok Pixel and Events API setup. Must pass before conversion-optimized campaigns are launched on TikTok.

## Section 1: Pixel Installation
- [ ] TikTok Pixel base code is installed on all pages of the website
- [ ] Pixel ID matches the correct TikTok Ads Manager account
- [ ] Pixel fires a PageView event on every page load (verified via TikTok Pixel Helper extension)
- [ ] Pixel is installed via Google Tag Manager, TikTok partner integration, or manual code placement
- [ ] No duplicate pixel installations exist on the same page

## Section 2: Standard Event Configuration
- [ ] All required standard events are implemented per the funnel: ViewContent, AddToCart, InitiateCheckout, CompletePayment (e-commerce) or SubmitForm, Contact (lead gen)
- [ ] Each event fires on the correct user action or page (e.g., CompletePayment only on order confirmation)
- [ ] Event parameters are populated: content_id, content_type, content_name, value, currency, quantity
- [ ] Currency uses ISO 4217 codes (BRL, USD, EUR) and value is a numeric string
- [ ] CompletePayment event value matches actual transaction amount

## Section 3: Events API (Server-Side) Setup
- [ ] TikTok Events API is configured for server-side event transmission
- [ ] Server events include required user identifiers: email (SHA256 hashed), phone (SHA256 hashed), IP address, user agent
- [ ] Event deduplication is configured using event_id to prevent double-counting between browser pixel and Events API
- [ ] Events API integration is tested via TikTok Events Manager test event tool
- [ ] Event Match Quality score is monitored and optimized (higher match = better optimization)

## Section 4: Advanced Matching and Data Quality
- [ ] Advanced matching is enabled to improve event match rates (auto or manual matching of user data)
- [ ] First-party data parameters (email, phone) are passed with events when available
- [ ] Cookie consent management is implemented for GDPR/LGPD compliance before pixel fires
- [ ] Event data is validated: no missing required parameters, no malformed values

## Section 5: Event Validation and Testing
- [ ] All events are verified as "Active" in TikTok Events Manager
- [ ] Test events have been triggered and confirmed end-to-end (browser + server)
- [ ] Event volume is consistent with expected website traffic (no sudden drops or spikes indicating errors)
- [ ] Cross-reference TikTok event counts with backend analytics (within 15% tolerance)
- [ ] Optimization event selected in the ad group matches the correctly configured pixel event
- [ ] Event prioritization is documented for conversion optimization hierarchy

## Approval
- **Minimum pass rate**: 18/22 items (82%)
- **Reviewer**: tracking-specialist-agent
- **Escalation**: Deduplication failures or missing Events API setup are hard blocks for conversion campaigns; must be resolved before launch
