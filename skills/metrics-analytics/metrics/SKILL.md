---
description: Design a comprehensive product metrics framework with hierarchy, instrumentation, and alerting
---

You are a PM designing a metrics framework for:

**Input:** $ARGUMENTS (product, stage — early/growth/mature, business model)

## 1. Metrics Philosophy
State the guiding principles for how this team will use metrics:
- Are we optimizing for growth, retention, revenue, or efficiency?
- Which metrics are leading vs. lagging?
- What is the review cadence?

## 2. Metrics Hierarchy

### L1: Business Metrics (CEO-level, monthly)
| Metric | Definition | Current | Target | Owner |
|--------|-----------|---------|--------|-------|
| Revenue / ARR | | | | |
| Customer count | | | | |
| Net Revenue Retention | | | | |

### L2: Product Health Metrics (VP-level, weekly)
| Metric | Definition | Current | Target | Owner |
|--------|-----------|---------|--------|-------|
| DAU / WAU / MAU | | | | |
| Activation rate | | | | |
| Retention (D1/D7/D30) | | | | |
| NPS / CSAT | | | | |

### L3: Feature Metrics (PM-level, daily)
| Feature | Adoption rate | Engagement depth | Drop-off point | Owner |
|---------|--------------|-----------------|---------------|-------|
| | | | | |

## 3. HEART Framework (for UX quality)
| Dimension | Definition | Signal | Metric |
|-----------|-----------|--------|--------|
| **Happiness** | Subjective satisfaction | Survey, NPS | |
| **Engagement** | Depth of interaction | Events per session | |
| **Adoption** | New users of a feature | % users activating | |
| **Retention** | Users coming back | D7/D30 retention | |
| **Task Success** | Can they complete it? | Completion rate | |

## 4. Funnel Metrics
Map the full funnel from acquisition to expansion:
| Stage | Definition | Metric | Benchmark | Current |
|-------|-----------|--------|-----------|---------|
| Acquisition | | | | |
| Activation | | | | |
| Engagement | | | | |
| Retention | | | | |
| Revenue | | | | |
| Referral | | | | |

## 5. Counter-Metrics (Guardrails)
Metrics that CANNOT regress as you optimize for the North Star:
| Guardrail | Threshold | What it protects |
|-----------|-----------|-----------------|
| Support ticket volume | ≤ X/week | Quality |
| p99 latency | ≤ Xms | Performance |
| Churn rate | ≤ X% | Retention |

## 6. Instrumentation Requirements
| Metric | Event to log | Properties needed | Data freshness needed |
|--------|-------------|------------------|----------------------|

## 7. Alerting Thresholds
| Metric | Green | Yellow | Red | Who gets paged |
|--------|-------|--------|-----|----------------|

## 8. Metrics Review Cadence
| Audience | Frequency | Metrics reviewed | Format |
|----------|-----------|-----------------|--------|
| Team | Daily | L3 | Slack alert |
| PM + Eng | Weekly | L2 + L3 | Dashboard |
| Leadership | Monthly | L1 + L2 | Slides |
