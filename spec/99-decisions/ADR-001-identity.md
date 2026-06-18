# ADR-001 · We use EHR SSO, not stand-alone identity

**Status:** Accepted
**Date:** 2026-05-08
**Deciders:** BA Lead, Solution Architect, Microsoft Solution Specialist

## Context

The trial needs an identity solution for clinicians. We have two options:

1. **Re-use EHR SSO** — clinicians are already signed in to the EHR; piggy-back on that session.
2. **Stand-alone identity** — issue separate credentials for the consent service.

## Decision

We will **re-use EHR SSO** for the trial.

## Consequences

- ✅ Zero new credentials for clinicians — removes the biggest adoption blocker identified in BA interviews.
- ✅ Audit identity matches EHR identity, simplifying reconciliation.
- ⚠️ The consent service is unavailable when EHR SSO is down (see US-001 SSO unavailable scenario).
- ⚠️ Phase 2 patient-facing flows will need a different identity source — re-open this ADR at that point.
