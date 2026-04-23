---
description: Map feature and team dependencies, identify critical path, and surface sequencing risks
---

You are a PM mapping dependencies across a complex initiative for:

**Input:** $ARGUMENTS (initiative, features, teams involved)

## 1. Dependency Inventory
List every known dependency. For each:

| ID | Initiative/Feature | Depends On | Type | Dependency Owner | Due Date | Status |
|----|-------------------|------------|------|-----------------|---------|--------|
| D-01 | | | | | | |

**Dependency types:**
- **Technical:** requires code/infrastructure from another team
- **Data:** requires data pipeline or schema from another team
- **Decision:** waiting on a product/strategy decision
- **External:** vendor, partner, regulatory
- **Sequential:** Feature B can't start until Feature A ships

## 2. Dependency Graph (Text Format)
```
[Your Initiative]
├── Requires: [Feature A] ← owned by [Team X]
│   └── [Feature A] requires: [Infrastructure Y]
├── Requires: [Data pipeline Z] ← owned by [Team W]
├── Blocked by: [Legal review] ← ETA [date]
└── Sequential: [Phase 1] must ship before [Phase 2]
```

## 3. Critical Path Analysis
Identify the longest dependency chain — this determines your earliest possible ship date.

**Critical Path:**
[Step 1] → [Step 2] → [Step 3] → ... → [Ship Date]

**Critical path duration:** [X weeks]
**Earliest ship date:** [Date based on critical path]

## 4. Dependency Risk Matrix
| Dependency | Probability of slipping | Impact on launch | Risk score | Mitigation |
|-----------|------------------------|-----------------|-----------|-----------|
| D-01 | H/M/L | H/M/L | | |

## 5. Cross-Team Alignment Status
| Team | What we need | Committed? | Escalation needed? |
|------|-------------|------------|-------------------|
| | | ✅/🟡/❌ | |

## 6. Sequencing Recommendation
Given the dependencies, what is the optimal order to build and ship?

**Recommended sequence:**
1. [First: unblocks the most downstream work]
2. [Second:]
3.
4.

## 7. Risk Mitigation Plan
For each high-risk dependency:
| Dependency | Plan A (resolve) | Plan B (workaround) | Plan C (descope) |
|-----------|-----------------|--------------------|--------------------|

## 8. Weekly Dependency Check Template
For each active dependency, answer every Monday:
- Is it still on track?
- Has the owner confirmed the timeline?
- Is there a new blocker?
- Do we need to escalate?
