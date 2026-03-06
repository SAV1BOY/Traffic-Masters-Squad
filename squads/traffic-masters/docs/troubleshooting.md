# Troubleshooting Guide

> Common issues encountered in Traffic Masters Squad operations and their solutions.

---

## Campaign Delivery Issues

### Ads Not Delivering

**Symptoms:** Zero impressions, campaign shows "active" but no delivery

**Diagnostic Steps:**
1. Check ad review status — ads may be pending review or disapproved
2. Verify budget is set and payment method is active
3. Check audience size — if too small, delivery may be limited
4. Review bid/cost cap — may be too low for the auction
5. Check scheduling — campaign may be scheduled for future dates
6. Verify account status — account may have spending limits or restrictions

**Solutions:**
| Cause | Fix |
|-------|-----|
| Ads under review | Wait 24 hours; contact support if longer |
| Disapproved ads | Review policy violation, fix creative/copy, resubmit |
| Audience too small | Broaden targeting or use broader audience types |
| Bid too low | Increase bid/cost cap or switch to automatic bidding |
| Payment issue | Update payment method in account settings |
| Account restriction | Contact platform support for resolution |

---

### Under-Delivery (Spend Below Target)

**Symptoms:** Budget utilization below 80%

**Diagnostic Steps:**
1. Check bid strategy — cost cap/bid cap may be too restrictive
2. Review audience size and saturation
3. Check if you're in learning phase (limited delivery is normal)
4. Review ad relevance/quality scores
5. Check for competing campaigns (internal auction competition)

**Solutions:**
- Loosen bid caps by 10-20%
- Broaden audience targeting
- Improve creative relevance scores
- Consolidate overlapping ad sets to reduce internal competition
- Allow learning phase to complete (50 conversions) before adjusting

---

### Over-Delivery (Spend Above Target)

**Symptoms:** Budget utilization above 120%

**Diagnostic Steps:**
1. Check budget type — daily budgets can overspend by up to 25% (Meta)
2. Review accelerated delivery settings
3. Check for recently paused campaigns that front-loaded spend
4. Verify campaign spending limits are set

**Solutions:**
- Set campaign spending limits as a safety net
- Switch from accelerated to standard delivery
- Adjust daily budget to account for platform overspend allowance
- Monitor pacing more frequently during high-spend periods

---

## Performance Issues

### CPA Rising Significantly

**Symptoms:** CPA increased 25%+ from baseline

**Diagnostic Steps:**
1. Check creative fatigue (frequency, CTR trends)
2. Review audience saturation (frequency, reach depletion)
3. Check for market changes (seasonal CPM increases, competition)
4. Verify tracking — conversion pixel may have broken
5. Check landing page (load time, form errors, changes)
6. Review recent changes (any settings modified in last 7 days?)

**Solutions:**
| Root Cause | Recommended Action |
|-----------|-------------------|
| Creative fatigue | Introduce new creative variations |
| Audience saturation | Expand or refresh audiences |
| CPM increases | Improve ad relevance or diversify placements |
| Broken tracking | Fix tracking immediately (see Tracking Issues) |
| Landing page issue | Fix page speed, errors, or message match |
| Recent changes | Revert if performance declined post-change |

---

### CTR Dropping

**Symptoms:** CTR declined 20%+ from peak

**Diagnostic Steps:**
1. Check frequency — are users seeing ads too often?
2. Review creative age — how long has this creative been running?
3. Check audience changes — has targeting shifted?
4. Review competitive landscape — are competitors running similar ads?
5. Check platform changes — have algorithm updates affected delivery?

**Solutions:**
- Refresh creative with new hooks, angles, or formats
- Adjust frequency caps
- Expand audiences to reach new users
- Differentiate messaging from competitors
- Test new ad placements

---

### Conversion Rate Dropping (Landing Page)

**Symptoms:** Traffic quality appears normal, but landing page CVR declined

**Diagnostic Steps:**
1. Test page load speed (ideally under 3 seconds)
2. Check for form errors or broken elements
3. Review message match between ad and page
4. Check mobile experience separately
5. Look for UX changes that may have been deployed
6. Verify tracking — events may have stopped firing

**Solutions:**
- Optimize page speed (compress images, reduce scripts)
- Fix any broken forms or elements
- Ensure headline and offer match the ad that drives traffic
- Optimize mobile experience separately
- Revert any recent UX changes and test
- Verify and fix conversion event tracking

---

## Tracking Issues

### Platform vs. Analytics Discrepancy

**Symptoms:** Ad platform reports different conversion numbers than analytics tool

**Common Causes:**
1. Different attribution windows (platform: 7-day click; analytics: session-based)
2. Ad blockers preventing client-side pixel from firing
3. Cross-domain tracking misconfiguration
4. Cookie consent blocking tracking scripts
5. Delayed conversion reporting (platform attribution lag)
6. View-through conversions included in platform but not analytics

**Solutions:**
- Document expected discrepancy range (10-30% is common)
- Implement server-side tracking (CAPI) to reduce ad blocker impact
- Verify cross-domain tracking configuration
- Audit cookie consent implementation
- Use consistent attribution windows for comparison
- Exclude view-through conversions when comparing to analytics

---

### Pixel Not Firing

**Symptoms:** Zero or unexpectedly low conversion counts

**Diagnostic Steps:**
1. Use platform's pixel helper tool (Meta Pixel Helper, Google Tag Assistant)
2. Check if pixel base code is present on the page
3. Verify event code is on the correct page (thank-you page, not landing page)
4. Check for JavaScript errors blocking pixel execution
5. Verify server-side events are configured and sending
6. Check if cookie consent is blocking the pixel

**Solutions:**
- Reinstall pixel base code if missing
- Move event code to the correct page
- Fix JavaScript errors
- Implement server-side tracking as backup
- Test with cookie consent in both accepted and rejected states
- Verify through platform's event manager / diagnostics tool

---

### UTM Parameters Missing or Incorrect

**Symptoms:** Analytics shows "(not set)" or incorrect source/medium

**Diagnostic Steps:**
1. Check UTM parameters in the actual ad destination URLs
2. Verify URL formatting (proper ? and & usage)
3. Check for URL redirects that strip parameters
4. Verify landing page isn't removing URL parameters
5. Check for duplicate ? in the URL

**Solutions:**
- Rebuild UTMs using a consistent template
- Test destination URLs with UTMs appended
- Configure redirects to preserve URL parameters
- Use URL builder tools to prevent formatting errors
- Audit all active campaigns for UTM consistency

---

## Account & Policy Issues

### Ad Disapprovals

**Symptoms:** Ads rejected by platform policy review

**Diagnostic Steps:**
1. Read the specific policy violation cited
2. Review the ad copy and creative against the policy
3. Check if the landing page is flagged (misleading content, broken links)
4. Determine if the policy is new or recently changed

**Solutions:**
- Edit the ad to comply with the specific policy cited
- Remove prohibited claims, imagery, or language
- Fix landing page issues (add required disclosures, fix broken elements)
- Appeal if you believe the disapproval is incorrect
- Consult Compliance Agent for compliant alternatives

---

### Account Restrictions / Spending Limits

**Symptoms:** Account has unexpected spending limits or restricted features

**Solutions:**
- For new accounts: Spending limits increase automatically with payment history
- Request spending limit increase through platform settings
- Verify business verification is complete
- Ensure payment method is valid and has sufficient funds
- Contact platform support for account-specific restrictions

---

## System & Process Issues

### Registry Data Inconsistency

**Symptoms:** Registry entries don't match actual campaign settings

**Solutions:**
- Run a full registry audit comparing entries to platform settings
- Update all stale entries
- Implement a post-change registry update step in all workflows
- Set up weekly registry consistency checks

---

### Workflow Bottlenecks

**Symptoms:** Tasks are delayed, approvals are stalled

**Solutions:**
- Identify the specific bottleneck stage
- Check if the owning agent has the required inputs
- Escalate approval requests with deadline context
- Consider whether quality gates can be streamlined without sacrificing quality
- Document recurring bottlenecks for process improvement

---

## Escalation Matrix

| Issue Severity | Response Time | Escalation Path |
|---------------|--------------|-----------------|
| Critical (revenue loss, broken tracking) | < 1 hour | Diagnostics Agent -> Account lead -> Stakeholder |
| High (significant performance decline) | < 8 hours | Optimization Agent -> Strategy Agent |
| Medium (optimization opportunity) | < 2 days | Optimization Agent -> Weekly cycle |
| Low (minor issue, no performance impact) | < 1 week | Log and address in next optimization cycle |

---

## When to Contact Platform Support

Contact platform support when:
- Account is suspended or restricted without clear cause
- Ad disapprovals cannot be resolved through self-service
- Bug or glitch is suspected (data anomalies, UI errors)
- Feature access issues
- Billing discrepancies
- API access problems

Document every support interaction in the decisions log with ticket numbers and outcomes.
