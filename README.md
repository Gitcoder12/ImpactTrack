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

## Branch Activity & Development History

**Audit date:** 2026-11-18 · **Comparison base:** `main`

| Branch | Difference from `main` | Observed work / changed paths |
|---|---:|---|
| `docs/portfolio-operating-kit-2026-11-13` | 5 ahead / 3 behind | Activity log, agent guidance, worklog, company-fit notes, feature plan and skills; README has additions and removals |
| `docs/project-status-audit20261116` | Comparison unavailable | GitHub returned 404 for the comparison; recheck branch existence |

### Open pull requests observed during this audit

- [PR #2 — project status snapshot](https://github.com/Gitcoder12/ImpactTrack/pull/2)
- [PR #1 — project handbook and data integrity roadmap](https://github.com/Gitcoder12/ImpactTrack/pull/1)

**Review note:** The portfolio branch includes README removals as well as additions. Inspect its diff before merging. No branches have been merged or deleted by this documentation update.
