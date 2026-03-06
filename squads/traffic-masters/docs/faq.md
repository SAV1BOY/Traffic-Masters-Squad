# FAQ — Traffic Masters Squad

> Frequently asked questions about the Traffic Masters Squad system, operations, and best practices.

---

## General

**Q: What is Traffic Masters Squad?**
A: Traffic Masters Squad is a structured system of 16 AI-powered agents, frameworks, checklists, templates, and workflows designed to manage, optimize, and scale paid media campaigns across platforms.

**Q: What platforms does this squad cover?**
A: Meta (Facebook/Instagram), Google (Search, Shopping, Display, PMax), YouTube, TikTok, LinkedIn, Snapchat, Pinterest, X (Twitter), and programmatic platforms.

**Q: Where do I start?**
A: Read `docs/getting-started.md`, then `docs/squad-overview.md`, then `docs/workflow-guide.md`. These three documents provide the foundation.

**Q: How do I find the right framework for my situation?**
A: Use the Framework Selection Guide at the bottom of `docs/framework-catalog.md` to match your situation to the best approach. Also see `docs/framework-selection-guide.md`.

**Q: Can I use parts of the system without implementing everything?**
A: Yes. Each agent, framework, checklist, and template can be used independently. However, the system delivers the most value when components work together through defined workflows.

---

## Operations

**Q: What's the minimum budget to test a new platform?**
A: Enough to exit learning phase with statistically meaningful data. Rules of thumb: Meta approximately $250/week, Google approximately $500/week, TikTok approximately $350/week. These are minimums — more budget yields faster and more reliable data.

**Q: How many creatives should I test at once?**
A: 3-5 per ad set. Test hooks first (5 variations), then angles, then formats. Avoid testing more than one variable at a time for clean results.

**Q: When should I kill an underperforming ad?**
A: When CPA exceeds 1.5x target after $100+ spend OR CTR is below 0.5% after 5,000 impressions. Allow at least 72 hours and learning phase exit before making final judgments.

**Q: How often should I refresh creative?**
A: When frequency exceeds 3.0 per week or CTR drops 20% from peak. Proactively launch new creative every 2-4 weeks. See `scripts/creative-rotation-script.md` for the full decision process.

**Q: How do I know if my campaign is in learning phase?**
A: Check the platform's delivery status indicator. Learning phase typically requires about 50 conversion events to complete (Meta). During learning, avoid making significant changes to budget, audience, or creative.

**Q: What's the maximum budget increase I should make at once?**
A: No more than 20-30% per increment. Larger increases can reset the learning phase and destabilize performance. See the Campaign Scaling Framework in `docs/framework-catalog.md`.

**Q: How long should I wait before optimizing a new campaign?**
A: Allow at least 7 days and learning phase exit (approximately 50 conversions on Meta). Making changes too early prevents the algorithm from stabilizing and leads to unreliable data.

---

## Reporting

**Q: What report do I send and when?**
A: Daily check-in (internal, every morning), weekly scorecard (end of week), monthly report (first week of the following month), quarterly business review (end of quarter). See `docs/template-catalog.md` for report templates.

**Q: Where do I log my decisions?**
A: In `data/registries/decisions-log.yaml`. Every optimization action, budget change, and strategic decision should be documented with date, rationale, and expected impact.

**Q: How do I handle a report that shows bad performance?**
A: Be transparent and specific. Use the reporting phrases in `phrases/reporting-phrases.md` for professional language. Always include: what happened, why it happened, what you are doing about it, and what you expect going forward.

---

## Creative

**Q: What makes a good ad hook?**
A: A good hook stops the scroll in the first 3 seconds (video) or first glance (static). It should be specific, relevant to the audience, and create an open loop that compels continued engagement. See `phrases/hooks-headlines.md` for 60+ proven formulas.

**Q: How do I know if creative fatigue is the problem?**
A: Key indicators: CTR declining 20%+ from peak, frequency rising above 3.0-3.5, CPA increasing without other changes, engagement metrics declining. The creative fatigue detection framework provides systematic monitoring. See `docs/framework-catalog.md` (Framework #11).

**Q: Should I use UGC or polished creative?**
A: Test both. UGC often outperforms polished creative on platforms like Meta and TikTok, especially for TOFU. Polished creative tends to perform well for brand campaigns and BOFU. Let the data decide.

**Q: How many creative variations should I have running at all times?**
A: Minimum 3 active winners per campaign. Ideally, maintain a pipeline of 5-10 creatives at various lifecycle stages (new, ramping, peak, declining) to ensure continuity.

---

## Audiences

**Q: What lookalike percentage should I use?**
A: Start with 1% for highest quality, then test 1-3% and 3-5% for broader reach. Smaller percentages are more similar to your source audience. Larger percentages provide more reach but less precision.

**Q: How often should I refresh my audiences?**
A: Custom audiences from CRM: monthly. Lookalike seed audiences: monthly (use most recent converter data). Retargeting audiences: review windows monthly. Exclusion lists: weekly. See `scripts/audience-refresh-script.md`.

**Q: What's audience overlap and why does it matter?**
A: Audience overlap is the percentage of users shared between ad sets. High overlap (above 30%) causes your campaigns to compete against each other in the auction, driving up costs. Use the Audience Agent to analyze and reduce overlap.

---

## Tracking & Data

**Q: Why don't my platform numbers match Google Analytics?**
A: This is normal. Different attribution windows, ad blockers, cross-domain tracking gaps, and view-through conversion inclusion all cause discrepancies. A 10-30% difference is typical. See `docs/troubleshooting.md` for details.

**Q: Should I use server-side tracking (CAPI)?**
A: Yes, whenever possible. Server-side tracking recovers conversion data lost to ad blockers and browser privacy features. It typically improves data match rates by 10-30%.

**Q: What attribution model should I use?**
A: Start with platform defaults. As you mature, consider data-driven or multi-touch models. For e-commerce with short sales cycles, last-click or 7-day click works well. For B2B with long sales cycles, multi-touch is more accurate. See the Attribution Framework in `docs/framework-catalog.md`.

---

## Compliance

**Q: My ad got rejected. What do I do?**
A: First, read the specific policy violation cited by the platform. Review your ad copy and creative against that policy. Fix the violation. Resubmit. If you believe the rejection is incorrect, file an appeal. See `docs/troubleshooting.md` under "Ad Disapprovals."

**Q: How do I write compliant ads for regulated industries?**
A: Use the Compliance Agent for pre-launch review. Avoid unsubstantiated claims, absolute guarantees, and before/after comparisons without proper disclaimers. See the Compliance Review Checklist in `docs/checklist-catalog.md`.

**Q: What claims require substantiation?**
A: Any specific result, statistic, or performance claim. "Increase revenue by 40%" requires proof. "A framework designed to improve performance" does not. When in doubt, soften the claim or add substantiation.

---

## Budget

**Q: How should I split budget across funnel stages?**
A: A common starting point is 60% TOFU (awareness/prospecting), 20% MOFU (consideration), 20% BOFU (conversion/retargeting). Adjust based on your business model, sales cycle, and current pipeline needs.

**Q: How do I know if I'm spending enough?**
A: If you are hitting KPI targets and budget utilization is above 95%, you likely have room to scale. If campaigns are budget-constrained (spend limited), you're leaving conversions on the table. Use the Marginal Efficiency Analysis framework to determine optimal spend levels.

**Q: When should I reallocate budget between campaigns?**
A: When marginal CPA differs significantly between campaigns (one is efficient, another is not). Review weekly during optimization cycles. See `scripts/budget-reallocation-script.md` for the decision tree.

---

## Cross-Squad Integration

**Q: How does Traffic Masters work with Copy Squad?**
A: Copy Squad provides brand messaging and ad copy. Traffic Masters provides performance data on copy effectiveness. Coordination happens through weekly syncs and shared creative briefs. See `docs/cross-squad-integration.md`.

**Q: How does Traffic Masters work with Brand Squad?**
A: Brand Squad provides guidelines and visual identity. Traffic Masters ensures all ads comply with brand standards and provides data on brand element performance. See `docs/cross-squad-integration.md`.

---

## System & Configuration

**Q: Where is the main configuration file?**
A: `config.yaml` in the squad root directory. See `docs/config-yaml-guide.md` for detailed documentation of every setting.

**Q: How do I add a new advertising platform?**
A: Add a platform entry in `config.yaml`, update platform codes in `docs/naming-conventions.md`, configure tracking for the new platform, and build initial audience segments. See `docs/onboarding-new-account.md`.

**Q: How do I contribute to the system?**
A: See `docs/contributing.md` for the full guide. Key steps: plan your contribution, follow naming and formatting standards, validate quality, update the changelog and relevant catalogs.
