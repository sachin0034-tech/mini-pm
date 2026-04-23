---
description: Plan a sprint with goal setting, capacity allocation, risk assessment, and success criteria
---

You are a PM running sprint planning for:

**Input:** $ARGUMENTS (team, sprint number/dates, available velocity, candidate stories)

## 1. Sprint Context
- **Sprint:** [Number] | **Dates:** [Start] → [End]
- **Duration:** [1 or 2 weeks]
- **Team size:** [N engineers + PM + designer]
- **Velocity (last 3 sprints avg):** [X story points]
- **Capacity this sprint:** [adjusted for PTO, meetings, etc.]

## 2. Sprint Goal (one sentence)
The sprint goal is NOT a list of features — it's a customer-outcome statement.

**Format:** "By [end of sprint], [user type] will be able to [do X] so that [outcome]."

Write 2 options and recommend one.

## 3. Capacity Planning
| Team Member | Role | Days available | Point capacity | Notes |
|------------|------|---------------|---------------|-------|
| | | | | PTO, other meetings |

**Total available capacity:** [X points]
**Target commitment:** [~85% of capacity = Y points] *(leave buffer for bugs/interrupts)*

## 4. Story Selection

| Story | Points | Priority | Fits sprint goal? | Risk | Owner |
|-------|--------|---------|------------------|------|-------|
| | | P0/P1/P2 | ✅/❌ | L/M/H | |

**Total committed:** [X points]

## 5. Sprint Risk Register
| Risk | Probability | Impact | Mitigation |
|------|------------|--------|-----------|
| [Dependency not resolved] | | | |
| [Key person absent] | | | |
| [Technical unknown] | | | |

## 6. Definition of Done (Sprint-Level)
- [ ] All acceptance criteria met
- [ ] Code reviewed and merged
- [ ] Unit tests passing (coverage ≥ threshold)
- [ ] No new P0/P1 bugs introduced
- [ ] Demo-able in sprint review
- [ ] Docs updated if user-facing

## 7. Sprint Ceremonies Plan
| Ceremony | When | Duration | Owner |
|----------|------|---------|-------|
| Daily standup | Daily [time] | 15 min | Team |
| Mid-sprint check | Day 5 | 30 min | PM |
| Sprint review | Last day | 60 min | PM |
| Retrospective | Last day | 45 min | Scrum Master |

## 8. Sprint Success Criteria
How will we know this sprint was successful?
| Metric | Target |
|--------|--------|
| Stories completed | [X/Y committed] |
| Sprint goal achieved | Yes/No |
| Bugs introduced | ≤ [N] |
| Demo delivered | ✅ |

## 9. Dependencies Requiring Unblocking This Sprint
| Dependency | Blocked story | Who to contact | Deadline |
|-----------|--------------|---------------|---------|
