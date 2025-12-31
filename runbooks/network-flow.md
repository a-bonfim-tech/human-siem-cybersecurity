# RUNBOOK — Network Flow

## Purpose

This runbook defines how network flow data is interpreted and governed
within the Human SIEM operating model.

The objective is to understand behavior across trust boundaries,
not to inspect packets indiscriminately.

---

## Scope

This runbook applies to:

* network flow logs
* firewall allow/deny events
* ingress and egress traffic
* inter-segment communication

It does not cover:

* deep packet inspection
* payload analysis
* application-layer logic without network relevance

---

## Core Assumptions

* Network traffic gains meaning only through context
* East–west traffic is as critical as north–south
* Exfiltration and command-and-control rely on persistence, not volume

Network signals are interpreted behaviorally, not statistically alone.

---

## Signals Observed (Abstract)

The following signal categories are monitored:

* unexpected egress destinations
* changes in communication patterns
* traffic crossing trust boundaries
* repeated connection attempts
* long-lived or periodic outbound connections

Signals are evaluated over time, not in isolation.

---

## Decision Logic

### Observe

Network activity is observed without alerting when:

* traffic patterns are consistent with baseline
* destinations are known and justified
* communication occurs within expected segments
* volume and timing are explainable

Observation decisions must be documented.

---

### Alert

An alert is triggered when:

* new or rare destinations appear unexpectedly
* communication crosses sensitive boundaries
* traffic patterns suggest command-and-control
* data movement deviates from expected behavior

Alerts must clearly state:

* source and destination context
* why the pattern is unusual
* potential data or control impact

---

### Act

Immediate action is taken when:

* active exfiltration is suspected
* command-and-control persistence is detected
* segmentation controls are bypassed
* network behavior enables lateral movement

Actions may include:

* traffic blocking
* network isolation
* rate limiting
* incident response escalation

---

## Escalation

Escalation occurs when:

* data exposure is possible
* containment impacts availability
* attribution or intent remains unclear
* regulatory or contractual boundaries are crossed

Escalation shifts accountability to leadership.

---

## False Positives and Silence

False positives are mitigated by:

* improving baseline definitions
* refining segment expectations
* correlating with identity and workload context

Silence is acceptable when:

* traffic behavior is well understood
* compensating controls exist
* risk remains within tolerance

Silence decisions must be documented.

---

## Audit Notes

For every network-related decision, the following must be explainable:

* why the traffic was considered acceptable or risky
* how baseline was defined
* what controls mitigated the risk
* who owned the decision

Network flow analysis must withstand post-incident scrutiny.

---

## Final Statement

Networks do not attack systems.
Behaviors do.

This runbook exists to ensure that network visibility
supports judgment, not noise.
