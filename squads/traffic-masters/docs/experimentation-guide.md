# Experimentation Guide

## Purpose
How to design, run, and learn from experiments in the traffic squad.

## Experiment Process

### 1. Hypothesis Formation
- Use the formula: "If [change], then [metric] will [direction] by [amount] because [reason]"
- Reference `lib/components/test-hypothesis-component.md`

### 2. Test Design
- Isolate one variable per test
- Define primary metric and success criteria
- Calculate required sample size
- Set test duration (minimum 7 days)

### 3. Execution
- Use platform-native split testing when available
- Ensure equal budget allocation between variants
- Do not make changes during the test
- Monitor for data quality issues

### 4. Analysis
- Wait for statistical significance (95% confidence)
- Check `lib/utilities/statistical-significance-guide.md`
- Verify results across segments (device, day, audience)
- Document in `data/registries/experiments-registry.yaml`

### 5. Action
- Implement winner across relevant campaigns
- Plan next iteration based on learnings
- Update `data/registries/lessons-learned-registry.yaml`

## What to Test (Priority Order)
1. **Hooks** — Highest impact on performance
2. **Angles** — Changes the core message
3. **Creative format** — Video vs static vs carousel
4. **Audiences** — New segments and targeting
5. **Bid strategy** — Auto vs manual approaches
6. **Landing pages** — Conversion rate optimization

## Test Velocity Target
- Minimum 2 experiments per week
- Track win rate (target: 30-40%)
- Maintain experiment backlog of 10+ ideas
