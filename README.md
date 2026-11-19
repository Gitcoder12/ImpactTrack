# ImpactTrack

ImpactTrack is a transparency layer for charitable giving.
It enables tracking of donations, fund allocation, and real-world impact through structured updates.

---

## Overview

The platform connects donors with verified causes and provides visibility into how funds are used over time.

---

## Core Features

* Cause listing with basic verification
* Donation tracking per user and per project
* Impact updates (text, images, progress)
* Simple dashboard for activity and history

---

## MVP Scope

* Static or seeded causes
* Simulated or external payment flow
* Manual impact updates
* Basic user profiles

---

## Architecture (planned)

Frontend:

* React / Next.js

Backend:

* Firebase (Auth, Firestore) or Supabase

Data:

* Users
* Causes
* Donations
* Updates

---

## Key Concepts

* **Cause**: A project or initiative requesting support
* **Donation**: A transaction linked to a user and cause
* **Update**: Proof of progress or fund usage
* **Tracking**: Mapping donations to visible outcomes

---

## Future Enhancements

* Payment integration (Stripe / Razorpay)
* Verification workflows (KYC / admin approval)
* Real-time updates and notifications
* Public impact timelines
* Analytics and reporting

---

## Status

Early-stage MVP in development

---

## Goal

Provide a simple, extensible foundation for transparent donation tracking.


---

## AI-maintained project notes (secondary — 2026-11-13)

This section supplements the maintainer-authored README above. The original text has been restored verbatim from Git-history baseline `3a0533b97a7843002a3f1f87c9ce8a6183a25835`; this addendum does not replace or certify the original claims.

- The source tree, runtime data and tests are the implementation source of truth. Do not treat roadmap items, draft PRs or AI-generated descriptions as shipped features.
- Preserve existing maintainer-provided data. Never replace real data with synthetic or placeholder records. Any test fixture must be clearly labelled and isolated from runtime data.
- Mark unverified sources, IDs, records, metrics and external claims as unknown/unverified rather than guessing.
- Verify installation, execution, tests and public claims against the exact current commit before presenting this project to recruiters, researchers or professors.
- See [MODEL_AUDIT_ROUTER.md](MODEL_AUDIT_ROUTER.md) for the independent multi-model review and merge gate.

---

## Engineering Audit & Handover — 2026-11-17

**Review scope:** default branch `main`; static inspection of `causes.json`. Runtime tests were not executed.

### Confirmed findings
- The inspected file contains three cause records with funding goals, raised amounts, and progress updates.
- Two records set `verified: true`, but the inspected JSON does not include verification evidence, verifier identity, verification date, or source links.
- The figures and progress updates therefore cannot be independently substantiated from this file alone. Do not present them as verified real donations or impact.

### Next actions
1. Label current records as demo/sample data unless independently substantiated.
2. Add a verifiable audit trail: evidence URLs/documents, verifier, timestamp, and verification status.
3. Separate payment-provider transaction records from manually entered progress; add tests for amount validation and status transitions.

**Verification status:** data-file inspection only; payment flow, persistence, and tests remain unverified.

---

## Examples Used
- Tracking donations to a community water project
- Following fund allocation for disaster relief
- Recording evidence-backed project progress


---

## Comparison with Existing Open-Source Projects

ImpactTrack is described as a transparency layer for charitable giving: causes, donations, fund allocation and progress updates. These projects are adjacent references, not proof that ImpactTrack already provides equivalent payment or verification capabilities.

| Project | Established focus | Relationship to ImpactTrack |
|---|---|---|
| [Open Collective](https://github.com/opencollective/opencollective) | Open-source collective funding, contributions and transparent financial activity | A mature reference for contribution records and public financial transparency; ImpactTrack's stated emphasis is linking individual donations to cause-level progress evidence. |
| [CiviCRM](https://github.com/civicrm/civicrm-core) | Open-source constituent relationship management, fundraising and contribution management | Much broader fundraising/CRM system; ImpactTrack aims for a narrower donor-facing impact timeline. |
| [Mautic](https://github.com/mautic/mautic) | Open-source marketing automation and contact engagement | Adjacent donor-engagement tooling, not a direct donation-audit or impact-verification equivalent. |

### Where ImpactTrack is different
- **Donation-to-outcome narrative:** the product concept links a contribution to subsequent, dated project updates rather than stopping at a payment receipt.
- **Cause-level progress view:** the intended interface makes allocation and progress understandable to donors in one place.
- **Small, focused experience:** the documented MVP is narrower than a full CRM or fundraising suite.

### Where established projects are stronger
Open Collective and CiviCRM have much more mature financial workflows and ecosystems. ImpactTrack's README describes an early-stage MVP with seeded/demo causes and a simulated or external payment flow; it must not claim real donation processing, verified fund allocation or independently confirmed impact until those integrations and audit trails exist.

### Evidence and trust requirements
For every real cause, publish the verification method, verifier, date, source evidence, transaction reference where appropriate, and correction history. Clearly distinguish payment-provider confirmation from manually entered progress updates. This comparison is based on documented scope, not a security, payment-compliance or feature-parity audit.
