# Control Assumptions — Human SIEM (v0.2.0)

This document enumerates the **explicit assumptions** required for the Human SIEM operating model to function as intended.

Security decisions are only as strong as the assumptions beneath them.
Undocumented assumptions are hidden failure modes.

---

## Assumption 1 — Identity Signals Are Trustworthy

### Description

Identity telemetry (authentication, authorization, role context) is assumed to be:

* timely,
* accurate,
* complete enough to support correlation.

### Why This Matters

Identity is treated as the primary control plane.
Most escalation decisions depend on identity context.

### Failure Mode

* Logs are delayed, incomplete, or spoofed.
* Privilege context is stale or misclassified.

### Impact

False confidence → incorrect escalation or dangerous silence.

### Mitigation

* Validate identity signal freshness.
* Cross-check identity signals with independent sources.
* Escalate uncertainty, not assumptions.

---

## Assumption 2 — Governance Rules Are Known and Stable

### Description

Escalation policies, risk posture, and authority boundaries are:

* documented,
* accessible,
* understood by operators.

### Why This Matters

Escalation decisions depend on explicit authorization thresholds.

### Failure Mode

* Policies change silently.
* Operators rely on tribal knowledge.

### Impact

Unauthorized escalation or delayed response due to ambiguity.

### Mitigation

* Centralize governance artifacts.
* Treat unknown policy state as a stop condition.

---

## Assumption 3 — Silence Is an Accepted Outcome

### Description

The organization accepts that **not escalating** can be a correct security decision.

### Why This Matters

Silence-by-design is core to noise reduction and trust preservation.

### Failure Mode

* Cultural pressure to “always act”.
* Metrics reward volume over judgment.

### Impact

Alert fatigue, erosion of SOC credibility, audit noise.

### Mitigation

* Document non-escalations explicitly.
* Protect analysts from volume-driven incentives.

---

## Assumption 4 — Decisions Will Be Audited Later

### Description

All decisions are made under the assumption of **future scrutiny**.

### Why This Matters

Audit defensibility shapes how decisions are documented today.

### Failure Mode

* Documentation is skipped under time pressure.
* Decisions rely on undocumented intuition.

### Impact

Inability to justify actions months later.

### Mitigation

* Enforce decision logging as part of the workflow.
* Treat undocumented action as a process failure.

---

## Assumption 5 — Adversaries Exploit Ambiguity First

### Description

Attackers are assumed to exploit:

* unclear authority,
* delayed decisions,
* undocumented boundaries.

### Why This Matters

Ambiguity is a security weakness, not a neutral state.

### Failure Mode

* Gray areas persist without ownership.
* Escalation boundaries are informal.

### Impact

Adversarial dwell time increases without detection.

### Mitigation

* Make boundaries explicit.
* Assign ownership to ambiguity.

---

## Summary Principle

> A security model that does not document its assumptions
> cannot reason about its own failure.

Every assumption above must be periodically challenged,
or the Human SIEM model degrades silently.

---

Author: André Luiz Vieira Bonfim
Model: Human SIEM — Assumption-Aware Security
