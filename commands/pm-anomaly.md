---
description: Investigate a metric anomaly with structured diagnostic framework and root cause analysis
---

You are a PM investigating a metric anomaly for:

**Input:** $ARGUMENTS (metric that moved, magnitude of change, when it happened, product context)

## 1. Anomaly Characterization
Before diagnosing, characterize the anomaly precisely:

| Dimension | Description |
|-----------|------------|
| **Metric affected** | |
| **Direction of change** | Up / Down |
| **Magnitude** | X% change |
| **Start time** | |
| **Duration** | Ongoing / Resolved |
| **Affected segments** | All users / [specific segment] |
| **Severity** | P0: Critical / P1: High / P2: Monitor |

## 2. First 30-Minute Checklist (Is this real?)
Before investigating causes, rule out data issues:
- [ ] Is the tracking code firing correctly? (check event logs)
- [ ] Is there a data pipeline lag or backfill in progress?
- [ ] Did the definition or query for this metric change?
- [ ] Is the sample size too small for this to be statistically significant?
- [ ] Is this a known seasonal pattern (weekend, holiday, end of month)?

**If any are true:** label as "data artifact" and stop. Fix instrumentation.

## 3. Diagnostic Tree — Top-Down
Start broad, narrow down:

```
Metric changed
├── Was there a product change / deploy?
│   ├── Yes → Which feature? Which users were affected?
│   └── No → External cause?
│       ├── Platform/infrastructure issue?
│       ├── Competitor event?
│       └── Market/seasonal factor?
├── Which segment is driving it?
│   ├── New vs. returning users?
│   ├── Mobile vs. desktop?
│   ├── Geographic region?
│   └── Acquisition channel?
└── Which funnel stage is affected?
```

## 4. Root Cause Hypotheses (Ranked by Probability)
| # | Hypothesis | Evidence for | Evidence against | How to validate |
|---|-----------|-------------|-----------------|----------------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

## 5. Immediate Actions
| Action | Owner | ETA | Purpose |
|--------|-------|-----|---------|
| [Page on-call if P0] | | Immediate | |
| [Validate instrumentation] | | 30 min | |
| [Segment analysis] | | 1 hour | |
| [Check deploy log] | | 15 min | |

## 6. Root Cause Identified
*Fill in after investigation:*
- **Root cause:**
- **Why it happened:**
- **Why we didn't catch it sooner:**

## 7. Resolution
- **Fix:**
- **ETA to resolution:**
- **Rollback option:**
- **Monitoring to confirm recovery:**

## 8. Prevention — Post-Mortem Actions
| Action | Owner | Priority | Due |
|--------|-------|---------|-----|
| Add alert for [specific signal] | | | |
| Improve logging for [component] | | | |
| Add test coverage for [scenario] | | | |
