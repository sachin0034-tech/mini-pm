---
description: [SCHEDULER] Set up a daily automated metrics monitoring routine with threshold alerts
---

You are setting up a daily automated metrics monitoring system for:

**Input:** $ARGUMENTS (product name, key metrics to monitor, alert thresholds, Slack channel or notification preference)

## Step 1: Metrics Monitoring Configuration

Define the metrics to monitor daily:

| Metric | Baseline (7-day avg) | Yellow threshold | Red threshold | Data source |
|--------|---------------------|-----------------|--------------|------------|
| DAU | | <10% WoW drop | <20% WoW drop | |
| Activation rate | | <5% drop | <15% drop | |
| D7 retention | | <3% drop | <10% drop | |
| Error rate | | >10% increase | >25% increase | |
| [Custom metric] | | | | |

## Step 2: Daily Check Template

**Date:** [AUTO]
**Product:** $ARGUMENTS

### Metric Status
| Metric | Yesterday | 7-day avg | WoW change | Status |
|--------|-----------|-----------|-----------|--------|
| | | | | 🟢/🟡/🔴 |

### Anomalies Detected
List any metric outside normal thresholds with the anomaly investigation checklist triggered.

### Notable Events Yesterday
- Deploys / feature flags changed:
- Support ticket spikes:
- Competitor news:

### Action Required
| Metric | Issue | Owner | Priority |
|--------|-------|-------|---------|

---

## Step 3: Schedule Daily Automated Monitoring

Use the CronCreate tool to schedule this metrics monitoring routine:

**Cron schedule:** `0 8 * * 1-5` (Every weekday at 8:00 AM)

**Automated prompt:** "Run daily metrics check for [product from input]. Pull latest metric values, compare to 7-day averages and defined thresholds. Flag any anomalies and trigger pm-anomaly analysis for anything in red status. Output the daily monitoring report."

After scheduling, confirm:
1. The cron job is registered
2. Show the next 5 scheduled run times
3. Confirm what action will be taken if a red-threshold metric is detected

## Step 4: Alert Escalation Path
- **Green:** No action, log for weekly review
- **Yellow:** PM reviews during morning standup
- **Red:** Page PM immediately + trigger pm-anomaly investigation
