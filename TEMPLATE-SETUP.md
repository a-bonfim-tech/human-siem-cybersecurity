# Template Setup Guide

Follow these steps immediately after creating a repository from this template.

## Step 1 — Rename and Scope

* Rename the repository to reflect your environment
* Define scope: cloud, on-prem, hybrid
* Declare exclusions explicitly

## Step 2 — Define Risk Posture

Edit `RISK-POSTURE.md`:

* Tolerance thresholds
* Escalation boundaries
* Assumptions

No undefined risk posture is allowed.

## Step 3 — Create First Decision

* Add one decision entry under `audit-mapping/`
* State the hypothesis
* Attach minimum required evidence
* Declare whether escalation occurred or not

## Step 4 — Run Validation

* Select one scenario from `validation/`
* Confirm whether confidence increased or decreased
* Record outcome

## Step 5 — Publish Evidence

* Open a pull request
* Merge with a clear commit message
* Reference the decision and validation performed

If you cannot complete this process, the framework is not yet operational.
