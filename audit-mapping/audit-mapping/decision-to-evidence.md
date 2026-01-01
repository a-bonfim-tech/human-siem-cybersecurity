# Decision-to-Evidence Mapping — Human SIEM (v0.2.0)

This document maps **security decision types** to the **minimum evidence** required to defend them under audit, legal, or leadership scrutiny.

A decision without evidence is an opinion.
An action without evidence is a liability.

---

## Decision Type 1 — Document-Only (Silence-by-Design)

### Decision Description

A signal is observed, assessed, and intentionally **not escalated**.

### Evidence Required

* Timestamped decision log entry
* Signal summary (what was observed)
* Explicit rationale for non-escalation
* Reference to risk posture or policy threshold

### Audit Question Answered

“Why did you not act?”

### Failure Condition

Missing rationale or undocumented silence.

---

## Decision Type 2 — Validation (Increase Certainty)

### Decision Description

Additional data is collected to reduce uncertainty before escalation.

### Evidence Required

* Initial signal record
* Validation hypothesis (what is being tested)
* Additional signals collected
* Outcome (confidence increased or decreased)

### Audit Question Answered

“What did you do to become more certain?”

### Failure Condition

Validation performed without a stated hypothesis.

---

## Decision Type 3 — Escalation (Formal Handoff)

### Decision Description

Risk crosses a defined threshold and is escalated to another role or process.

### Evidence Required

* Escalation trigger (policy, impact, confidence, time)
* Evidence bundle summary
* Decision log entry
* Receiving party acknowledgment

### Audit Question Answered

“Why was this escalated, and to whom?”

### Failure Condition

Escalation without clear authority or trigger.

---

## Decision Type 4 — Non-Escalation After Validation

### Decision Description

Validation confirms the signal does not warrant escalation.

### Evidence Required

* Validation results
* Explicit closure decision
* Reference to thresholds not crossed

### Audit Question Answered

“Why did this stop here?”

### Failure Condition

Closure without documented justification.

---

## Decision Type 5 — Stop / Kill-Switch Activation

### Decision Description

Human intervention halts automation or response actions.

### Evidence Required

* Stop condition description
* Authority invoking the stop
* Risk of continuation vs. halt
* Follow-up action plan

### Audit Question Answered

“Who stopped this, and why was it necessary?”

### Failure Condition

Untraceable or unauthorized stop actions.

---

## Cross-Cutting Evidence Principles

* Evidence must be **contemporaneous**, not reconstructed.
* Evidence must reflect **reasoning**, not just outcomes.
* Absence of evidence defaults to process failure.

---

## Summary Principle

> Security maturity is measured not by how fast you act,
> but by how well you can explain your actions later.

This mapping ensures every Human SIEM decision
produces evidence proportional to its impact.

---

Author: André Luiz Vieira Bonfim
Model: Human SIEM — Audit-Mapped Decisions
