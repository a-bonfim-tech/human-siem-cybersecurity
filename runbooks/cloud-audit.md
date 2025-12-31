# RUNBOOK — Cloud Audit

## Purpose

This runbook defines how cloud administrative actions are monitored,
interpreted, and governed within the Human SIEM operating model.

The focus is not infrastructure noise, but control-plane integrity.

---

## Scope

This runbook applies to:

* cloud control-plane actions
* administrative API calls
* configuration changes
* identity-driven cloud operations

It does not cover:

* application-level logic
* data-plane traffic without administrative context

---

## Core Assumptions

* Control-plane abuse precedes technical compromise
* Administrative actions are high-impact by definition
* Identity context is mandatory for interpretation

Any cloud event without identity attribution is treated as incomplete.

---

## Signals Observed (Abstract)

The following signal categories are monitored:

* creation, modification, or deletion of cloud resources
* IAM policy changes and role bindings
* network or security control changes
* logging, monitoring, or security feature disablement
* service account creation or permission expansion

Signals are evaluated for intent and reversibility.

---

## Decision Logic

### Observe

Cloud actions are observed without alerting when:

* changes follow approved workflows
* actions are reversible
* identity and purpose are clear
* timing and scope match expectations

Observation decisions must be documented.

---

### Alert

An alert is triggered when:

* administrative actions occur outside approved workflows
* privilege scope increases unexpectedly
* security or logging controls are weakened
* actions affect multiple critical resources

Alerts must clearly state:

* who performed the action
* what changed
* potential impact
* whether the change is reversible

---

### Act

Immediate action is taken when:

* security controls are disabled
* logging or monitoring is intentionally reduced
* irreversible actions are initiated
* administrative access is abused

Actions may include:

* access revocation
* configuration rollback
* resource isolation
* incident response activation

---

## Escalation

Escalation occurs when:

* actions introduce institutional risk
* regulatory or compliance exposure exists
* business continuity is affected
* administrative intent cannot be established

Escalation transfers decision ownership to leadership.

---

## False Positives and Silence

False positives are addressed by:

* refining workflow baselines
* improving identity attribution
* clarifying approval processes

Silence is acceptable when:

* changes are expected and approved
* impact is limited and reversible
* governance controls remain intact

Silence must be intentional and documented.

---

## Audit Notes

For each cloud-related decision, the following must be explainable:

* why the action was risky or acceptable
* how approval was validated
* who owned the decision
* how reversibility was assessed

Cloud audit decisions must withstand regulatory and internal audits.

---

## Final Statement

Most cloud incidents are management failures
before they are technical failures.

This runbook exists to detect and govern
control-plane risk before damage occurs.
