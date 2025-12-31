# DETECTION STRATEGY — Correlation Principles

## Purpose

This document defines how events are correlated within the Human SIEM
operating model.

Correlation exists to reduce ambiguity, not to increase complexity.

---

## Correlation Is a Decision, Not a Feature

Correlation is not the act of joining events.
It is the act of deciding which relationships matter.

Every correlation implies intent, cost, and operational impact.
Unnecessary correlation creates noise and erodes trust.

---

## Principle of Minimal Correlation

Correlation must be minimal and intentional.

A valid correlation:

* answers a specific hypothesis
* reduces uncertainty
* supports a clear decision

If correlation does not change the decision outcome,
it should not exist.

---

## Context Over Volume

Correlation prioritizes:

* identity context over event count
* sequence over simultaneity
* behavior over anomalies

More data does not mean more clarity.
Context does.

---

## Temporal Reasoning

Events are correlated based on:

* logical sequence
* realistic adversarial timing
* operational workflows

Artificially tight time windows create false confidence.
Overly broad windows create noise.

Time must reflect plausible behavior.

---

## Cross-Domain Correlation

Cross-domain correlation is applied only when:

* identity links events meaningfully
* behavior crosses trust boundaries
* escalation of privilege or impact is plausible

Blindly correlating domains increases false positives.

---

## Correlation and False Positives

False positives indicate:

* excessive correlation
* missing context
* incorrect assumptions

False positives are design feedback,
not analyst failure.

Correlation must be revised accordingly.

---

## Correlation and Silence

Correlation may result in:

* alert
* continued observation
* intentional silence

Silence after correlation is valid
when uncertainty is sufficiently reduced.

Silence must be documented.

---

## Governance of Correlation Logic

All correlation logic must be:

* documented in purpose
* explainable without tools
* reviewable over time

Correlation that cannot be explained
should not be deployed.

---

## When Not to Correlate

Correlation should not be used when:

* a single event is sufficient
* impact is negligible
* decision is unaffected

More correlation is not better correlation.

---

## Final Statement

Correlation is the art of knowing
what to ignore.

This model exists to ensure that correlation
serves judgment, not complexity.
