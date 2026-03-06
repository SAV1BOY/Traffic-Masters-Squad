# Google Tag Manager Configuration Quality Gate

> Quality gate for Google Tag Manager (GTM) container setup and tag management. Must pass before the GTM container is published to production.

## Section 1: Container Setup
- [ ] GTM container ID is correct and matches the website/property it is installed on
- [ ] GTM container snippet is installed correctly: <script> in <head> and <noscript> immediately after <body>
- [ ] Only one GTM container is installed per page (no duplicate containers)
- [ ] Container is organized with descriptive naming: tags, triggers, and variables use consistent naming conventions
- [ ] Container version notes document what changed in each published version

## Section 2: Data Layer Configuration
- [ ] Data layer (dataLayer) is initialized before the GTM container snippet loads
- [ ] E-commerce data layer follows Google's recommended schema (Enhanced E-commerce or GA4 e-commerce)
- [ ] Data layer pushes include all required variables: page type, user ID (hashed), transaction data, product data
- [ ] Data layer values are validated: no undefined, null, or empty values for required fields
- [ ] Custom data layer variables are created in GTM to extract values from dataLayer pushes

## Section 3: Tag Configuration
- [ ] All platform tags (GA4, Meta Pixel, Google Ads, TikTok, LinkedIn) are implemented via GTM (not hardcoded)
- [ ] Tags use built-in templates where available (GA4 Configuration, Google Ads Conversion Tracking, etc.)
- [ ] Custom HTML tags are used only when no built-in template exists (documented with justification)
- [ ] Tag firing priority is set correctly: consent tags > configuration tags > event tags
- [ ] Tag sequencing is configured where order matters (e.g., GA4 config tag fires before event tags)
- [ ] No tag fires on all pages unnecessarily (each tag has a specific trigger)

## Section 4: Trigger Configuration
- [ ] Page view triggers use the correct type: Page View, DOM Ready, or Window Loaded based on requirements
- [ ] Click triggers use Click - All Elements or Click - Just Links with proper CSS selectors or click text
- [ ] Form submission triggers are tested across all form types on the site
- [ ] Custom event triggers match the exact event names pushed to the data layer
- [ ] Trigger conditions (filters) are correctly configured to prevent misfires

## Section 5: Consent Mode and Privacy
- [ ] Consent Mode v2 is implemented with proper default and update commands
- [ ] Tags respect consent signals: ad_storage, analytics_storage, ad_user_data, ad_personalization
- [ ] Consent-dependent tags are blocked until consent is granted
- [ ] Cookie banner/CMP integration with GTM is tested and fires consent update events correctly

## Section 6: Testing and Publishing
- [ ] All tags, triggers, and variables are tested in GTM Preview mode before publishing
- [ ] Preview mode confirms correct firing order and data layer values on key pages
- [ ] No JavaScript errors appear in the browser console caused by GTM tags
- [ ] Container version is published with descriptive version notes
- [ ] A workspace backup or version snapshot is saved before each publish

## Approval
- **Minimum pass rate**: 21/25 items (84%)
- **Reviewer**: tracking-specialist-agent
- **Escalation**: Missing consent mode implementation or duplicate containers are hard blocks; must be resolved before publishing to production
