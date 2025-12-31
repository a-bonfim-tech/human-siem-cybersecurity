# DETECTION STRATEGY — Hypothesis Model

## Purpose

This document defines how detection hypotheses are formulated within
the Human SIEM operating model.

Detections are not created from tools or data availability.
They are created from hypotheses about adversarial behavior.

---

## Detection Begins with a Question

Every detection starts with a question, not a signal.

Examples:

* What would abuse look like if this control failed?
* How would an attacker remain unnoticed here?
* What behavior would precede irreversible damage?

If no meaningful question exists, detection should not exist.

---

## Hypothesis-Driven Detection

A detection hypothesis describes:

* a plausible adversarial goal
* a sequence of behaviors required to achieve it
* the constraints the attacker must operate under

Hypotheses are written in natural language
before any technical implementation.

---

## Structure of a Detection Hypothesis

Each hypothesis must include:

1. **Intent**
   What the adversary is trying to achieve.

2. **Behavior**
   Observable actions required to reach that goal.

3. **Context**
   Identity, environment, and timing assumptions.

4. **Impact**
   Why this behavior matters to the organization.

5. **Decision Expectation**
   What action or decision the detection should trigger.

If any element is missing, the hypothesis is incomplete.

---

## From Hypothesis to Signal

Signals are selected only after the hypothesis is clear.

Signals must:

* reduce uncertainty about the hypothesis
* be observable with available telemetry
* provide context, not just confirmation

Data availability does not justify detection creation.

---

## Avoiding Tool-Driven Detection

Detections must never exist because:

* the tool supports it
* the vendor recommends it
* the data is easy to collect

Tool-driven detection creates noise without meaning.

Hypothesis-driven detection creates trust.

---

## Validation and Refinement

Hypotheses are refined through:

* false positive analysis
* contextual enrichment
* operational feedback from SOC

A hypothesis that produces persistent noise
must be revised or discarded.

---

## Documentation and Governance

Every hypothesis must be documented with:

* its rationale
* assumptions made
* known limitations
* review cadence

Undocumented hypotheses are unmanaged risk.

---

## When Not to Create a Hypothesis

A hypothesis should not be created when:

* the impact is negligible
* no meaningful decision would result
* behavior is already covered by stronger controls

Not detecting is a valid design choice.

---

## Final Statement

Detection engineering is not about finding everything.
It is about asking the right questions.

This model exists to ensure that detections
are born from reasoning, not reflex.
