# RUNBOOK — Applications & APIs

## Purpose

This runbook defines how application- and API-level signals are interpreted
and governed within the Human SIEM operating model.

Applications are treated as business logic surfaces,
not merely technical components.

---

## Scope

This runbook applies to:

* application authentication and authorization events
* API access and usage patterns
* application errors and failures
* business logic abuse indicators
* rate limiting and abuse control signals

It does not cover:

* infrastructure-only events without application relevance
* client-side telemetry unrelated to security decisions

---

## Core Assumptions

* Applications embody business intent
* Logic abuse often precedes technical exploitation
* Identity context is essential for interpretation
* Availability and trust are business assets

Application security decisions balance risk and user impact.

---

## Signals Observed (Abstract)

The following signal categories are monitored:

* authentication and authorization failures
* abnormal API usage patterns
* unexpected parameter manipulation
* error patterns indicating probing or abuse
* bypass attempts of application controls

Signals are evaluated in business context, not volume alone.

---

## Decision Logic

### Observe

Application behavior is observed without alerting when:

* errors align with expected user behavior
* usage patterns are explainable by business activity
* impact is limited and reversible
* no trust boundary is violated

Observation decisions must be documented.

---

### Alert

An alert is triggered when:

* application logic abuse is plausible
* authentication or authorization boundaries are stressed
* API usage suggests automation or misuse
* application behavior deviates from established norms

Alerts must clearly state:

* affected functionality
* identity context
* potential business impact
* confidence level of malicious intent

---

### Act

Immediate action is taken when:

* abuse threatens availability or data integrity
* authorization controls are bypassed
* user trust is at risk
* continued activity increases business damage

Actions may include:

* temporary access restriction
* rate limiting or blocking
* feature-level containment
* incident response escalation

Actions must consider user experience impact.

---

## Escalation

Escalation occurs when:

* business operations are disrupted
* customer data may be exposed
* legal or regulatory obligations are triggered
* security decisions affect product functionality

Escalation aligns security with product and leadership.

---

## False Positives and Silence

False positives are mitigated by:

* close alignment with product teams
* understanding normal user behavior
* refining application baselines

Silence is acceptable when:

* behavior is consistent with business usage
* controls function as designed
* risk remains within tolerance

Silence must be intentional and documented.

---

## Audit Notes

For every application-related decision, the following must be explainable:

* why the behavior mattered to the business
* how user impact was assessed
* what controls mitigated the risk
* who approved the decision

Application security decisions must withstand executive and regulatory scrutiny.

---

## Final Statement

Applications are where trust is earned or lost.

This runbook exists to ensure that application security
protects the business without obstructing it.
