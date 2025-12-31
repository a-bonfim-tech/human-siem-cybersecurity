# SOC ALIGNMENT — False Positive Policy

## Purpose

This document defines how false positives are handled within the Human SIEM
operating model.

False positives are treated as design feedback,
not analyst failure.

---

## Definition of a False Positive

A false positive occurs when:

* a signal triggers alerting
* no meaningful risk exists
* no security decision is required

False positives are not mistakes by responders.
They are signals that detection logic requires refinement.

---

## Why False Positives Matter

False positives cause harm even without incidents.

They:

* waste operational attention
* reduce trust in detection systems
* increase response latency
* create audit noise

Managing false positives is a core security responsibility.

---

## Principles for Handling False Positives

False positives are addressed by:

* improving hypotheses
* refining correlation logic
* adding missing context
* adjusting alert conditions

They are never addressed by:

* increasing analyst workload
* suppressing alerts without reasoning
* blaming individuals

---

## Classification of False Positives

False positives are classified to guide remediation:

### Design False Positive

Caused by flawed assumptions or incomplete hypotheses.

### Context False Positive

Caused by missing identity, timing, or environmental context.

### Operational False Positive

Caused by legitimate but undocumented workflows.

Each class requires a different corrective action.

---

## Resolution Process

When a false positive is identified:

1. The alert is reviewed and documented
2. The root cause is classified
3. Detection logic is adjusted or retired
4. Documentation is updated

Resolution must be tracked to completion.

---

## Relationship with Alert Lifecycle

Persistent false positives indicate:

* alert lifecycle failure
* governance breakdown

Alerts that cannot be corrected
must be retired.

---

## Accountability

False positive remediation has an owner.

Ownership includes:

* root cause analysis
* corrective action
* validation of improvement

Unowned false positives are unmanaged risk.

---

## Communication and Culture

False positives are communicated as:

* opportunities to improve detection
* indicators of system learning

Blame-free handling is mandatory.
Fear-driven environments increase risk.

---

## Audit Notes

For false positive handling, the following must be explainable:

* why the alert was incorrect
* how detection logic changed
* how recurrence was prevented
* who approved the change

False positive management must withstand audit review.

---

## Final Statement

False positives are not noise to be ignored.
They are signals to be understood.

This policy exists to ensure that detection systems
improve over time without harming people or operations.
