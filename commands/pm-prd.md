---
description: Generate a complete, senior-quality Product Requirements Document from a brief
---

You are a Principal PM at a top-tier tech company. Generate a full PRD for the following product or feature:

**Input:** $ARGUMENTS

Produce the PRD using this exact structure:

---

## 1. Problem Statement
- What problem are we solving and for whom?
- What is the cost of NOT solving it (user pain + business impact)?
- What evidence do we have this problem exists? (data, research, support tickets)

## 2. Goals & Non-Goals
- **Goals:** 3–5 crisp, measurable outcomes we want to achieve
- **Non-Goals:** explicit list of what is out of scope and why

## 3. User Personas
For each persona:
- **Name / Role**
- **Context** (what they're doing when they hit this problem)
- **Jobs to Be Done** (functional + emotional)
- **Current workaround** (and why it's insufficient)

## 4. User Stories
Write 5–8 user stories in the format:
> As a [persona], I want [capability] so that [outcome].
Mark each as P0 / P1 / P2.

## 5. Success Metrics
| Metric | Baseline | Target | Measurement Method |
|--------|----------|--------|--------------------|
| Primary (North Star) | | | |
| Secondary (leading) | | | |
| Guardrail (don't break) | | | |

## 6. Requirements
### Functional Requirements
- List each requirement with a unique ID (FR-01, FR-02…)
- Tag each: P0 (launch blocker) / P1 (launch target) / P2 (nice-to-have)

### Non-Functional Requirements
- Performance, reliability, security, compliance, accessibility

## 7. Design Considerations
- Key UX principles
- Accessibility requirements
- Edge cases the design must handle

## 8. Technical Considerations
- Architecture constraints
- API / data model changes
- Dependencies on other teams or systems
- Risks and mitigations

## 9. Launch Plan
- Alpha / Beta / GA criteria
- Rollout strategy (% ramp, flags, regions)
- Rollback plan

## 10. Open Questions
| # | Question | Owner | Due Date |
|---|----------|-------|----------|

## 11. Appendix
- Links to research, data, mockups, competitive analysis

---

Make every section specific, not generic. If the input lacks detail, make explicit assumptions labeled **[ASSUMPTION]** and flag them in Open Questions.
