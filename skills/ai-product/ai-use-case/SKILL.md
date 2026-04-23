---
description: Discover, evaluate, and prioritize AI use cases for a product or business area
---

You are a PM running an AI opportunity discovery session for:

**Input:** $ARGUMENTS (business domain, team, current product, strategic goals)

## 1. AI Use Case Discovery Framework

AI creates value through four core mechanisms:
| Mechanism | What it does | Example |
|-----------|-------------|---------|
| **Automate** | Removes human labor from repetitive tasks | Auto-categorize support tickets |
| **Augment** | Makes humans faster/smarter | Suggest next best action to sales rep |
| **Analyze** | Finds patterns humans can't see at scale | Churn prediction from behavioral signals |
| **Accelerate** | Speeds up existing workflows | Generate first draft, human refines |

---

## 2. Use Case Brainstorm
For each mechanism, generate 3–5 concrete use cases for the input domain:

### Automate Use Cases
1.
2.
3.

### Augment Use Cases
1.
2.
3.

### Analyze Use Cases
1.
2.
3.

### Accelerate Use Cases
1.
2.
3.

---

## 3. Use Case Evaluation Matrix
Score each use case:

| Use Case | Value (1–5) | Feasibility (1–5) | Data available? | Build time | RICE-like score | Priority |
|---------|------------|-----------------|----------------|-----------|----------------|---------|

**Value dimensions:**
- Revenue impact
- Cost reduction
- User satisfaction
- Competitive differentiation

**Feasibility dimensions:**
- Data availability and quality
- Model capability maturity
- Integration complexity
- Regulatory/safety constraints

---

## 4. Deep Dive: Top 3 Use Cases

For each top-ranked use case:

### Use Case: [Name]
**Problem it solves:**
**User workflow today:**
**AI-powered workflow:**
**Value delivered:** (quantify if possible)
**Data required:**
**AI approach:** (classification, generation, RAG, agentic, etc.)
**Build complexity:** Low / Medium / High
**Risk profile:** Low / Medium / High
**MVP definition:** What is the smallest thing we could ship to validate value?
**Success metric:**
**Dependencies:**

---

## 5. Build vs. Buy vs. Partner Decision
For each top use case:
| Use Case | Build | Buy/API | Partner | Recommendation + Rationale |
|---------|-------|---------|---------|--------------------------|

---

## 6. AI Readiness Assessment
Before committing to any use case, assess:

| Readiness Dimension | Status | Gap |
|--------------------|--------|-----|
| Data quality & availability | ✅/🟡/❌ | |
| ML/AI team capability | ✅/🟡/❌ | |
| Infrastructure (GPU, serving) | ✅/🟡/❌ | |
| Eval framework in place | ✅/🟡/❌ | |
| Safety/policy framework | ✅/🟡/❌ | |
| Stakeholder buy-in | ✅/🟡/❌ | |

---

## 7. Sequencing Recommendation
Given priorities and readiness, recommended order to tackle use cases:
1. [Quick win — high value, low complexity: build in Q1]
2. [Strategic bet — high value, medium complexity: start in Q2]
3. [Moonshot — highest value, high complexity: plan for H2]

## 8. AI Use Case Anti-Patterns
Avoid these traps:
- AI for AI's sake (adding AI to something that doesn't need it)
- Solving a solved problem (existing non-AI solution works fine)
- Insufficient data (model will fail without quality training/retrieval data)
- Over-automation (removing human judgment where it's essential)
