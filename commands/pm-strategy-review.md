---
description: [SCHEDULER] Set up a recurring weekly product strategy review with automated prompts
---

You are setting up a recurring weekly strategy review. 

**Input:** $ARGUMENTS (product area, team context, key OKRs to track)

First, generate the strategy review template. Then schedule the recurring weekly review using the CronCreate tool.

## Weekly Strategy Review Template

**Week of:** [AUTO-FILLED]
**Product Area:** $ARGUMENTS

---

### 1. OKR Pulse (5 min)
For each active OKR, rate progress: 🟢 On track | 🟡 At risk | 🔴 Off track

| OKR | Status | Delta from last week | Blocker |
|-----|--------|---------------------|---------|

### 2. Top 3 Wins This Week
1.
2.
3.

### 3. Top 3 Blockers / Risks
| Blocker | Impact | Owner | Resolution path |
|---------|--------|-------|----------------|

### 4. Competitive & Market Signals
Any new competitor moves, customer feedback, or market shifts this week?

### 5. Decisions Made
| Decision | Rationale | Who decided | Date |
|----------|-----------|-------------|------|

### 6. Decisions Needed Next Week
| Decision | Options | Decision owner | Deadline |
|----------|---------|----------------|---------|

### 7. Focus for Next Week (Top 3 Priorities)
1.
2.
3.

### 8. One Strategic Risk to Watch
The thing most likely to knock the strategy off course right now.

---

After generating this template, use the CronCreate tool to schedule this review prompt to run every Monday at 9:00 AM:

**Cron schedule:** `0 9 * * 1` (Every Monday at 9 AM)
**Prompt to run:** "Run /pm-strategy-review for [product area from input]. Pull current OKR status, recent decisions, and blockers. Generate the filled-out weekly strategy review."

Confirm the schedule is set and show the next 4 scheduled run dates.
