# GTM Container Template

> **Type**: Template
> **Category**: tracking
> **Used by tasks**: gtm-setup, tracking-implementation, tag-management
> **Filled by agents**: tracking-agent, analytics-agent

## Purpose
Provides a structured blueprint for organizing a Google Tag Manager container with proper tags, triggers, variables, and folder structure following naming conventions that keep the container clean and maintainable.

## Template

### Container Metadata
**Container name**: [client-name-web]
**Container ID**: [GTM-XXXXXXX]
**Environment**: [production / staging / development]
**Last published**: [date]
**Published by**: [person or agent]
**Version notes**: [what changed in this version]

### Naming Conventions
**Tags**: `[Platform] - [Event] - [Type]`
**Triggers**: `[Action] - [Location/Condition]`
**Variables**: `[Type] - [Name]`
**Folders**: `[Platform or Function]`

### Folder Structure
| Folder Name | Contents |
|---|---|
| Meta Pixel | All Meta/Facebook pixel tags |
| Google Ads | Google Ads conversion and remarketing tags |
| GA4 | GA4 configuration and event tags |
| TikTok | TikTok pixel tags |
| LinkedIn | LinkedIn Insight Tag and events |
| Utilities | Helper tags (consent, data layer pushes, error tracking) |
| Deprecated | Old tags kept for reference but paused |

### Tags by Platform

#### GA4 Tags
| Tag Name | Tag Type | Trigger | Notes |
|---|---|---|---|
| GA4 - Config - PageView | GA4 Configuration | All Pages | Base config with Measurement ID |
| GA4 - Event - ViewContent | GA4 Event | ViewContent - Product Page | Sends view_item event |
| GA4 - Event - AddToCart | GA4 Event | AddToCart - Button Click | Sends add_to_cart event |
| GA4 - Event - BeginCheckout | GA4 Event | Checkout - Page Load | Sends begin_checkout event |
| GA4 - Event - Purchase | GA4 Event | Purchase - Confirmation Page | Sends purchase event |
| GA4 - Event - Lead | GA4 Event | FormSubmit - Lead Form | Sends generate_lead event |

#### Meta Pixel Tags
| Tag Name | Tag Type | Trigger | Notes |
|---|---|---|---|
| Meta - PageView - Base | Custom HTML | All Pages | Base pixel with PageView |
| Meta - ViewContent - Product | Custom HTML | ViewContent - Product Page | Includes content_id, value |
| Meta - AddToCart - Click | Custom HTML | AddToCart - Button Click | Includes content_id, value |
| Meta - Purchase - Confirmation | Custom HTML | Purchase - Confirmation Page | Includes value, order_id |
| Meta - Lead - FormSubmit | Custom HTML | FormSubmit - Lead Form | Includes lead type |

#### Google Ads Tags
| Tag Name | Tag Type | Trigger | Notes |
|---|---|---|---|
| GoogleAds - Remarketing - AllPages | Google Ads Remarketing | All Pages | Base remarketing tag |
| GoogleAds - Conversion - Purchase | Google Ads Conversion | Purchase - Confirmation Page | Primary conversion action |
| GoogleAds - Conversion - Lead | Google Ads Conversion | FormSubmit - Lead Form | Secondary conversion action |

#### TikTok Tags
| Tag Name | Tag Type | Trigger | Notes |
|---|---|---|---|
| TikTok - PageView - Base | Custom HTML | All Pages | Base pixel initialization |
| TikTok - ViewContent - Product | Custom HTML | ViewContent - Product Page | Product view event |
| TikTok - Purchase - Confirmation | Custom HTML | Purchase - Confirmation Page | Purchase conversion |

### Triggers by Action
| Trigger Name | Trigger Type | Condition | Used By |
|---|---|---|---|
| All Pages | Page View | All pages | Base pixel tags, config tags |
| ViewContent - Product Page | Page View | URL contains /product/ | ViewContent event tags |
| AddToCart - Button Click | Click - All Elements | Click class contains "add-to-cart" | AddToCart event tags |
| Checkout - Page Load | Page View | URL contains /checkout | BeginCheckout event tags |
| Purchase - Confirmation Page | Page View | URL contains /thank-you or /confirmation | Purchase event tags |
| FormSubmit - Lead Form | Form Submission | Form ID equals "lead-form" | Lead event tags |
| ScrollDepth - 25/50/75/100 | Scroll Depth | Vertical scroll thresholds | GA4 scroll events |
| VideoPlay - YouTube | YouTube Video | Start, Progress, Complete | GA4 video events |
| Custom Event - DataLayer | Custom Event | Event name matches [custom_event] | Custom event tags |

### Variables (Data Layer)
| Variable Name | Variable Type | Data Layer Key | Used For |
|---|---|---|---|
| DL - Product ID | Data Layer | ecommerce.items.0.item_id | ViewContent, AddToCart, Purchase |
| DL - Product Name | Data Layer | ecommerce.items.0.item_name | Event parameters |
| DL - Product Value | Data Layer | ecommerce.value | Value parameter across events |
| DL - Currency | Data Layer | ecommerce.currency | Currency parameter |
| DL - Order ID | Data Layer | ecommerce.transaction_id | Purchase deduplication |
| DL - Event ID | Data Layer | eventId | CAPI deduplication |
| DL - User Email Hash | Data Layer | user.email_hash | Enhanced conversions |

### Variables (Built-in and Custom)
| Variable Name | Variable Type | Purpose |
|---|---|---|
| Page URL | Built-in | Trigger conditions and event parameters |
| Click Classes | Built-in | Button click identification |
| Form ID | Built-in | Form submission identification |
| JS - Timestamp | Custom JavaScript | Generate event timestamps |
| JS - Event ID Generator | Custom JavaScript | Generate unique event IDs for dedup |
| Lookup - Page Type | Lookup Table | Map URLs to page types |

## Usage Notes
- Always publish in staging first and QA before pushing to production.
- Use GTM preview mode to test every tag before publishing.
- Document every version with clear notes on what changed.
- Keep deprecated tags in their folder for 90 days before deleting.

## Example
Ecommerce container with 15 tags across GA4, Meta, Google Ads, and TikTok. 8 triggers covering page views, clicks, and form submissions. 12 variables pulling from data layer for ecommerce parameters.

## Related
- event-map-template.md
- data-layer-spec-template.md
- qa-checklist-template.md
