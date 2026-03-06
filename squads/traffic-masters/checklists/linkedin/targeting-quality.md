# LinkedIn Targeting Quality Gate

> Quality gate for LinkedIn audience targeting (job title, company, seniority, skills, groups). Must pass before campaigns are activated.

## Section 1: Professional Demographic Targeting
- [ ] Job title targeting uses LinkedIn's standardized job titles (not free-text guesses)
- [ ] Job function targeting is used as a broader alternative when specific titles are too narrow
- [ ] Seniority level targeting is applied (Entry, Senior, Manager, Director, VP, CXO, Owner)
- [ ] Years of experience filter is applied when relevant to narrow the audience
- [ ] Job titles, functions, and seniority are combined with AND logic (not stacked as OR creating overly broad reach)

## Section 2: Company Targeting
- [ ] Company size targeting matches the ICP (Ideal Customer Profile): SMB (1-200), Mid-Market (201-1000), Enterprise (1001+)
- [ ] Company industry targeting uses LinkedIn's industry taxonomy aligned with the target verticals
- [ ] Company name targeting is used for ABM (Account-Based Marketing) campaigns with uploaded account lists
- [ ] Company followers targeting is used or excluded based on campaign goal (brand fans vs. new prospects)
- [ ] Company growth rate or company revenue filters are applied when available and relevant

## Section 3: Skills, Interests, and Groups
- [ ] Member skills targeting identifies relevant professional competencies (e.g., "Salesforce", "Digital Marketing")
- [ ] Member interests targeting is used for broader topical alignment (LinkedIn infers from content engagement)
- [ ] LinkedIn Group membership targeting reaches engaged professionals in specific communities
- [ ] Matched Audiences (website retargeting, contact lists, account lists) are configured for retargeting campaigns
- [ ] Lookalike audiences are built from high-performing seed audiences (minimum 300 members in seed)

## Section 4: Exclusions and Audience Quality
- [ ] Existing customers or current clients are excluded from prospecting campaigns
- [ ] Competitors' employees are excluded (by company name) unless running a competitive campaign
- [ ] Audience size is within LinkedIn's recommended range: 50,000-500,000 for Sponsored Content
- [ ] Targeting is not too narrow (under 50,000 will result in slow delivery and high CPMs)
- [ ] Audience forecast in Campaign Manager shows reasonable estimated results for the budget

## Section 5: Geographic and Language Settings
- [ ] Geographic targeting matches the business's serviceable market (country, state/region, city, or radius)
- [ ] Profile language targeting is set to match the ad creative language
- [ ] "Recent or permanent" location setting is selected (default) vs. "Permanent" only
- [ ] Multi-country campaigns are split into separate campaigns for budget control and performance analysis
- [ ] Targeting does not combine so many criteria that the audience becomes impractically small

## Approval
- **Minimum pass rate**: 19/23 items (83%)
- **Reviewer**: media-buyer-agent
- **Escalation**: Audience size below 10,000 or missing exclusions are hard blocks; targeting must be revised before activation
