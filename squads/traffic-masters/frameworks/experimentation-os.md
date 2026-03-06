# Experimentation OS
> **Type**: Testing and Optimization Framework
> **Used by agents**: Performance Analyst, Media Buyer, Creative Analyst

## Overview
An operating system for running structured experiments in paid media and marketing. Covers hypothesis creation, variable isolation, sample size requirements, test duration, statistical significance, and decision frameworks. Transforms guessing into a disciplined science of learning.

## When to Use
- Before launching any test (creative, audience, landing page, offer)
- When deciding whether a test result is meaningful or noise
- Building a testing culture within a marketing team
- When campaigns are stagnant and need systematic improvement

## The Framework

### Step 1: Hypothesis Template
- Format: "If we [change X], then [metric Y] will [improve/decline] by [Z%], because [reasoning]."
- Example: "If we change the hook from question to statistic, then CTR will improve by 15%, because data-driven hooks outperform questions in this vertical."
- Every test must start with a written hypothesis. No random testing.

### Step 2: Variable Isolation
- Test ONE variable at a time: hook, image, audience, CTA, headline, etc.
- Control: The current best-performing version
- Variant: One change from the control
- If multiple variables change, you cannot attribute results to any single change

### Step 3: Sample Size
- Minimum: 100 conversions per variant (ideal: 300-500)
- For CTR tests: minimum 1,000 impressions per variant
- For conversion tests: minimum 100 conversions per variant
- Use sample size calculators before launching

### Step 4: Test Duration
- Minimum: 7 days (to capture day-of-week variation)
- Maximum: 28 days (to avoid external variable contamination)
- Do not end tests early based on early trends
- Account for learning phase in platform ad delivery (first 24-48 hours)

### Step 5: Statistical Significance
- Target: 95% confidence (p < 0.05) for strategic decisions
- Acceptable: 90% confidence (p < 0.10) for tactical adjustments
- Use proper statistical tests, not eyeball comparisons

### Step 6: Decision Framework
- **Ship**: Variant wins with >95% confidence — implement permanently
- **Iterate**: Variant shows promise (80-95%) — refine and retest
- **Kill**: Variant loses or no significant difference — discard and learn

## Key Concepts
- Every test is a learning opportunity, even failures
- Document learnings, not just results — build institutional knowledge
- Testing velocity matters: more tests = more learnings = faster improvement
- The biggest gains come from testing big ideas, not minor tweaks

## Decision Rules
- IF test reaches significance — apply the decision framework (ship/iterate/kill)
- IF test is inconclusive after maximum duration — kill and move on
- IF result contradicts hypothesis — investigate why before discarding
- IF external factors changed during test — consider re-running
- IF traffic is too low for significance — test bigger changes or combine metrics

## Integration
- Feeds into: Creative Testing Framework (structured creative experiments)
- Pairs with: Creative Iteration Loop (iterating on test learnings)
- Source data: Tracking Stack Standard (reliable data for test analysis)

## Output
- Hypothesis document for each planned test
- Sample size and duration calculations before launch
- Test result analysis with statistical confidence assessment
- Decision recommendation (ship/iterate/kill) with supporting data
- Learning log entry for organizational knowledge base
