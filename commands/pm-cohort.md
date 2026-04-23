---
description: Design and interpret a cohort retention analysis to understand user behavior over time
---

You are a PM conducting cohort analysis for:

**Input:** $ARGUMENTS (product, metric to analyze, time period, any data available)

## 1. Cohort Analysis Design

**Cohort type to use:**
- **Acquisition cohort:** Users who joined in the same time period — most common
- **Behavioral cohort:** Users who completed the same action — for feature analysis
- **Size cohort:** Users in the same company-size tier — for B2B

**Recommended for this context:** [Type + rationale]

## 2. Retention Curve Template
(Fill with actual data or estimate from benchmarks)

| Cohort | Day 1 | Day 7 | Day 14 | Day 30 | Day 60 | Day 90 | Asymptote |
|--------|-------|-------|--------|--------|--------|--------|-----------|
| Jan cohort | 100% | X% | X% | X% | X% | X% | X% |
| Feb cohort | 100% | X% | X% | X% | X% | X% | X% |
| Mar cohort | 100% | X% | X% | X% | X% | X% | X% |

**What to look for:**
- **Improving cohorts** (newer > older at same period): product is getting better
- **Degrading cohorts** (newer < older): quality or ICP fit is worsening
- **Retention asymptote > 0%:** you have a retained user base — grow it
- **Retention asymptote ≈ 0%:** fundamental product-market fit problem

## 3. Retention Benchmarks by Product Type
| Product type | D1 | D7 | D30 | Notes |
|-------------|----|----|-----|-------|
| Consumer social | 25–35% | 10–20% | 5–10% | |
| Consumer utility | 35–50% | 20–35% | 10–20% | |
| B2B SaaS | 60–80% | 50–70% | 40–60% | |
| Enterprise | 85–95% | 75–90% | 65–80% | |
| Marketplace | 20–40% | 10–25% | 8–15% | |

## 4. Retention Drivers Analysis
For cohorts with better retention, what's different about them?
| Variable | High-retention cohorts | Low-retention cohorts | Insight |
|---------|----------------------|----------------------|---------|
| Acquisition channel | | | |
| Activation milestone hit | | | |
| Feature used in week 1 | | | |
| Onboarding path taken | | | |
| Company size (B2B) | | | |

## 5. Magic Moment Identification
The "magic moment" is the action/event most correlated with long-term retention.

**Method:** Find the action in the first 7 days that has the highest correlation with D30 retention.
**Hypothesis for this product:** [What action is likely the magic moment and why?]

## 6. Intervention Points
| Retention phase | Drop-off signal | Intervention | Expected lift |
|----------------|----------------|-------------|--------------|
| D0–D1 | User doesn't complete onboarding | Trigger email/in-app | |
| D1–D7 | No return visit | Re-engagement push | |
| D7–D30 | Usage declining | Feature discovery prompt | |
| D30+ | Engagement drop | Win-back campaign | |

## 7. Revenue Cohort Analysis (if applicable)
Layer revenue on top of retention:
| Cohort | M1 ARPU | M3 ARPU | M6 ARPU | LTV estimate |
|--------|---------|---------|---------|-------------|

## 8. Key Questions This Analysis Answers
1. Is our product retaining users better over time?
2. Which acquisition channels bring the most retained users?
3. What is the magic moment we should push new users toward?
4. Where in the lifecycle is churn concentrated?
