# SOC Escalation Boundary Policy

## Purpose

Define a **clear, defensible escalation boundary** for SOC operations, ensuring that human action is taken only when justified, authorized, and auditable.

This policy prevents:

* alert-driven panic,
* hero-mode decision making,
* unnecessary incident escalation,
* undocumented judgment calls.

## Scope

Applies to all SOC-relevant signals evaluated under the Human SIEM operating model.

Out of scope:

* tooling configuration,
* detection rule syntax,
* organization-specific thresholds.

## Decision States

Every signal must end in **one and only one** state:

1. **Document-only**
2. **Validate**
3. **Escalate**
4. **Stop (Kill-switch)**

No action outside these states is permitted.

## Escalation Rule (Hard Boundary)

Escalation is permitted **only if at least one condition below is met** and documented.

### Escalation Conditions

* **Impact Threshold**
  Credible risk to confidentiality, integrity, or availability with material consequence.

* **Confidence Threshold**
  Correlated signals reduce uncertainty beyond a single alert or indicator.

* **Time Sensitivity**
  Delay materially increases expected harm (short time-to-impact).

* **Policy Trigger**
  Explicit governance rule mandates escalation (identity breach, admin access, regulated data).

* **Blast Radius Expansion**
  Scope crosses a defined boundary (identity plane, control plane, org-wide services).

If none apply, escalation is forbidden.

## Default Actions

* **Validate**
  Used when the scenario is plausible but uncertainty remains high.

* **Document-only**
  Used when signal quality is weak or non-actionable (silence-by-design).

## Definition of Escalation

Escalation is a **formal handoff**, not an emotional response.

It must include:

* concise summary (what happened / why it matters),
* observed evidence (facts only),
* decision log entry (why escalation occurred),
* explicit next owner.

## Kill-Switch Condition

If authority, scope, or policy alignment is unclear:
**STOP. Document. Escalate only after clarification.**

## Audit Principle

Every escalation decision must be defensible:

> “Would I justify this decision six months later, with no additional context?”

If not, escalation must not occur.

---

Author: André Luiz Vieira Bonfim
Model: Human SIEM – Governance-first SOC
