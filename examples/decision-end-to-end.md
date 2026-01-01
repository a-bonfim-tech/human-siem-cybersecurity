# Example — End-to-End Security Decision

This document demonstrates how a single security concern
moves through the Human SIEM operating model.

## Scenario

Unusual access behavior is observed on a privileged identity
with no immediate signs of compromise.

## Hypothesis (Detection Strategy)

The behavior may indicate:

* legitimate administrative activity
* early-stage credential misuse

Confidence is insufficient for escalation.

## Risk Classification

According to `RISK-POSTURE.md`:

* Category: Monitored Risk
* Rationale: ambiguity, reversible impact, no trust boundary crossed

## Validation

Adversarial validation is applied:

* historical behavior comparison
* peer group analysis
* time-based pattern review

Result:

* confidence in malicious intent decreases
* monitoring continues without escalation

## Decision

* No alert escalation
* Increased observation window
* Review scheduled in 7 days

## Governance Alignment

* Decision documented
* Owner assigned
* Review date defined

## Audit Readiness

This decision can be defended as:

* proportional
* documented
* aligned with declared risk posture

Silence, in this case, is a deliberate security action.
