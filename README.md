> **Start here:** read **[START_HERE.md](./START_HERE.md)** for the 10–15 minute guided tour and evaluation path.

# Human SIEM — Cybersecurity Operating System

This repository documents a **governance-driven cybersecurity operating system**
designed to model how a senior security professional **thinks, decides, and documents risk**.

It is not a collection of tools.
It is a collection of **judgment**.

---

## If you only read one thing

Choose the path that matches **your role**:

### 🛠️ Technical Security (Engineer / Architect / IAM / Detection)

👉 **[examples/decision-end-to-end.md](./examples/decision-end-to-end.md)**
*A complete, end-to-end example of how a security decision is reasoned, validated, governed, and made audit-ready.*

---

### 🧠 Security Leadership (CISO / Head of Security / Manager)

👉 **[ARCHITECTURE-DECISIONS.md](./ARCHITECTURE-DECISIONS.md)**
*Why this security architecture exists, which trade-offs were made, and which alternatives were explicitly rejected.*

---

### 👀 Recruiter / HR / Initial Screening

👉 **[SECURITY-ARCHITECTURE-SNAPSHOT.md](./SECURITY-ARCHITECTURE-SNAPSHOT.md)**
*A one-page explanation of what kind of security system this is — and what kind of professional built it.*

---

## Use This Repository as a Template

This repository is designed to be **forked as a template**, not studied as a static document.

It provides a **replicable, audit-ready framework** for modeling how security decisions are made, validated, and defended under scrutiny.

### Intended Use

* Clone via **“Use this template”**
* Adapt scope (cloud, on-prem, hybrid)
* Produce **defensible decision evidence**, not detections

---

## 15-Minute Evaluation Path (for reviewers)

1. Read **START_HERE.md**
2. Read **SECURITY-ARCHITECTURE-SNAPSHOT.md**
3. Review **ARCHITECTURE-DECISIONS.md**
4. Read the end-to-end example:
   **examples/decision-end-to-end.md**
5. Review one decision in **audit-mapping/**
6. Inspect validation logic in **validation/**
7. Check governance constraints in **GOVERNANCE.md**

This is not a toolset.
It is a **governance operating model**.

---

## Purpose

To demonstrate how cybersecurity excellence is achieved through:

* signal selection over data accumulation
* correlation over isolated alerts
* silence by design over alert fatigue
* audit-ready decision making

---

## What this repository is

* A public, compliant portfolio of cybersecurity reasoning
* A transferable operating model aligned with SOC, Audit, and Leadership
* A documentation-first approach to trust and governance

---

## What this repository is NOT

* No real logs
* No real infrastructure
* No copy-paste detection rules
* No organizational secrets

All examples are abstracted, synthetic, and compliance-safe.

---

## Core Principles

* Identity is the primary control plane
* Every alert must be defensible six months later
* Silence is a security decision
* Automation amplifies thinking — it does not replace it

---

## Structure

* **runbooks/** — enterprise-style operational logic
* **detection-strategy/** — hypothesis and correlation models
* **soc-alignment/** — triage and escalation reasoning
* **audit-ready/** — documentation templates for compliance

---

## Intended Audience

* Security leadership (CISO, Head of Security)
* SOC and Detection Engineering
* Risk, Audit, and Compliance stakeholders

---

**Current roadmap:** v0.2.0 — Cloud Audit & Adversarial Validation
This repository operates under explicit governance principles defined in **GOVERNANCE.md**.

**Maintainer / Original Author:** André Luiz Vieira Bonfim
**Focus:** Cloud Security, SIEM, Governance, Identity, Zero Trust

