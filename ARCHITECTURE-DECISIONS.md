# Architecture Decisions — Human SIEM

## Purpose

This document explains why this security architecture exists,
which decisions were made, and which alternatives were explicitly rejected.

Architecture is not what is built.
Architecture is what is chosen — and what is refused.

---

## Decision 1: Governance before tooling

**Chosen:** Documentation-first security governance
**Rejected:** Tool-first SIEM implementation

**Rationale:**
Tools change. Decisions persist.

Without documented reasoning, security actions cannot be defended during audits, incidents, or leadership reviews.

---

## Decision 2: Silence as a security control

**Chosen:** Silence-by-design detection philosophy
**Rejected:** Alert volume as a proxy for security

**Rationale:**
Excessive alerts dilute attention and accountability.

Silence is acceptable when risk is understood, documented, and monitored.

---

## Decision 3: Identity as the primary control plane

**Chosen:** Identity-centric detection and escalation
**Rejected:** Network-only or perimeter-centric models

**Rationale:**
Modern environments are cloud-native and identity-driven.

Identity events provide the highest signal-to-noise ratio for institutional risk.

---

## Decision 4: Explicit escalation boundaries

**Chosen:** Documented escalation criteria
**Rejected:** Ad-hoc human judgment during incidents

**Rationale:**
When escalation criteria are implicit, responsibility becomes unclear.

Explicit boundaries protect both the organization and the security team.

---

## Decision 5: Audit-ready by default

**Chosen:** Decisions mapped to evidence and rationale
**Rejected:** Retroactive documentation after incidents

**Rationale:**
If a decision cannot be explained six months later, it was never complete.

Audit readiness is a design requirement, not an afterthought.

---

## Architectural Outcome

The result is an operating model where:

* security actions are traceable
* risk ownership is clear
* leadership decisions are supported by evidence
* compliance is a natural by-product

---

## Final Note

This architecture optimizes for trust, clarity, and accountability.

It assumes that the most expensive failure is not a missed alert,
but an **undefensible decision**.


