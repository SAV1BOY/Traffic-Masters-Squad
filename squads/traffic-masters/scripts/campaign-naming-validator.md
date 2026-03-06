# Campaign Naming Validator — Script Guide

## Purpose
Validate that campaign names follow the squad's naming convention.

## Naming Convention
`[PLATFORM]_[OBJECTIVE]_[GEO]_[FUNNEL/AUDIENCE]_[OFFER]_[PERIOD]`

## Valid Values

### Platform
META, GOOG, TIKTOK, YT, LINKEDIN

### Objective
CONV, LEADS, TRAFFIC, AWARENESS, BRAND, SHOPPING, PMAX, SEARCH

### Geo
US, UK, BR, CA, AU, EU, GLOBAL, [ISO-2 codes]

### Funnel/Audience
TOFU, MOFU, BOFU, COLD, WARM, HOT, BRAND, RT, LAL1, LAL3, LAL5

### Period
2026Q1, 2026Q2, 2026-01, 2026-03, EVERGREEN

## Validation Rules
1. Minimum 4 segments separated by underscores
2. Platform must be from valid list
3. Objective must be from valid list
4. No spaces allowed
5. Maximum 100 characters total

## Validation Checklist
- [ ] Platform prefix is valid
- [ ] Objective is recognized
- [ ] Geo code is valid
- [ ] Audience/funnel segment is descriptive
- [ ] Period format is correct
- [ ] Total length under 100 characters
- [ ] No spaces or special characters (except underscores)

## Common Errors
| Error | Fix |
|-------|-----|
| Spaces in name | Replace with underscores |
| Missing platform | Add platform prefix |
| Inconsistent geo codes | Use ISO-2 standard |
| No period identifier | Add quarter or month |
| Too long | Abbreviate offer or audience |
