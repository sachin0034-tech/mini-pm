---
description: Write an AI/ML feature product spec covering model behavior, evaluation, safety, and user trust
---

You are a PM speccing out an AI feature. Write a comprehensive AI product specification for:

**Input:** $ARGUMENTS (AI feature description, product context, users, constraints)

## AI Feature Specification

---

## 1. Feature Overview
- **Name:**
- **Category:** Generative / Predictive / Recommendation / Agentic / Search
- **Modality:** Text / Image / Audio / Video / Multimodal
- **AI approach:** LLM / Fine-tuned model / RAG / Classification / Other

---

## 2. User Problem & Value
- What problem does this AI capability solve?
- Why is AI the right approach vs. non-AI alternatives?
- What would the user do without this feature?

---

## 3. Behavior Specification

### Happy Path (core use case)
| Input | Expected AI behavior | Expected output |
|-------|--------------------| ----------------|
| [Typical input] | | |

### Edge Cases
| Input type | Expected handling |
|-----------|------------------|
| Empty / null input | |
| Input too long | |
| Ambiguous query | |
| Harmful / adversarial input | |
| Out-of-domain query | |
| Non-English input | |

---

## 4. Model Evaluation Framework
Define what "good" looks like before building:

| Eval Dimension | Definition | Measurement method | Target |
|---------------|-----------|-------------------|--------|
| **Accuracy / Correctness** | | Human eval + automated | |
| **Relevance** | | Human eval | |
| **Groundedness** (RAG) | Factual claims supported by context | Citation check | |
| **Latency (P50/P99)** | | Automated | |
| **Safety** | Refuses harmful requests | Red team eval | 0% slip rate |
| **Helpfulness** | Users complete their task | Task completion rate | |

### Evals to Build
- [ ] Golden set: N test cases covering [scenarios]
- [ ] Automated regression suite
- [ ] Human evaluation rubric
- [ ] Red team test set (adversarial prompts)

---

## 5. Safety & Guardrails
| Risk | Severity | Mitigation |
|------|---------|-----------|
| Hallucination / false information | High | Source grounding, confidence scoring |
| Harmful content generation | Critical | Content filter, refusal instructions |
| PII leakage | Critical | Data masking, output scanning |
| Bias in outputs | High | Demographic eval, bias testing |
| Prompt injection | High | Input sanitization, context isolation |

---

## 6. User Trust Design
How do we build appropriate trust (not over-trust, not under-trust)?
- [ ] Confidence indicators shown when appropriate
- [ ] Sources cited for factual claims
- [ ] "AI-generated" label visible
- [ ] Easy correction mechanism for wrong outputs
- [ ] Clear capability boundaries communicated (what AI does/doesn't do)

---

## 7. Failure Mode Handling
| Failure | User experience | Recovery path |
|---------|----------------|--------------|
| Model timeout | | Retry with backoff |
| Low-confidence output | | Show uncertainty, offer alternatives |
| Context too long | | Summarize / truncate strategy |
| Content filtered | | Explain refusal, offer alternative |

---

## 8. Data Requirements
- **Training data:** (if fine-tuning)
- **Retrieval corpus:** (if RAG)
- **Data freshness requirement:**
- **PII handling:**
- **Data lineage / provenance:**

---

## 9. A/B Test Plan for AI Quality
| Variant | Change | Primary eval metric | Duration |
|---------|--------|--------------------| ---------|
| Control | Current behavior | | |
| Variant A | [Prompt change / model change] | | |

---

## 10. Responsible AI Checklist
- [ ] Bias evaluation across demographic groups
- [ ] Accessibility of AI-generated content
- [ ] Human-in-the-loop for high-stakes decisions
- [ ] Opt-out mechanism for users who don't want AI
- [ ] Model card / transparency documentation
- [ ] Privacy impact assessment completed
