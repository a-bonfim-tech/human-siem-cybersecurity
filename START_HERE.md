# START HERE — Human SIEM (v0.1.0-alpha)

If you have 10–15 minutes, this file is your guided tour.
This repository is a governance-driven model of how a senior security professional selects signals, validates risk, and documents decisions in an audit-safe way.

Release baseline: **v0.1.0-alpha** (Governance Baseline)

## What you will get from this repository

* A defensible approach to **alert selection** (reduce noise, increase certainty)
* A repeatable model for **SOC decision-making**
* Audit-ready **documentation templates** and **decision logs**
* A compliance-safe portfolio demonstrating security judgment

## What you will NOT find (by design)

* Real logs or organizational data
* Production detection rules or copy-paste queries
* Real infrastructure, credentials, or secrets

All examples are synthetic, abstracted, and compliance-safe.

## 10-minute evaluation path (recommended)

Open these in order:

1. **GOVERNANCE.md**
   Core principles and constraints. This is the control plane.

2. **ALERT-PHILOSOPHY.md**
   How signals are filtered, when silence is a decision, and why “more alerts” is not maturity.

3. **RISK-POSTURE.md**
   Explicit thresholds and escalation logic (what triggers action vs. documentation vs. silence).

4. **runbooks/**
   Operational logic (how decisions are made and documented).

5. **audit-ready/**
   Templates that turn judgment into evidence (post-mortem, decision logs, audit artifacts).

## If you are a recruiter / hiring manager

This repository demonstrates:

* Security judgment under constraints (governance-first)
* Clear scope control and compliance awareness
* Documentation-first operating discipline (audit-ready thinking)
* SOC alignment and decision defensibility over “tool collecting”

Suggested interview prompts:

* “Explain your alert philosophy and why silence can be a security decision.”
* “Walk me through your escalation boundary and how you defend it six months later.”
* “Where do you place the human kill-switch in an incident flow, and why?”

## If you are SOC / Detection Engineering

Use this repo as a decision model:

* How to select signals
* How to validate and correlate
* How to document defensibly
* How to reduce alert fatigue without losing coverage

## Next planned milestone (public roadmap)

* **v0.2.0 – Cloud Audit & Adversarial Validation** (evidence-driven validation model)

---

Author: André Luiz Vieira Bonfim
Focus: Cloud Security, SIEM, Governance, Identity, Zero Trust
