# ImpactTrack — Feature Upgrade Plan

## Objective

A prototype data model for showing how charitable causes, funding targets, donations and progress updates could be recorded transparently.

## P0 — data integrity and trust

- [ ] Define source, beneficiary verification state, currency, timezone, update date and evidence fields for each cause/progress record.
- [ ] Label every bundled record and amount as illustrative; do not imply real donations or verified impact.

## P1 — basic user workflow

- [ ] Add schema validation and correction history for cause and progress records.
- [ ] Create a read-only cause explorer with transparent funding-target and progress calculations.

## P2 — verification and transactions

- [ ] Add evidence review states and audit trails before allowing public contribution records.
- [ ] Only consider payment integration after legal, security, accounting and beneficiary verification requirements are defined.

## Collaborator work packages

1. Cause/progress schema and units.
2. Verification states, provenance and correction history.
3. Read-only catalogue and transparent progress calculations.
4. Security/legal requirements analysis before any payment feature.

## Definition of done

- [ ] Sample data are visibly marked as illustrative.
- [ ] Money amounts include currency and clear status (target, pledge, donation).
- [ ] Progress updates include sources, dates and verification state.
- [ ] No payment capability is claimed unless implemented and reviewed.
