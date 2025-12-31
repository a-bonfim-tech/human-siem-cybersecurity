# SOC ALIGNMENT — Triage Logic

## Purpose

This document defines the triage logic used within the Human SIEM
operating model.

Triage exists to ensure that signals are evaluated consistently,
proportionally, and without improvisation.

---

## Triage Is a Decision Function

Triage is not classification.
Triage is decision-making under uncertainty.

Its purpose is to determine:

* whether a signal matters
* how urgently it matters
* who must decide next

Speed without judgment is risk.

---

## Triage Inputs

Triage decisions consider the following inputs:

* identity context
* signal confidence
* potential impact
* scope of exposure
* reversibility of damage
* alignment with known hypotheses

No single input is sufficient alone.

---

## Triage Outcomes

Every triage decision results in one of three outcomes:

1. **Close**
   The signal does not represent meaningful risk.

2. **Monitor**
   The signal warrants observation without escalation.

3. **Escalate**
   The signal requires immediate or prioritized action.

Ambiguous outcomes are not allowed.

---

## Close Criteria

A signal is closed when:

* behavior is understood and benign
* impact is negligible
* compensating controls exist
* no decision escalation is required

Closure must be documented.

---

## Monitor Criteria

A signal is monitored when:

* behavior is unusual but plausible
* confidence of malicious intent is low
* additional context is required over time
* risk remains within tolerance

Monitoring must have a review timeline.

---

## Escalate Criteria

A signal is escalated when:

* impact may be significant or irreversible
* privileged access is involved
* trust boundaries are crossed
* institutional risk is possible

Escalation transfers accountability.

---

## Triage and False Positives

False positives indicate:

* overly broad hypotheses
* excessive correlation
* missing context

False positives are used to improve detection design,
not to penalize analysts.

---

## Triage Documentation

Every triage decision must record:

* decision taken
* rationale
* owner
* next review or action

Documentation ensures consistency and auditability.

---

## Relationship with Alert Severity

Severity supports triage.
Severity does not replace triage.

High severity does not guarantee escalation.
Low severity does not guarantee closure.

Judgment prevails.

---

## Final Statement

Good triage is quiet, fast, and consistent.

This model exists to ensure that SOC decisions
are trusted by leadership and defensible over time.
