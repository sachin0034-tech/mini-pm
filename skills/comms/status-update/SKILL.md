---
description: [SCHEDULER] Generate and schedule weekly product status updates for stakeholders
---

You are setting up a recurring weekly product status update system for:

**Input:** $ARGUMENTS (product area, team, stakeholder audience, key metrics to include)

## Status Update Template

**[Product Area] — Week of [AUTO-DATE]**
*Prepared by: [PM] | Audience: [Stakeholders from input]*

---

### 🎯 This Week's Headline
[One sentence: the most important thing that happened or is happening]

---

### ✅ Shipped / Completed
| Item | Impact | Notes |
|------|--------|-------|
| | | |

### 🔨 In Progress
| Item | Status | ETA | Blocker? |
|------|--------|-----|---------|
| | 🟢/🟡/🔴 | | |

### 📊 Metrics Pulse
| Metric | This Week | vs. Last Week | vs. Target | Status |
|--------|-----------|--------------|-----------|--------|
| [North Star] | | | | 🟢/🟡/🔴 |
| [Key leading metric] | | | | |
| [Retention] | | | | |

### ⚠️ Risks & Blockers
| Risk/Blocker | Impact | Owner | Escalation needed? |
|-------------|--------|-------|-------------------|

### 📅 Next Week Focus
1. [Top priority]
2.
3.

### 🔮 Looking Ahead (2–4 weeks)
Key decisions, milestones, or dependencies coming up.

### 💬 Asks / FYIs for Stakeholders
- **Ask:** [Specific thing you need]
- **FYI:** [Heads up that needs no action]

---

**Format notes:**
- Target length: fits in one email / Slack message
- No acronyms without spelling out
- Lead with outcomes, not activities ("shipped X that reduced Y by Z%" not "worked on X")

---

## Schedule Weekly Automated Status Update

Use the CronCreate tool to schedule this status update every Friday at 4:00 PM:

**Cron schedule:** `0 16 * * 5` (Every Friday at 4:00 PM)

**Prompt:** "Generate the weekly status update for [product area from input]. Include: top 3 wins, blockers, metric pulse from the monitoring dashboard, next week priorities. Send to [stakeholder audience from input]."

Confirm:
1. Schedule is registered
2. Next 4 run dates
3. Remind PM to review before auto-send (or confirm auto-send if desired)
