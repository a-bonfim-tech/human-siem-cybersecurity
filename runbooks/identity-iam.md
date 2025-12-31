# RUNBOOK — Identity & IAM

## Purpose

This runbook defines how identity-related signals are observed, interpreted,
and acted upon within the Human SIEM operating model.

Identity is treated as the primary security control plane.
All other signals are contextualized through identity.

---

## Scope

This runbook applies to:

* authentication events
* authorization decisions
* privilege changes
* identity lifecycle events

It does not cover:

* application-specific logic
* network-only anomalies without identity context

---

## Core Assumptions

* Authenticated actions are more meaningful than anonymous traffic
* Privilege escalation is more critical than access volume
* Identity context precedes infrastructure context

Any analysis that ignores these assumptions is considered incomplete.

---

## Signals Observed (Abstract)

The following signal categories are monitored:

* authentication success and failure
* changes in authentication methods (e.g., MFA state)
* privilege assignment or removal
* service account or machine identity activity
* anomalous access context (time, location, device)

Signals are evaluated collectively, not in isolation.

---

## Decision Logic

### Observe

Identity events are observed without alerting when:

* behavior matches known patterns
* access is low privilege
* contextual anomalies are explainable
* no privilege boundary is crossed

Observation must be documented.

---

### Alert

An alert is triggered when:

* authentication anomalies suggest credential misuse
* privilege escalation occurs outside expected workflows
* identity behavior deviates significantly from baseline
* service accounts act outside defined purpose

Alerts must clearly state:

* who acted
* what changed
* why it matters

---

### Act

Immediate action is taken when:

* privileged identities are compromised
* irreversible access changes occur
* identity controls are bypassed
* trust boundaries are violated

Actions may include:

* access revocation
* session termination
* forced credential reset
* escalation to incident response

---

## Escalation

Escalation occurs when:

* identity compromise impacts critical systems
* regulatory or legal exposure is possible
* business operations are affected
* attribution or intent remains unclear

Escalation shifts accountability beyond the security function.

---

## False Positives and Silence

Identity-related false positives are treated as:

* detection design issues
* not analyst failure

Silence is acceptable when:

* identity behavior is understood
* compensating controls exist
* risk remains within tolerance

Silence decisions must be documented.

---

## Audit Notes

For every identity-related decision, the following must be explainable:

* why the signal mattered
* why action was or was not taken
* who owned the decision
* how the decision aligns with risk posture

Identity decisions must withstand audit review months later.

---

## Final Statement

Identity failures cascade.
Identity discipline contains damage.

This runbook exists to ensure that identity signals
lead to consistent, defensible, and timely decisions.
