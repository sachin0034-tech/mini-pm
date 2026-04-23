---
description: Analyze a conversion funnel, identify drop-off points, and generate optimization hypotheses
---

You are a PM conducting a funnel analysis for:

**Input:** $ARGUMENTS (funnel stages, conversion data if available, product context)

## 1. Funnel Definition
Clearly define each stage — ambiguity in definitions causes bad analysis.

| Stage | Entry event | Exit event | What happens here |
|-------|-------------|------------|------------------|
| Stage 1 | | | |
| Stage 2 | | | |
| Stage 3 | | | |

## 2. Current Funnel Performance
| Stage | Users entering | Users exiting | Conversion rate | Industry benchmark |
|-------|---------------|--------------|----------------|-------------------|
| [Stage 1 → 2] | | | X% | |
| [Stage 2 → 3] | | | X% | |
| [Stage 3 → 4] | | | X% | |
| **End-to-end** | | | X% | |

## 3. Drop-off Analysis (Worst Stage First)
For each stage with >30% drop-off:

### Drop-off at [Stage N → N+1]
- **Current conversion:** X%
- **Users lost:** N per week
- **Revenue/value lost (if calculable):** $X per week
- **Likely causes:** (list hypothesis ranked by confidence)
  1. 
  2. 
  3. 
- **Evidence to gather:** (session recordings, surveys, support tickets)
- **Quick wins to test:**

## 4. Cohort Breakdown
Does conversion vary significantly by segment?
| Segment | Stage 1→2 | Stage 2→3 | Stage 3→4 | End-to-end |
|---------|---------|---------|---------|----------|
| Mobile | | | | |
| Desktop | | | | |
| New users | | | | |
| Returning | | | | |
| [Channel] | | | | |

## 5. Time-in-Stage Analysis
How long do users spend at each stage before converting or dropping?
| Stage | Median time | P90 time | Insight |
|-------|------------|---------|---------|

Users who take >2× median time at a stage are at high churn risk.

## 6. Optimization Opportunity Scorecard
| Stage | Current rate | Potential rate | Uplift | Reach | Priority |
|-------|-------------|---------------|--------|-------|---------|

**Priority formula:** (Potential − Current) × Reach → highest = attack first

## 7. Hypotheses to Test (A/B test candidates)
| Hypothesis | Stage | Expected lift | Effort | Test duration |
|-----------|-------|--------------|--------|--------------|

## 8. Funnel Monitoring Plan
| Metric | Alert threshold | Frequency | Owner |
|--------|----------------|-----------|-------|
| End-to-end conversion | Drops >5% WoW | Daily | PM |
| Worst stage conversion | Drops >10% | Daily | PM |
