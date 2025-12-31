# AUDIT READY — Decision Logging

## Purpose

This document defines how security decisions are logged within the Human SIEM
operating model.

Decision logging exists to ensure that actions, alerts, and silence
can be explained, defended, and reconstructed over time.

---

## Decisions Are the Primary Audit Artifact

Logs record events.
Decision logs record judgment.

Audits do not evaluate tools.
Audits evaluate decisions made under uncertainty.

This model prioritizes decision logging over raw data retention.

---

## What Must Be Logged

A decision must be logged whenever:

* an alert is created
* an alert is closed
* silence is intentionally chosen
* escalation occurs
* containment or blocking actions are taken
* risk is accepted or deferred

If a decision affects risk posture, it must be logged.

---

## Mandatory Fields for Decision Logs

Every decision log must include:

* **Decision ID**
* **Date and Time**
* **Decision Type** (Observe / Alert / Act / Escalate)
* **Summary** (one paragraph, plain language)
* **Rationale** (why this decision was made)
* **Evidence Considered** (categories, not raw data)
* **Risk Assessment** (acceptable, monitored, unacceptable)
* **Decision Owner**
* **Review Date (if applicable)**

Incomplete logs are governance failures.

---

## Quality of Decision Logs

A valid decision log must be:

* understandable without tools
* explainable to non-technical stakeholders
* sufficient to reconstruct reasoning months later

If a decision cannot be explained without screenshots or dashboards,
it is insufficiently logged.

---

## Decision Logs and Silence

Silence requires the same level of logging as action.

Silence logs must explain:

* what was observed
* why escalation was not required
* how risk was controlled
* when the decision will be reviewed

Unlogged silence is unacceptable.

---

## Retention and Accessibility

Decision logs must be:

* retained according to policy
* protected against modification
* accessible for audit and review

Loss of decision logs equals loss of accountability.

---

## Relationship with Incident Records

Decision logs are independent from incident reports.

Incidents summarize outcomes.
Decision logs preserve reasoning.

Both are required.
Neither replaces the other.

---

## Review and Improvement

Decision logs are periodically reviewed to:

* identify recurring assumptions
* improve detection and governance
* refine risk posture

Audit is not punishment.
Audit is feedback.

---

## Final Statement

Security decisions age.
Good documentation keeps them valid.

This model exists to ensure that cybersecurity judgment
remains defensible long after the incident ends.
