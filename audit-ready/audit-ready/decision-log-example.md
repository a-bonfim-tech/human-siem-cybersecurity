# Decision Log — Escalation vs. Non-Escalation (Example)

This document demonstrates how **security judgment is documented** under the Human SIEM operating model.

All scenarios are synthetic, abstracted, and compliance-safe.

---

## Scenario A — Escalation Triggered

### Context

Multiple correlated signals indicate potential compromise of an identity with elevated privileges.

### Observed Signals

* Anomalous authentication behavior across distinct systems.
* Privilege context exceeds baseline role expectation.
* Temporal clustering reduces likelihood of benign explanation.

### Evaluation

* **Impact threshold:** Met
  Elevated identity could affect control plane access.

* **Confidence threshold:** Met
  Correlation across independent signals reduces uncertainty.

* **Time sensitivity:** Met
  Delay increases risk of lateral movement.

### Decision

**Escalate**

### Rationale

At least one hard escalation condition was met and documented.
Non-action would increase expected harm.

### Escalation Package

* Summary of observed behavior
* Evidence list (signals only, no speculation)
* Decision justification
* Ownership handoff to incident response

### Audit Note

This escalation can be defended six months later based on documented thresholds.

---

## Scenario B — Deliberate Non-Escalation

### Context

Single alert indicating unusual network activity without corroboration.

### Observed Signals

* One isolated alert
* No identity, privilege, or scope expansion
* No corroborating indicators

### Evaluation

* **Impact threshold:** Not met
* **Confidence threshold:** Not met
* **Time sensitivity:** Not met
* **Policy trigger:** Not met

### Decision

**Document-only**

### Rationale

Escalation would violate silence-by-design principles and introduce unnecessary noise.

### Action Taken

* Decision documented
* Monitoring maintained
* No handoff initiated

### Audit Note

Non-escalation is an explicit, defensible security decision — not inaction.

---

## Control Question

> “Would I justify this decision six months later, with no additional context?”

If the answer is **no**, the decision must be revisited.

---

Author: André Luiz Vieira Bonfim
Model: Human SIEM — Audit-Ready Decision Logging
