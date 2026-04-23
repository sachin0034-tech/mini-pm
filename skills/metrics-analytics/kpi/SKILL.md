---
description: Design a product KPI dashboard with metric hierarchy, visualizations, and review rituals
---

You are a PM designing a KPI dashboard system for:

**Input:** $ARGUMENTS (product, audience for the dashboard, business context)

## 1. Dashboard Philosophy
A dashboard is only useful if it drives decisions. Before designing it, answer:
- **Primary audience:** Who reads this and what decisions do they make from it?
- **Cadence:** When is it reviewed?
- **Action threshold:** What would cause someone to act based on what they see?

## 2. Dashboard Architecture (Layer Cake)

### Dashboard 1: Executive Pulse (Leadership, weekly, 60-second read)
4–6 metrics max. Each should be:
- Directional (up/down vs. last period)
- With context (target, benchmark, trend)

| Metric | Current | vs. Last Week | vs. Target | vs. Benchmark | RAG Status |
|--------|---------|--------------|-----------|--------------|-----------|
| | | | | | 🟢🟡🔴 |

### Dashboard 2: Product Health (PM + Eng, daily)
| Metric | Today | WoW% | MoM% | YoY% | Alert |
|--------|-------|------|------|------|-------|
| DAU | | | | | if <X |
| Activation rate | | | | | if <X% |
| D7 retention | | | | | if <X% |
| Feature adoption | | | | | if <X% |
| Error rate | | | | | if >X% |

### Dashboard 3: Feature Metrics (PM, per-feature, weekly)
| Feature | Weekly actives | Adoption % | Usage frequency | Satisfaction | Trend |
|---------|---------------|------------|-----------------|-------------|-------|

## 3. Metric Definitions (Prevent Dashboard Disputes)
Every metric on a dashboard must have a canonical definition:
| Metric | Exact formula | Inclusions | Exclusions | Data source |
|--------|--------------|-----------|-----------|------------|

## 4. Visualization Recommendations
| Metric type | Best visualization | Why |
|------------|------------------|-----|
| Trend over time | Line chart | Shows direction |
| Comparison across segments | Bar chart | Easy ranking |
| Part of a whole | Pie only if <5 slices | |
| Correlation | Scatter plot | Relationship |
| Funnel | Waterfall/funnel | Shows drop-off |
| Cohort retention | Heatmap | Pattern visibility |

## 5. Alert System Design
| Metric | Green (normal) | Yellow (watch) | Red (act now) | Who gets notified |
|--------|---------------|---------------|--------------|------------------|

## 6. Dashboard Review Ritual
| Audience | Cadence | Duration | Format | Owner |
|----------|---------|---------|--------|-------|
| Team standup | Daily | 5 min | Slack | PM |
| PM weekly review | Monday | 30 min | Live dashboard | PM |
| Leadership review | Monthly | 15 min | Slides | PM |

## 7. Common Dashboard Anti-Patterns to Avoid
- Too many metrics (max 6 per view — cognitive overload kills action)
- Vanity metrics (page views without context)
- Missing context (a number without target/benchmark/trend is meaningless)
- Stale data (if refresh is >24h, say so prominently)
- No owner (every metric needs someone responsible for it)
