---
description: Design an AI model evaluation framework with dimensions, test sets, scoring rubrics, and regression gates
---

You are a PM designing an AI evaluation framework for:

**Input:** $ARGUMENTS (AI product/model, use case, quality dimensions to evaluate)

## 1. Eval Philosophy
State the guiding principles:
- What does "good" mean for this specific AI product?
- Who is the judge of quality: users, automated systems, domain experts, or all three?
- What is the acceptable failure rate for each dimension?

## 2. Eval Dimensions Matrix

| Dimension | Definition | Why it matters | Automated? | Human eval? | Weight |
|-----------|-----------|---------------|------------|-------------|--------|
| **Correctness** | Output is factually accurate | | ✅/❌ | ✅/❌ | |
| **Completeness** | All required elements present | | | | |
| **Relevance** | Output addresses the actual request | | | | |
| **Coherence** | Logically consistent, well-structured | | | | |
| **Groundedness** | Claims are supported by source material | | | | |
| **Safety** | No harmful, biased, or policy-violating content | | | | |
| **Latency** | Response time meets SLA | | | | |
| **Instruction following** | Follows formatting/style instructions | | | | |
| **Tone** | Matches expected voice and audience | | | | |

## 3. Test Set Design

### Golden Set (Core Regression)
- **Size:** Minimum 200 examples (more for high-stakes use cases)
- **Coverage:** Must include all user intents and edge cases
- **Format:** Input → Expected output → Scoring rubric

### Edge Case Set
| Category | Examples | Pass criteria |
|----------|---------|--------------|
| Adversarial inputs | | |
| Out-of-domain queries | | |
| Ambiguous queries | | |
| Very long inputs | | |
| Multilingual inputs | | |

### Red Team Set
Prompts designed to elicit policy violations, hallucinations, or unsafe behavior.
- Minimum 50 adversarial prompts
- 0% acceptable failure rate on safety dimensions

## 4. Scoring Rubrics

### Human Eval Rubric (1–5 scale per dimension)
| Score | Meaning |
|-------|---------|
| 5 | Excellent — no improvements needed |
| 4 | Good — minor issues, wouldn't affect user |
| 3 | Acceptable — user can work with this but it's not ideal |
| 2 | Poor — significant issue, user notices |
| 1 | Failure — incorrect, harmful, or incomplete |

### LLM-as-Judge Prompt Template
For automated scoring, use an evaluation model with this structure:
```
You are evaluating an AI system's response quality.
Criterion: [dimension]
Definition: [exact definition]
Input: [original prompt]
Response: [model output]
Score 1-5 and explain your reasoning.
```

## 5. Regression Gate
Define pass/fail thresholds for shipping:

| Dimension | Ship gate | Block gate |
|-----------|-----------|------------|
| Correctness | ≥85% | <75% |
| Safety | 100% | <100% |
| Latency (P99) | ≤2s | >5s |
| Overall score | ≥4.0/5 | <3.5/5 |

## 6. Eval Run Schedule
| Eval type | Trigger | Frequency | Owner |
|-----------|---------|-----------|-------|
| Regression | Every model/prompt change | Per PR | Eng |
| Human eval | Monthly | Monthly | PM + QA |
| Red team | Major releases | Per version | Safety team |
| A/B comparison | New model candidates | On demand | PM |

## 7. Model Comparison Scorecard
Use for side-by-side model evaluation:
| Dimension | Model A | Model B | Model C | Winner |
|-----------|---------|---------|---------|--------|
| Correctness | | | | |
| Safety | | | | |
| Latency | | | | |
| Cost/token | | | | |
| **Overall** | | | | |

## 8. Eval Infrastructure Requirements
- [ ] Eval harness for automated scoring
- [ ] Annotation tool for human evaluators
- [ ] Inter-annotator agreement tracking (target κ > 0.7)
- [ ] Eval result versioning and trend tracking
- [ ] Dashboard to track eval scores over model versions
