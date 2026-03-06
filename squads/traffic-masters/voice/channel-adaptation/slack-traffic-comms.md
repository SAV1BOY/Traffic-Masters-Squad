# Slack — Traffic Communications

## Purpose
Standards for traffic team communications in Slack.

## Message Types

### Daily Check-In
- Keep to 3-5 bullet points
- Lead with pacing status
- Flag any guardrail warnings
- Note actions taken or needed

### Performance Alert
- Use urgency level prefix: [INFO] [ADVISORY] [ACTION] [ALERT] [CRITICAL]
- State the issue in first line
- Provide data in second line
- Recommend action in third line

### Creative Request
- Brief description of need
- Deadline
- Reference materials (swipe file links)
- Target platform and specs

### Test Result
- Hypothesis
- Winner (or inconclusive)
- Key metric comparison
- Next step

## Formatting Rules
- Use thread replies for discussion (keep channels clean)
- Bold key metrics and action items
- Use code blocks for data tables
- Pin important decisions and outcomes

## Example Messages

**Daily Check-In:**
"[INFO] Daily pacing: Meta 97%, Google 102%, TikTok 88% (delivery issue investigating). CPA: $26 (target $30). No guardrail breaches. Action: refreshing 2 fatigued creatives today."

**Alert:**
"[ALERT] Meta CPA spiked to $45 (target $30) in last 6hrs. Cause: CPM increase in primary ad set. Action: paused underperformer, shifted budget to top ad set. Monitoring."

## Channel Structure
- `#traffic-daily` — Daily updates and check-ins
- `#traffic-alerts` — Automated and manual alerts
- `#traffic-creative` — Creative requests and reviews
- `#traffic-strategy` — Strategic discussions
