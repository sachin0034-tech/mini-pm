---
description: Apply MoSCoW prioritization to a feature set with explicit rationale for each bucket
---

You are a PM facilitating a prioritization workshop using MoSCoW. Apply it to:

**Input:** $ARGUMENTS (list of features/requirements, release scope, constraints)

## MoSCoW Framework

| Category | Definition | Rule of thumb |
|----------|-----------|---------------|
| **Must Have** | Non-negotiable for the release to ship | Failing these = mission failure |
| **Should Have** | High value, but there are workarounds | Include if time allows |
| **Could Have** | Nice to have, limited impact if cut | First to cut when squeezed |
| **Won't Have (this time)** | Explicitly out of scope NOW | Commit to reviewing later |

**Constraint:** Must-Haves should consume no more than 60–70% of total capacity.

---

## Categorized Feature List

### MUST HAVE (P0 — non-negotiable)
| Feature | Why it's a Must | What breaks without it |
|---------|----------------|------------------------|
| | | |

### SHOULD HAVE (P1 — strong preference)
| Feature | Value delivered | Workaround if cut | Effort |
|---------|----------------|-------------------|--------|
| | | | |

### COULD HAVE (P2 — nice to have)
| Feature | Incremental value | Effort | Cut-decision criteria |
|---------|-----------------|--------|----------------------|
| | | | |

### WON'T HAVE THIS RELEASE (Committed Backlog)
| Feature | Why deferred | Target horizon | Owner |
|---------|-------------|---------------|-------|
| | | | |

---

## Capacity Sanity Check
| Category | Feature count | Estimated effort | % of total capacity |
|----------|--------------|-----------------|---------------------|
| Must Have | | | Should be ≤70% |
| Should Have | | | |
| Could Have | | | |
| **Total** | | | **100%** |

## Challenge Round
For each Must Have: answer "What happens if we ship without this?"
- If the answer is "not much" → downgrade to Should Have
- If the answer is "the product fails its purpose" → keep it

## Must Have Risks
| Must Have | Risk if it slips | Mitigation |
|----------|-----------------|-----------|

## Communication Plan for Won't Haves
Who needs to know, and how will you communicate the cut decisions?
