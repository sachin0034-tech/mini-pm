---
description: Design a rigorous A/B test with sample size calculation, success criteria, and analysis plan
---

You are a PM designing a statistically rigorous A/B test for:

**Input:** $ARGUMENTS (hypothesis, feature being tested, primary metric, traffic available)

## 1. Test Hypothesis
**Format:** "If we [change X], then [metric Y] will [increase/decrease] by [Z%] because [user behavior reason]."

**Null hypothesis (H0):** No difference between control and variant.
**Alternative hypothesis (H1):** Variant outperforms control by ≥ [minimum detectable effect].

## 2. Test Design

| Parameter | Value |
|-----------|-------|
| **Control (A)** | [Current experience] |
| **Variant (B)** | [Changed experience] |
| **Test type** | One-tailed / Two-tailed |
| **Primary metric** | [Specific metric + formula] |
| **Secondary metrics** | [2–3 supporting signals] |
| **Guardrail metrics** | [Must not regress] |

## 3. Sample Size Calculation

| Parameter | Value | Notes |
|-----------|-------|-------|
| Baseline conversion rate | X% | Current state |
| Minimum Detectable Effect | +Y% relative | Smallest change worth shipping |
| Statistical significance (α) | 95% | False positive tolerance |
| Statistical power (1-β) | 80% | False negative tolerance |
| **Required sample per variant** | N users | Calculate using power analysis |
| **Available daily traffic** | N users/day | |
| **Required test duration** | [Days] | Sample needed ÷ daily traffic |

**Duration rule:** Run for at least 1 full business cycle (≥7 days for most products). Never stop early based on early results.

## 4. Segmentation Plan
Will you analyze results for sub-segments?
| Segment | Expected effect direction | Reason |
|---------|--------------------------|--------|

## 5. Novelty Effect Check
- Expected novelty period: [X days]
- Plan: exclude first [X days] from final analysis OR run test for [3×] the novelty period

## 6. Assignment Rules
- **Unit of assignment:** User ID / session / device? (User-level recommended to avoid contamination)
- **Randomization method:**
- **Exclusion criteria:** (existing users, employees, bots)
- **Traffic split:** 50/50 or [X%/Y%] — explain if not 50/50

## 7. Launch Checklist
- [ ] Logging instrumented and validated in staging
- [ ] Holdout group defined (if needed)
- [ ] Experiment ID registered in experiment tracking system
- [ ] Rollback plan defined
- [ ] Stakeholders notified

## 8. Analysis Plan
After test completes:
1. Check for Sample Ratio Mismatch (SRM) — if actual split differs from intended, the test is compromised
2. Run primary metric test (t-test or z-test for proportions)
3. Check secondary and guardrail metrics
4. Segment analysis for heterogeneous treatment effects
5. Document: effect size, p-value, confidence interval

## 9. Decision Framework
| Result | Decision |
|--------|---------|
| P<0.05, effect ≥ MDE, no guardrails regressed | Ship variant |
| P<0.05, effect ≥ MDE, guardrail regressed | Investigate before shipping |
| P>0.05 | Do NOT ship — result is inconclusive, not "neutral" |
| SRM detected | Invalidate test, fix assignment bug, re-run |

## 10. Iterated Learning
Regardless of outcome, document: what we learned about user behavior that informs the next test.
