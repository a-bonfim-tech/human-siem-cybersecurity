# RUNBOOK — Endpoint

## Purpose

This runbook defines how endpoint-level signals are interpreted
and governed within the Human SIEM operating model.

Endpoints are treated as evidence sources,
not as alert generators by default.

---

## Scope

This runbook applies to:

* process creation and termination
* command execution
* file creation, modification, and deletion
* privilege use at the host level
* endpoint security control events

It does not cover:

* pure network-based detections
* application business logic
* user experience monitoring

---

## Core Assumptions

* Most malicious activity executes on endpoints
* Context is more important than individual commands
* Execution chains matter more than single events

Endpoints are interpreted narratively, not atomically.

---

## Signals Observed (Abstract)

The following signal categories are monitored:

* process creation patterns
* parent-child process relationships
* execution of administrative tools
* file system changes in sensitive locations
* abnormal use of scripting or automation engines

Signals are correlated over time and context.

---

## Decision Logic

### Observe

Endpoint activity is observed without alerting when:

* execution matches known operational patterns
* tools are used within expected scope
* user intent is plausible and documented
* no privilege boundary is crossed

Observation decisions must be documented.

---

### Alert

An alert is triggered when:

* execution chains resemble known attack techniques
* administrative tools are used unexpectedly
* persistence mechanisms are introduced
* endpoint behavior deviates significantly from baseline

Alerts must clearly state:

* what executed
* under which identity
* why the execution is suspicious
* what risk it introduces

---

### Act

Immediate action is taken when:

* malicious execution is highly probable
* privilege escalation is confirmed
* endpoint integrity is compromised
* continued execution increases impact

Actions may include:

* process termination
* endpoint isolation
* credential invalidation
* incident response activation

---

## Escalation

Escalation occurs when:

* endpoint compromise affects critical systems
* forensic preservation is required
* legal or compliance exposure exists
* business operations may be disrupted

Escalation shifts responsibility beyond endpoint operations.

---

## False Positives and Silence

False positives are addressed by:

* refining execution baselines
* improving tool allowlists
* correlating with identity and task context

Silence is acceptable when:

* execution behavior is understood
* administrative intent is validated
* compensating controls exist

Silence must be intentional and documented.

---

## Audit Notes

For every endpoint-related decision, the following must be explainable:

* why execution was considered benign or malicious
* how context was established
* what evidence supported the decision
* who owned the response

Endpoint decisions must be defensible under forensic review.

---

## Final Statement

Endpoints do not lie.
Interpretations do.

This runbook exists to ensure that endpoint evidence
leads to proportional, defensible security decisions.
