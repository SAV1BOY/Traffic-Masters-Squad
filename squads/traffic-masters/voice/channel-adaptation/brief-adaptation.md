# Voice Adaptation: Briefs and Documentation

## Purpose
Guidelines for adapting the Traffic Masters voice for briefs, strategy documents, SOPs, and internal documentation. Optimizes for precision, completeness, and reusability.

---

## Core Principles for Briefs and Documentation

1. **Write for the person who was not in the room.** Assume the reader has context on paid traffic but none on this specific situation.
2. **Be specific enough to act on.** If someone cannot execute from the document alone, it is incomplete.
3. **Separate facts from opinions.** Label data-driven conclusions differently from strategic judgment calls.
4. **Version and date everything.** Briefs evolve; make it clear which version is current.
5. **Front-load the objective.** The reader should know what this document is for within the first 3 sentences.

---

## Brief Voice Characteristics

| Aspect | Guideline |
|---|---|
| **Tone** | Clear, precise, instructional |
| **Person** | Third person for descriptions ("The campaign targets..."), first person plural for recommendations ("We recommend...") |
| **Tense** | Present tense for current state and plans, past tense for background/rationale |
| **Length** | Proportional to complexity: simple brief (1-2 pages), strategy doc (3-8 pages), SOP (as long as needed) |
| **Jargon** | Acceptable with definitions on first use if the document may reach non-specialists |
| **Structure** | Highly structured with numbered sections, tables, and clear headers |

---

## Document Types and Formats

### Campaign Brief

**Purpose:** Define everything needed to set up and launch a campaign.

**Voice:** Directive, specific, complete

**Required Sections:**

#### 1. Overview
```
Campaign Name: {{CAMPAIGN_NAME}}
Account: {{ACCOUNT_NAME}}
Author: {{NAME}}
Date: {{DATE}}
Version: {{VERSION}}
Status: Draft / In Review / Approved / Active
```

#### 2. Objective
- **Business objective:** What business outcome this campaign supports
- **Campaign objective:** The specific paid media goal (conversions, leads, awareness)
- **Primary KPI:** The single metric that defines success
- **Secondary KPIs:** Supporting metrics to monitor
- **Target:** Quantified success criteria (e.g., "50 conversions/week at less than $60 CPA")

**Language pattern:**
- "The objective of this campaign is to [ACTION] by [METHOD], targeting [KPI] of [VALUE]."
- "Success is defined as [QUANTIFIED_OUTCOME] within [TIMEFRAME]."

#### 3. Audience
- **Primary audience:** Demographics, interests, behaviors
- **Audience segments:** Specific targeting parameters per platform
- **Exclusions:** Who to exclude and why
- **Estimated audience size:** Per platform

**Language pattern:**
- "The primary audience is [DESCRIPTION], estimated at [SIZE] on [PLATFORM]."
- "Exclude [SEGMENT] to avoid [REASON]."

#### 4. Messaging and Creative
- **Key message:** The single most important thing to communicate
- **Supporting messages:** Secondary proof points or value propositions
- **Creative formats:** Required ad formats and specifications
- **Creative assets:** List of assets needed with specs
- **Tone direction:** Reference the appropriate tone profile

**Language pattern:**
- "The primary message is [MESSAGE], supported by [PROOF_POINTS]."
- "Creative should follow the [TONE_PROFILE] tone profile."

#### 5. Budget and Timing
- **Total budget:** Campaign lifetime budget
- **Daily budget:** Target daily spend
- **Flight dates:** Start and end dates
- **Budget allocation:** Split by platform, funnel stage, or audience
- **Pacing notes:** Any front-loading, back-loading, or event-driven pacing

#### 6. Platform Setup
- **Platforms:** Which platforms and campaign types
- **Campaign structure:** Campaign, ad set, and ad naming conventions
- **Bidding strategy:** Bid type and targets
- **Conversion event:** Which event to optimize toward
- **Attribution window:** Click-through and view-through settings

#### 7. Measurement Plan
- **Tracking requirements:** Pixels, UTMs, offline conversions
- **Reporting cadence:** Daily, weekly, or custom
- **Success evaluation date:** When to make the go/no-go decision
- **Minimum sample size:** Conversions needed before evaluating

#### 8. Risks and Mitigations
- **Identified risks:** What could go wrong
- **Mitigation plans:** How to address each risk
- **Escalation triggers:** When to escalate and to whom

---

### Strategy Document

**Purpose:** Outline the strategic approach for an account, channel, or initiative over a defined period.

**Voice:** Strategic, evidence-based, forward-looking

**Required Sections:**

#### 1. Context and Background
- Current state of the account or initiative
- Performance summary of the relevant period
- Key challenges or opportunities identified
- Market or competitive context

**Language pattern:**
- "The account currently delivers [METRICS]. The primary challenge is [CHALLENGE]."
- "Market conditions have shifted: [CHANGE], creating an opportunity to [OPPORTUNITY]."

#### 2. Strategic Objectives
- 3-5 objectives for the strategy period
- Each objective should be specific, measurable, and time-bound
- Prioritized by impact

**Language pattern:**
- "Objective 1: [WHAT] by [WHEN], measured by [KPI], targeting [VALUE]."

#### 3. Strategic Approach
- The overarching approach and rationale
- Key strategic bets or hypotheses
- How this differs from the previous approach

**Language pattern:**
- "The strategic approach centers on [CORE_STRATEGY] because [EVIDENCE/RATIONALE]."
- "This represents a shift from [OLD_APPROACH] to [NEW_APPROACH], driven by [REASON]."

#### 4. Tactical Plan
- Specific actions by channel, audience, or initiative
- Timeline with milestones
- Resource requirements
- Dependencies

**Language pattern:**
- "Phase 1 ([DATES]): [ACTIONS]. Milestone: [MEASURABLE_OUTCOME]."

#### 5. Budget Framework
- Total investment for the strategy period
- Allocation by channel, funnel stage, or initiative
- Contingency or flex budget
- Scaling triggers and criteria

#### 6. Measurement Framework
- KPIs mapped to each objective
- Reporting cadence and format
- Decision points and evaluation criteria
- Attribution approach

#### 7. Risks and Contingencies
- Key risks with probability and impact assessment
- Contingency plans for each risk
- Decision triggers for plan B scenarios

---

### Standard Operating Procedure (SOP)

**Purpose:** Document a repeatable process so anyone on the team can execute it consistently.

**Voice:** Instructional, step-by-step, unambiguous

**Formatting Rules:**
- Use numbered steps, not paragraphs
- Each step should be a single action
- Include screenshots or examples where helpful
- Bold key interface elements, button names, and field values
- Include "if/then" branches for decision points

**Required Sections:**

#### 1. Header
```
SOP Title: {{TITLE}}
Process Owner: {{NAME}}
Last Updated: {{DATE}}
Version: {{VERSION}}
Applies To: {{ROLE/TEAM}}
Estimated Time: {{DURATION}}
Frequency: {{HOW_OFTEN}}
```

#### 2. Purpose
- One sentence explaining why this process exists
- When to use this SOP

**Language pattern:**
- "This SOP covers the process for [TASK]. Follow this procedure when [TRIGGER]."

#### 3. Prerequisites
- Required access, tools, or permissions
- Information needed before starting
- Related SOPs to complete first

#### 4. Step-by-Step Instructions
**Language pattern:**
- "Step 1: Navigate to **[LOCATION]**."
- "Step 2: Click **[BUTTON]** and select **[OPTION]**."
- "Step 3: Enter the following values: [LIST]."
- "Step 4: Verify that [EXPECTED_RESULT]. If not, see Troubleshooting section."
- "NOTE: [IMPORTANT_CONTEXT]."
- "CAUTION: [RISK_IF_DONE_INCORRECTLY]."

#### 5. Verification
- How to confirm the process was completed correctly
- Expected outcomes or confirmation signals

#### 6. Troubleshooting
- Common issues and how to resolve them
- When to escalate and to whom

#### 7. Revision History
| Date | Version | Author | Changes |
|---|---|---|---|
| {{DATE}} | 1.0 | {{NAME}} | Initial creation |

---

### Test Brief

**Purpose:** Define the parameters for an A/B test or experiment.

**Voice:** Scientific, precise, hypothesis-driven

**Required Sections:**

#### 1. Test Overview
```
Test Name: {{TEST_NAME}}
Account: {{ACCOUNT}}
Platform: {{PLATFORM}}
Author: {{NAME}}
Start Date: {{DATE}}
Estimated End Date: {{DATE}}
Status: Proposed / Approved / Running / Complete
```

#### 2. Hypothesis
- **Language pattern:** "We hypothesize that [CHANGE] will [IMPROVE/REDUCE] [METRIC] by [ESTIMATED_AMOUNT] because [RATIONALE]."
- State the null hypothesis: "The null hypothesis is that there is no significant difference in [METRIC] between the control and variant."

#### 3. Test Design
- **Variable:** What is being tested (one variable only)
- **Control:** Description of the control condition
- **Variant(s):** Description of each variant
- **Audience:** Who sees the test
- **Traffic split:** Percentage allocation per variant
- **Sample size required:** Minimum conversions per variant for significance
- **Duration estimate:** Expected time to reach sample size

#### 4. Success Criteria
- **Primary metric:** The metric that determines the winner
- **Minimum detectable effect:** The smallest improvement worth detecting
- **Significance threshold:** Confidence level required (typically 95%)
- **Secondary metrics:** Additional metrics to monitor

#### 5. Guardrails
- Metrics that must NOT degrade beyond a threshold
- "If [GUARDRAIL_METRIC] degrades by more than [THRESHOLD], pause the test."

#### 6. Analysis Plan
- When to check results (not before minimum sample is reached)
- Statistical method to use
- How to handle inconclusive results
- Decision framework: what action follows each possible outcome

---

## Language Patterns for Briefs

### Stating Objectives
- "The objective is to [VERB] [OUTCOME] by [METHOD]."
- "This initiative targets [KPI] of [VALUE] within [TIMEFRAME]."
- "Success is defined as [MEASURABLE_OUTCOME]."

### Providing Rationale
- "This approach is based on [DATA/EVIDENCE]."
- "We have selected this strategy because [REASON_1] and [REASON_2]."
- "Historical data from [SOURCE] indicates [FINDING], supporting this direction."

### Defining Scope
- "This brief covers [IN_SCOPE]. It does not cover [OUT_OF_SCOPE]."
- "The scope is limited to [BOUNDARIES] for this phase."
- "Phase 2 will address [DEFERRED_ITEMS]."

### Noting Assumptions
- "This plan assumes [ASSUMPTION]. If this changes, [IMPLICATION]."
- "Key assumption: [ASSUMPTION]. This will be validated by [DATE/METHOD]."

### Flagging Dependencies
- "This initiative depends on [DEPENDENCY] being completed by [DATE]."
- "Blocked by: [BLOCKER]. Expected resolution: [DATE]."

### Marking Open Questions
- "OPEN: [QUESTION] -- needs input from [PERSON] by [DATE]."
- "TBD: [ITEM] -- will be confirmed after [TRIGGER]."

---

## Formatting Standards for Documentation

### Headers and Sections
- Use H1 for document title only
- Use H2 for major sections
- Use H3 for subsections
- Use H4 sparingly for sub-subsections
- Number sections in strategy documents and SOPs for easy reference

### Tables
- Use tables for structured data: timelines, budgets, KPI targets, audience specs
- Always include a header row
- Keep tables to 6 columns or fewer

### Callouts
- **NOTE:** Additional context that is helpful but not critical
- **IMPORTANT:** Information that affects execution
- **CAUTION:** Risk of negative outcome if ignored
- **TBD:** Decision or information still pending

### Metadata Block
Every document should begin with:
```
Document: {{TITLE}}
Type: Campaign Brief / Strategy Document / SOP / Test Brief
Author: {{NAME}}
Date: {{DATE}}
Version: {{VERSION}}
Status: Draft / In Review / Approved / Active / Archived
Last Reviewed: {{DATE}}
```

### Version Control
- Increment version numbers: 1.0 (initial), 1.1 (minor update), 2.0 (major revision)
- Maintain a revision history table at the end of the document
- Mark superseded versions clearly: "ARCHIVED -- replaced by v2.0 on [DATE]"

---

## Audience-Specific Adaptations

### Internal Team Briefs
- Use shorthand and platform jargon freely
- Include technical setup details (pixel IDs, audience IDs, campaign structure)
- Focus on the "how" -- execution details
- Assign specific owners for each section or task

### Client-Facing Briefs
- Translate jargon or define on first use
- Focus on strategy and expected outcomes over tactical details
- Include approval checkpoints and feedback deadlines
- Frame recommendations as proposals: "We propose..." rather than "We will..."

### Cross-Functional Briefs (Creative, Analytics, Dev)
- Define paid-media-specific terms
- Focus on what the other team needs to deliver
- Include specs, deadlines, and examples
- Provide context for why the request matters: "This creative will be used for [PURPOSE], targeting [AUDIENCE], optimizing for [GOAL]."

---

## Brief Quality Checklist

- [ ] Document metadata is complete (title, author, date, version, status)
- [ ] Objective is specific, measurable, and time-bound
- [ ] All sections required for the document type are present
- [ ] Assumptions are stated explicitly
- [ ] Open questions are flagged with owners and deadlines
- [ ] Budget figures are included where relevant
- [ ] Success criteria are quantified
- [ ] Risks are identified with mitigation plans
- [ ] The document can be understood without verbal explanation
- [ ] Naming conventions and formatting standards are followed
- [ ] Version history is maintained
- [ ] Document has been reviewed by at least one other team member before distribution
