# Platform API Reference

## Purpose
Quick reference for major advertising platform APIs, endpoints, authentication methods, and common operations used in paid traffic management and reporting.

---

## Meta (Facebook) Marketing API

### Overview
| Property | Value |
|---|---|
| **Base URL** | `https://graph.facebook.com/v19.0/` |
| **Authentication** | OAuth 2.0 access token |
| **Rate Limits** | Tier-based; typically 200 calls/hour per ad account |
| **Documentation** | https://developers.facebook.com/docs/marketing-apis |

### Key Endpoints

| Operation | Endpoint | Method | Description |
|---|---|---|---|
| Get campaigns | `/act_{ad_account_id}/campaigns` | GET | List all campaigns |
| Get ad sets | `/act_{ad_account_id}/adsets` | GET | List all ad sets |
| Get ads | `/act_{ad_account_id}/ads` | GET | List all ads |
| Get insights | `/act_{ad_account_id}/insights` | GET | Performance data |
| Get campaign insights | `/{campaign_id}/insights` | GET | Campaign-level metrics |
| Create campaign | `/act_{ad_account_id}/campaigns` | POST | Create new campaign |
| Update campaign | `/{campaign_id}` | POST | Update campaign settings |
| Get custom audiences | `/act_{ad_account_id}/customaudiences` | GET | List audiences |
| Get ad creatives | `/act_{ad_account_id}/adcreatives` | GET | List creatives |

### Common Insights Fields
```
fields=campaign_name,spend,impressions,clicks,ctr,cpc,actions,
cost_per_action_type,action_values,reach,frequency
```

### Breakdowns
```
breakdowns=age,gender,country,publisher_platform,platform_position
```

### Date Range
```
time_range={"since":"2026-01-01","until":"2026-01-31"}
time_increment=1  (daily data)
```

### Useful Parameters
```
level=campaign|adset|ad
filtering=[{"field":"campaign.effective_status","operator":"IN","value":["ACTIVE"]}]
sort=spend_descending
limit=100
```

---

## Google Ads API

### Overview
| Property | Value |
|---|---|
| **Base URL** | `https://googleads.googleapis.com/v16/` |
| **Authentication** | OAuth 2.0 + Developer Token |
| **Rate Limits** | 15,000 requests/day (standard tier) |
| **Documentation** | https://developers.google.com/google-ads/api/docs |

### Key Services

| Service | Purpose | Common Operations |
|---|---|---|
| `GoogleAdsService` | Search and retrieve data | GAQL queries for reporting |
| `CampaignService` | Manage campaigns | Create, update, pause campaigns |
| `AdGroupService` | Manage ad groups | Create, update ad groups |
| `AdGroupAdService` | Manage ads | Create, update ads |
| `KeywordPlanService` | Keyword research | Get keyword ideas, forecasts |
| `CustomerService` | Account management | Get account info |

### Google Ads Query Language (GAQL) Examples

**Campaign Performance:**
```sql
SELECT campaign.name, campaign.status,
       metrics.impressions, metrics.clicks, metrics.cost_micros,
       metrics.conversions, metrics.cost_per_conversion
FROM campaign
WHERE segments.date DURING LAST_30_DAYS
  AND campaign.status = 'ENABLED'
ORDER BY metrics.cost_micros DESC
LIMIT 50
```

**Ad Group Performance:**
```sql
SELECT ad_group.name, campaign.name,
       metrics.impressions, metrics.clicks, metrics.ctr,
       metrics.conversions, metrics.cost_per_conversion
FROM ad_group
WHERE segments.date DURING LAST_7_DAYS
ORDER BY metrics.conversions DESC
```

**Search Terms Report:**
```sql
SELECT search_term_view.search_term,
       metrics.impressions, metrics.clicks, metrics.conversions,
       metrics.cost_micros
FROM search_term_view
WHERE segments.date DURING LAST_30_DAYS
ORDER BY metrics.impressions DESC
LIMIT 100
```

### Date Ranges
```
DURING LAST_7_DAYS
DURING LAST_30_DAYS
DURING THIS_MONTH
DURING LAST_MONTH
BETWEEN '2026-01-01' AND '2026-01-31'
```

### Important: Cost in Micros
Google Ads API returns cost in micros (1/1,000,000 of the currency unit).
```
Actual Cost = cost_micros / 1,000,000
Example: 5000000 micros = $5.00
```

---

## TikTok Marketing API

### Overview
| Property | Value |
|---|---|
| **Base URL** | `https://business-api.tiktok.com/open_api/v1.3/` |
| **Authentication** | Access Token (long-lived) |
| **Rate Limits** | 10 requests/second, 600/minute per app |
| **Documentation** | https://business-api.tiktok.com/portal/docs |

### Key Endpoints

| Operation | Endpoint | Method | Description |
|---|---|---|---|
| Get campaigns | `/campaign/get/` | GET | List campaigns |
| Get ad groups | `/adgroup/get/` | GET | List ad groups |
| Get ads | `/ad/get/` | GET | List ads |
| Get report | `/report/integrated/get/` | GET | Performance data |
| Create campaign | `/campaign/create/` | POST | Create campaign |
| Get audiences | `/dmp/custom_audience/list/` | GET | List custom audiences |

### Report Dimensions
```
dimensions=["campaign_id","stat_time_day"]
metrics=["spend","impressions","clicks","conversion","cost_per_conversion","ctr","cpc"]
```

---

## Google Analytics 4 (GA4) API

### Overview
| Property | Value |
|---|---|
| **Base URL** | `https://analyticsdata.googleapis.com/v1beta/` |
| **Authentication** | OAuth 2.0 or Service Account |
| **Documentation** | https://developers.google.com/analytics/devguides/reporting/data/v1 |

### Key Endpoint
```
POST /v1beta/properties/{property_id}:runReport
```

### Common Request Body
```json
{
  "dateRanges": [{"startDate": "2026-01-01", "endDate": "2026-01-31"}],
  "dimensions": [
    {"name": "sessionSource"},
    {"name": "sessionMedium"},
    {"name": "sessionCampaignName"}
  ],
  "metrics": [
    {"name": "sessions"},
    {"name": "conversions"},
    {"name": "totalRevenue"},
    {"name": "engagementRate"}
  ],
  "dimensionFilter": {
    "filter": {
      "fieldName": "sessionMedium",
      "stringFilter": {"matchType": "EXACT", "value": "cpc"}
    }
  }
}
```

---

## Common Integration Patterns

### Automated Reporting Pipeline
```
1. Scheduled API calls (daily) to pull platform data
2. Store in data warehouse (BigQuery, Snowflake, etc.)
3. Transform and join across platforms
4. Visualize in BI tool (Looker Studio, Tableau, etc.)
5. Automated alerts for threshold breaches
```

### Tools for No-Code API Access

| Tool | Platforms Supported | Best For |
|---|---|---|
| **Supermetrics** | Meta, Google, TikTok, LinkedIn, 70+ | Google Sheets, Looker Studio |
| **Funnel.io** | 500+ connectors | Data warehousing, ETL |
| **Fivetran** | Major platforms | Enterprise data pipelines |
| **Stitch** | Major platforms | Data warehousing |
| **Zapier** | Limited ad platform support | Simple automations |
| **Make (Integromat)** | Meta, Google | Workflow automation |
| **Google Ads Scripts** | Google Ads only | In-platform automation |

---

## API Authentication Quick Start

### Meta Marketing API
1. Create a Facebook App at developers.facebook.com
2. Generate a System User Access Token in Business Manager
3. Grant the token access to ad accounts
4. Use the token in API requests: `access_token={TOKEN}`

### Google Ads API
1. Create a Google Cloud project
2. Enable the Google Ads API
3. Create OAuth 2.0 credentials
4. Apply for a Developer Token (standard access)
5. Authenticate with refresh token flow

### TikTok Marketing API
1. Create an app at business-api.tiktok.com
2. Request API access for your app
3. Generate an access token via OAuth flow
4. Use the token in request headers

---

## Rate Limit Best Practices

1. Implement exponential backoff on 429 (rate limit) responses
2. Cache responses where data does not change frequently
3. Use batch requests where supported
4. Respect platform-specific rate limits
5. Schedule heavy data pulls during off-peak hours
6. Use webhooks or server-to-server callbacks instead of polling where available
