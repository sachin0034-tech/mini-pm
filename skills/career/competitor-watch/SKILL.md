---
description: [LOOP] Set up a continuous competitor monitoring loop with structured intelligence reports
---

You are setting up a continuous competitor intelligence monitoring system for:

**Input:** $ARGUMENTS (product area, competitors to track, intelligence categories, team context)

## Step 1: Competitor Intelligence Framework

Define what to monitor for each competitor:

| Intelligence Category | Why it matters | Sources |
|----------------------|---------------|---------|
| **Product releases** | New features may require response | Changelog, ProductHunt, press |
| **Pricing changes** | Directly affects win/loss rate | Pricing pages, G2, Reddit |
| **Hiring signals** | Predicts investment areas | LinkedIn, job boards |
| **Funding / acquisitions** | Signals strategy shifts | Crunchbase, TechCrunch |
| **Customer sentiment** | Reveals exploitable weaknesses | G2, Trustpilot, Twitter |
| **Executive moves** | Signals strategy changes | LinkedIn |
| **Partnership announcements** | New distribution threats | Press releases |

---

## Step 2: Competitor Watch Configuration

**Competitors to monitor:**
(Extracted from input)

| Competitor | Priority | Key products | Primary threat area |
|-----------|---------|-------------|--------------------| 

---

## Step 3: Intelligence Report Template

**Competitor Intelligence Report**
**Period:** [Week of DATE]
**Prepared by:** Claude

### 🔴 High-Priority Signals (Requires PM attention this week)
| Competitor | Signal | Source | Implication | Recommended Response |
|-----------|--------|--------|-------------|---------------------|

### 🟡 Monitor (Watch but no immediate action)
| Competitor | Signal | Source | Context |
|-----------|--------|--------|---------|

### 🟢 Background Intelligence (FYI)
| Competitor | Update | Notes |
|-----------|--------|-------|

### Trend Analysis
Over the past 30 days, here's the strategic direction each competitor appears to be taking:

### Opportunities Surfaced This Week
Based on competitor moves, what gaps or moments should we exploit?
1.
2.

### Threats to Prioritize
Based on competitor moves, what defensive actions should we take?
1.
2.

---

## Step 4: Set Up the Monitoring Loop

Use the loop skill to run competitor monitoring on a regular cadence:

**Invoke:** `/loop 1w /pm-competitor-watch [same input arguments]`

This will:
- Run the competitor intelligence check every 7 days
- Generate a new intelligence report each cycle
- Flag any high-priority signals for immediate PM review
- Build a running log of competitive moves over time

**Alternatively**, use CronCreate for a fixed weekly schedule:
**Cron:** `0 9 * * 2` (Every Tuesday at 9 AM)
**Prompt:** "Run competitor intelligence check for [competitors from input]. Search for new product releases, pricing changes, hiring signals, and customer sentiment shifts. Generate the competitor intelligence report. Flag anything that requires a product response this week."

---

## Step 5: Competitive Response Playbook

Pre-define responses to common competitive scenarios so the team can move fast:

| Scenario | Trigger | Response plan | Owner | SLA |
|---------|---------|--------------|-------|-----|
| Competitor ships feature we're building | Feature parity threat | Accelerate timeline, evaluate differentiation | PM | 48h |
| Competitor cuts price >20% | Win/loss rate drops | Pricing review meeting | PM + Finance | 1 week |
| Competitor acquires a key partner | Distribution threat | Partner strategy review | PM + BD | 2 weeks |
| Competitor announces major new feature | Roadmap impact | Roadmap review | PM | 1 week |

---

**Monitoring active.** Report frequency: Weekly. First report will be generated on the next scheduled run.
