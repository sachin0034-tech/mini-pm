---
description: Design AI safety guardrails covering content policy, topic boundaries, and abuse prevention
---

You are a PM designing the safety guardrails for an AI product for:

**Input:** $ARGUMENTS (AI product, user base, use case, risk tolerance)

## 1. Risk Assessment

### Product Risk Profile
| Dimension | Level | Rationale |
|-----------|-------|-----------|
| User vulnerability | H/M/L | (children, healthcare, finance?) |
| Output stakes | H/M/L | (advice vs. entertainment vs. productivity) |
| Abuse potential | H/M/L | (scale of misuse if guardrails fail) |
| Regulatory exposure | H/M/L | (HIPAA, GDPR, COPPA, financial regs) |

**Overall risk tier:** High / Medium / Low → determines guardrail strictness

---

## 2. Content Policy Framework

### Always Block (Hardcoded — no exceptions)
| Category | Definition | Example |
|----------|-----------|---------|
| CSAM | Child sexual abuse material | [explicit] |
| Instructions for mass-casualty weapons | CBRN weapons creation | |
| Critical infrastructure attacks | Power grid, water, financial system attacks | |
| Active violence facilitation | Direct instructions for harming specific people | |

### Block by Default (Softcoded — configurable for enterprise)
| Category | Default | Enterprise configurable? | Example |
|----------|---------|------------------------|---------|
| Explicit adult content | Block | Yes (adult platforms) | |
| Graphic violence | Block | Yes (gaming, research) | |
| Controlled substance guidance | Block | Yes (medical) | |
| Political persuasion at scale | Block | Limited | |

### Use-Case Specific Rules
| Rule | Block | Allow | Notes |
|------|-------|-------|-------|
| Off-topic queries | Redirect | — | "I can only help with [domain]" |
| Competitor mentions | — | Allow (factual) | |
| Medical advice | Disclaimer required | — | |

---

## 3. Guardrail Architecture

### Input Guardrails (Before LLM)
| Layer | What it checks | Action on violation |
|-------|---------------|---------------------|
| Prompt injection detection | Attempts to override system prompt | Block + log |
| PII detection | SSN, credit card, passwords in input | Warn user |
| Topic classifier | Is query in-scope? | Redirect if not |
| Content filter | Harmful intent | Block |

### Output Guardrails (After LLM)
| Layer | What it checks | Action on violation |
|-------|---------------|---------------------|
| Factual consistency | Output contradicts retrieved sources | Flag uncertainty |
| PII in output | Model generated PII | Redact |
| Harmful content | Safety policy violations | Block and log |
| Hallucination signals | Uncertain/fabricated content | Add disclaimer |

---

## 4. Refusal Design

A bad refusal is as harmful as a missing guardrail — it breaks trust and creates support escalations.

### Refusal Quality Standards
- [ ] Explain WHAT was refused (vaguely, not specifics that teach bypass)
- [ ] Offer what the system CAN help with instead
- [ ] Never lecture or moralize beyond what's necessary
- [ ] Be consistent (same input → same refusal every time)

### Refusal Templates
**For out-of-scope:**
> "That's outside what I can help with here. I'm designed to [scope]. For [user need], you might try [alternative]."

**For policy violation:**
> "I'm not able to help with that. If you have a question about [related safe topic], I'm happy to help."

---

## 5. Abuse Prevention

| Attack vector | Risk | Detection | Response |
|--------------|------|-----------|---------|
| Prompt injection | High | Pattern matching | Block |
| Jailbreak attempts | High | Classifier | Refuse + rate limit |
| High-volume scraping | Medium | Rate limiting | Throttle |
| Adversarial probing | Medium | Anomaly detection | Flag for review |

---

## 6. Red Team Testing Plan
Before launch:
- [ ] Internal red team: [N] hours of adversarial probing
- [ ] External red team: 3rd party safety evaluation
- [ ] Automated adversarial test suite: [N] prompts
- [ ] Edge case library: build from red team findings

---

## 7. Incident Response

| Severity | Definition | Response SLA | Escalation |
|---------|-----------|-------------|-----------|
| P0 | Active harm, legal exposure | 30 min | CEO + Legal |
| P1 | Policy violation, user harm | 2 hours | VP + Safety |
| P2 | Guardrail bypass, no user harm | 24 hours | PM + Eng |
| P3 | Policy edge case, ambiguous | 1 week | PM |

---

## 8. Governance & Review
- **Policy owner:**
- **Policy review cadence:** Quarterly
- **External feedback channel:**
- **Regulatory monitoring owner:**
