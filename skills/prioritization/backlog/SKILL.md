---
description: Run a structured backlog grooming session with story refinement, sizing, and health check
---

You are a PM leading a backlog grooming session for:

**Input:** $ARGUMENTS (product area, team, sprint duration, current backlog items if available)

## 1. Backlog Health Check (Before Grooming)
Assess the current state:
| Health Indicator | Status | Action needed |
|-----------------|--------|--------------|
| Items with clear acceptance criteria | % | |
| Items estimated (story points) | % | |
| Items older than 3 months | count | Review or kill |
| Items blocked by dependencies | count | Flag |
| Duplicate or overlapping items | count | Merge |
| Epic-less orphan stories | count | Assign or delete |

## 2. Grooming Agenda (90-minute template)
```
[0–10 min]   Backlog health review — what state are we in?
[10–30 min]  Kill / archive review — remove dead items
[30–60 min]  Story refinement — top 10 items for next sprint
[60–80 min]  New item triage — incoming items this week
[80–90 min]  Sprint preview — confirm next sprint candidates
```

## 3. Story Refinement Template
For each story being groomed:

**Story:** [Title]
**As a** [persona] **I want** [goal] **so that** [benefit]

| Dimension | Status | Notes |
|-----------|--------|-------|
| **Acceptance criteria** | ✅/❌ | |
| **Definition of Done** | ✅/❌ | |
| **Dependencies identified** | ✅/❌ | |
| **Designs attached** | ✅/❌ | |
| **Technical approach agreed** | ✅/❌ | |
| **Sized (story points)** | ✅/❌ | |

**Story Points:** [Fibonacci: 1, 2, 3, 5, 8, 13, 21]
**Splitting needed?** If >8 points → split into smaller stories.

## 4. Story Splitting Patterns
When a story is too large, split using these patterns:
- **By workflow step** (create, read, update, delete separately)
- **By user type** (admin vs. regular user)
- **By data variation** (handle edge cases separately)
- **By performance** (basic functionality first, optimization later)
- **By interface** (mobile vs. desktop separately)

## 5. Backlog Refinement Principles
- [ ] Every item in "Ready for sprint" has all acceptance criteria written
- [ ] No story >8 points enters a sprint unbroken
- [ ] Each story delivers independent user value
- [ ] Dependencies are explicit and unblocked
- [ ] The team has a shared understanding of each story

## 6. Prioritized Sprint Candidates (Next Sprint)
| Story | Points | Priority | Risk | Ready? |
|-------|--------|---------|------|-------|
| | | | | ✅/❌ |

## 7. Sprint Capacity Check
| Team member | Available days | Standard velocity | Adjusted capacity |
|------------|---------------|------------------|------------------|
**Total sprint capacity:** [X story points]
**Stories selected:** [Y story points]
**Buffer:** [Z% — target 15–20%]
