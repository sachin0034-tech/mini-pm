---
description: Build a comprehensive product launch plan with readiness checklist, war room protocol, and rollback plan
---

You are a PM owning a product launch for:

**Input:** $ARGUMENTS (product/feature name, launch date, target market, team)

## 1. Launch Overview
| Field | Details |
|-------|---------|
| **Feature/Product** | |
| **Launch date** | |
| **Launch tier** | T1 / T2 / T3 / T4 |
| **Launch owner** | |
| **Stakeholders** | |
| **Target segments** | |

## 2. Launch Readiness Checklist

### Product
- [ ] Feature complete against P0 acceptance criteria
- [ ] P0 / P1 bugs resolved
- [ ] Performance benchmarks met (latency, error rate)
- [ ] Security review completed
- [ ] Accessibility audit passed
- [ ] Mobile / cross-browser tested

### Data & Analytics
- [ ] All tracking events instrumented and verified
- [ ] Dashboard live with baseline populated
- [ ] Alerts configured for key metrics
- [ ] Success metrics agreed with stakeholders

### Go-to-Market
- [ ] Pricing finalized and approved
- [ ] Marketing copy approved
- [ ] In-product messaging / onboarding live
- [ ] Email / push notification scheduled
- [ ] Sales/CS enablement completed (battle card, demo, FAQ)
- [ ] Help center articles published

### Legal & Compliance
- [ ] Privacy review completed
- [ ] Terms of service updated
- [ ] Data retention policy confirmed
- [ ] Any regulatory approvals obtained

### Infrastructure
- [ ] Load test completed (at 2× expected peak traffic)
- [ ] Runbook written for on-call
- [ ] Feature flags configured for progressive rollout
- [ ] Rollback plan documented and tested

## 3. Progressive Rollout Plan
| Phase | % of users | Criteria to advance | Duration |
|-------|-----------|--------------------| ---------|
| Canary | 1% | No P0 bugs, metrics stable | 24 hours |
| Early access | 10% | Error rate <X%, latency <Xms | 3 days |
| Broad rollout | 50% | Activation rate >X% | 5 days |
| Full launch | 100% | All metrics green | - |

## 4. Launch Day War Room
| Role | Person | Responsibility | Contact |
|------|--------|---------------|---------|
| Launch owner | | Overall coordination | |
| Eng lead | | Technical monitoring | |
| Data | | Metrics monitoring | |
| CS/Support | | Customer escalations | |
| Comms | | Social/PR monitoring | |

**Launch day schedule:**
- [T-1h] Final readiness check
- [T-0] Feature flag flip
- [T+30min] First metrics check
- [T+2h] Decision point: continue or rollback
- [T+24h] Day-1 review

## 5. Rollback Plan
**Rollback trigger criteria:**
- Error rate > X% for > 15 minutes
- P0 bug with no ETA
- Core metric drops > Y% in first 2 hours

**Rollback steps:**
1. [Who authorizes the rollback]
2. [Technical steps to roll back — feature flag, deploy revert]
3. [Customer communication if needed]
4. [Post-rollback monitoring]

## 6. Launch Success Criteria
| Metric | Target | Measurement window |
|--------|--------|-------------------|
| | | Launch week |
| | | 30 days |

## 7. Post-Launch Review (T+30 days)
Schedule a 30-day review. Agenda:
- Metrics vs. targets
- Customer feedback themes
- Unexpected behaviors
- What to change in next iteration
- GTM lessons learned
