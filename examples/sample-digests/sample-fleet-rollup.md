# Fleet QA Rollup — 2024-01-15

## Fleet Summary
- **Fleet pass rate:** 78% (47 of 60 cases across 3 agents)
- **Status:** 1 green / 2 yellow / 0 red
- **Agents tested:** 3
- **Total test cases:** 60

## Agent Health
| Agent | Pass Rate | Status | Tier 1 | Tier 2 | Tier 3 | Critical Issues |
|-------|-----------|--------|--------|--------|--------|-----------------|
| service-agent-1 | 85% (17/20) | 🟢 Green | 100% | 80% | 100% | 0 |
| service-agent-2 | 75% (15/20) | 🟡 Yellow | 90% | 70% | 100% | 0 |
| email-agent-1 | 75% (15/20) | 🟡 Yellow | 85% | 75% | 100% | 0 |

## Fleet-Wide Tier Performance
| Tier | Pass Rate | Target | Status | Gap |
|------|-----------|--------|--------|-----|
| **T1 Canonical** | 92% (33/36) | 100% | 🟡 Yellow | -8% |
| **T2 Paraphrased** | 75% (18/24) | ≥85% | 🔴 Red | -10% |
| **T3 Adversarial** | 100% (12/12) | ≥90% | 🟢 Green | +10% |

## Critical Fleet-Wide Issues

### 1. Shared Escalation Integration Issue
- **Affects:** service-agent-2, email-agent-1 (2 of 3 agents)
- **Impact:** 4 of 60 test cases failing (7%)
- **Root cause:** Escalation action timeout in Omni-Channel integration
- **Owner:** Platform team — shared integration layer
- **Priority:** P1 — Blocks UAT entry

### 2. T2 Paraphrased Coverage Below Target
- **Affects:** All agents
- **Impact:** Fleet-wide T2 at 75% (target 85%)
- **Root cause:** Topic classification needs tuning for informal language
- **Owner:** AI/ML team — topic instruction optimization
- **Priority:** P2 — Must fix before launch

## Top Failure Modes Across Fleet
1. **Action Error** — 6 cases (10%) — Escalation timeouts, API failures
2. **Misclassification** — 4 cases (7%) — Wrong topic routing
3. **Incomplete Flows** — 3 cases (5%) — Multi-turn conversations not completing

## Recommendations

### Immediate (This Sprint)
1. Fix shared escalation timeout issue (affects 2 agents)
2. Tune topic classification for informal language (all agents)
3. Expand T2 test coverage from 24 to 50 cases

### Before UAT (Next 2 Sprints)
4. Achieve 100% T1 pass rate across fleet
5. Achieve 85%+ T2 pass rate across fleet
6. Add 2 more agents to testing framework

### Post-Launch
7. Implement automated daily regression
8. Set up Slack notifications for failures
9. Historical trending dashboard

## UAT Readiness Assessment

| Criteria | Current | Target | Status |
|----------|---------|--------|--------|
| Fleet Pass Rate | 78% | ≥85% | ❌ Not Ready |
| T1 Pass Rate | 92% | 100% | ❌ Not Ready |
| T2 Pass Rate | 75% | ≥85% | ❌ Not Ready |
| T3 Pass Rate | 100% | ≥90% | ✅ Ready |
| No P1 Blockers | 1 P1 | 0 P1 | ❌ Not Ready |

**Estimated time to UAT-ready:** 2-3 weeks

---

**Rollup generated:** 2024-01-15  
**Next rollup:** 2024-01-16  
**Contact:** qa-team-lead@company.com
