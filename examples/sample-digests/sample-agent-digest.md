# QA Digest — my-service-agent — 2024-01-15
**Owner:** qa-team  
**Sandbox:** qa-sandbox  
**Test Definition:** My_Service_Agent_Regression

## Summary
- Overall pass rate: 75% (15 of 20 cases)
- Status: Yellow — Overall good, but T2 below target
- Net change since last digest: +5% (recovered 2 cases, 1 new failure)

## Pass Rate by Tier
| Tier | Pass Rate | Target | Status |
|---|---|---|---|
| T1 Canonical    | 90% (9/10) | 100% | Yellow |
| T2 Paraphrased  | 70% (7/10) | ≥85% | Red |
| T3 Adversarial  | 100% (3/3) | ≥90% | Green |

## Pass Rate by Capability
| Test Set / Capability | Pass Rate | Trend |
|---|---|---|
| order_status | 100% (3/3) | ↑ |
| knowledge_qna | 100% (2/2) | → |
| returns_exchanges | 67% (2/3) | ↓ |
| escalation | 50% (1/2) | → |

## Failures Requiring Attention

### Failure Mode: Action Error (2 cases)
**Likely root cause:** Escalation action timing out

**Affected utterances:**
- "I need to speak with a human"
- "Can I talk to someone?"

**Suggested owner:** Dev — Integration/Omni-Channel

---

### Failure Mode: Misclassification (1 case)
**Likely root cause:** Exchange requests routing to wrong topic

**Affected utterances:**
- "Can I exchange my order?"

**Suggested owner:** Dev — Topic tuning

---

## Recommended Actions

1. **Fix escalation timeout** (Priority 1)
2. **Correct exchange classification** (Priority 1)
3. **Expand T2 test coverage** (Priority 2)

---

**Digest generated:** 2024-01-15  
**Duration:** 95 seconds
