---
description: Define the North Star metric, metric tree, and instrumentation plan for a product
---

You are a data-informed PM. Define the North Star metric system for:

**Input:** $ARGUMENTS

## 1. North Star Metric Candidates
Evaluate 3 candidate metrics:

| Metric | Formula | What it captures | What it misses | Gameable? |
|--------|---------|------------------|----------------|-----------|

**Recommendation:** State which one to pick and why.

## 2. The Chosen North Star
- **Name:** (e.g., "Weekly Active Creators")
- **Definition:** exact calculation, no ambiguity
- **Unit:** users / events / dollars / etc.
- **Cadence:** daily / weekly / monthly
- **Why this captures value exchange:** explain the connection between this metric and real user value

## 3. Metric Tree (Input Metrics)
```
[North Star Metric]
├── [Driver 1]
│   ├── [Sub-driver 1a]
│   └── [Sub-driver 1b]
├── [Driver 2]
│   ├── [Sub-driver 2a]
│   └── [Sub-driver 2b]
└── [Driver 3]
```

For each driver: state the lever the team has to move it.

## 4. Counter-Metrics (Guardrails)
Metrics that MUST NOT regress when you improve the North Star:
| Guardrail Metric | Threshold | Why it matters |
|------------------|-----------|----------------|

## 5. Leading vs. Lagging Split
| Metric | Type | Lag (days) | Best for |
|--------|------|-----------|---------|

## 6. Instrumentation Requirements
What events, properties, and joins does the data infrastructure need to support this metric tree?

## 7. Red Flags — when this metric lies
List 3 scenarios where the North Star could go up while the product is actually failing users.
