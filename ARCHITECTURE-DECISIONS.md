# ARCHITECTURE DECISIONS — Human SIEM Cybersecurity Operating System

## Why this document exists

This document captures **architecture-level security decisions** made in the Human SIEM operating model.

It answers one question clearly:

> *Why was this designed this way — and would the decision still hold under audit, incident, or leadership scrutiny?*

This is **not** a technical spec.
This is **decision evidence**.

---

## What counts as an Architecture Decision here

An architecture decision is recorded when it:

* Shapes **security posture**, not just implementation
* Introduces or constrains **risk**
* Affects **detection, response, identity, or governance boundaries**
* Would be questioned **months later** by audit, SOC, or leadership

If a decision cannot be defended without tribal knowledge, it belongs here.

---

## Decision Format (Standardized)

Each decision follows this structure:

1. **Context**
2. **Decision**
3. **Rationale**
4. **Alternatives Considered**
5. **Risk Trade-offs**
6. **Validation & Evidence**
7. **Status & Review**

This mirrors how real-world security architecture is evaluated.

---

## AD-001 — Identity as the Primary Control Plane

### Context

Traditional SIEM architectures prioritize logs and network telemetry.
Cloud and SaaS environments shift the real control boundary to **identity and authorization**.

### Decision

Treat **identity (IAM)** as the primary security control plane across detection, validation, and escalation.

### Rationale

* Most high-impact incidents involve identity misuse, not perimeter failure
* Identity events are semantically rich and audit-relevant
* IAM decisions map cleanly to governance and accountability

### Alternatives Considered

* Network-centric detection
* Tool-centric SIEM correlation

Rejected due to poor signal quality and weak audit defensibility.

### Risk Trade-offs

* Reduced visibility into low-level network anomalies
* Strong dependency on IAM telemetry quality

### Validation & Evidence

* Adversarial validation scenarios in `validation/`
* Escalation logic aligned with `soc-alignment/`

### Status

Accepted
Review cycle: Annual or upon major IAM model change

---

## AD-002 — Silence by Design over Alert Exhaustion

### Context

Alert fatigue degrades security outcomes and decision quality.

### Decision

Design detection logic to **optimize for silence**, not volume.

### Rationale

* Silence is a *decision*, not a failure
* Escalation must signal **decision points**, not raw events
* Human attention is a finite security resource

### Alternatives Considered

* Exhaustive alerting with downstream triage
* Tool-default alert thresholds

Rejected due to operational entropy and weak signal-to-noise ratio.

### Risk Trade-offs

* Risk of delayed detection for low-confidence scenarios
* Requires disciplined validation and documentation

### Validation & Evidence

* Detection principles in `ALERT-PHILOSOPHY.md`
* Correlation strategy in `strategy/`

### Status

Accepted
Continuously evaluated via adversarial validation

---

## AD-003 — Decision-to-Evidence over Tool Configuration

### Context

Security tooling changes frequently. Decisions must outlive tools.

### Decision

Document **security decisions**, not tool configurations, as the primary artifact.

### Rationale

* Tools are replaceable; reasoning is not
* Audits assess decisions, not dashboards
* Enables portability across environments

### Alternatives Considered

* Tool-specific documentation
* Detection-rule repositories

Rejected due to fragility and vendor lock-in.

### Risk Trade-offs

* Higher upfront documentation effort
* Requires architectural discipline

### Validation & Evidence

* `audit-ready/` decision logs
* End-to-end example in `examples/decision-end-to-end.md`

### Status

Accepted
Non-negotiable design principle

---

## AD-004 — Explicit Escalation Boundaries

### Context

Ambiguous escalation creates institutional risk.

### Decision

Define **explicit escalation boundaries** between SOC, Security, and Leadership.

### Rationale

* Not all risk is technical risk
* Institutional risk requires executive awareness
* Escalation is a governance act

### Alternatives Considered

* Implicit escalation via severity levels
* Case-by-case judgment

Rejected due to inconsistency and audit exposure.

### Risk Trade-offs

* Potential over-escalation in edge cases
* Requires clear risk posture alignment

### Validation & Evidence

* Escalation criteria in `RISK-POSTURE.md`
* SOC alignment in `soc-alignment/`

### Status

Accepted
Reviewed alongside risk posture updates

---

## How this document is used by reviewers

Recruiters, auditors, and senior engineers should be able to:

* Read **one decision**
* Understand **why it exists**
* See **where it is validated**
* Challenge it — and find an answer

If that fails, the architecture has failed.

---

## Final Statement

> *Good architecture is not about being clever.*
> *It is about being defensible when challenged.*

This document exists to make that defense explicit.
