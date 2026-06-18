# Overview — Patient Consent Service

> [!NOTE]
> This page describes *what we're building and why*. It is the first page a new joiner should read.

## The problem

Clinicians currently capture patient consent on paper or inside disconnected EHR modules. This creates three pain points:

1. **Consent records are not portable** between facilities — a patient consenting at Hospital A cannot have that consent honoured at Hospital B without a phone call.
2. **Withdrawal of consent is invisible** to downstream systems. A patient who withdraws consent today may still appear as "consented" in research extracts pulled next month.
3. **Audit is manual** — proving a specific consent was in force at a specific moment in time currently requires a Records request.

## In scope (trial)

- Capture consent for **research data sharing** only (one consent type to start).
- Single facility (Hospital A) for the trial.
- Web UI for clinicians; read-only API for downstream systems.

## Out of scope

- Patient-facing app — phase 2.
- Bulk-import of existing paper consents — phase 2.
- Consent for treatment, surgery, imaging — separate workstream.

## Success measures

| Measure | Target |
|---|---|
| Time to record a consent | < 60 seconds |
| Time to look up a current consent | < 5 seconds |
| Consent withdrawals propagated to downstream systems | within 15 minutes |
| Audit trail completeness | 100% of state changes |

## Personas in play

See [Personas](./02-personas.md).

## Open questions

- [ ] Do we need offline capture (paper backup workflow)?
- [ ] Identity: re-use EHR SSO or stand alone?
- [ ] Retention: how long do we keep withdrawn consents for audit?
