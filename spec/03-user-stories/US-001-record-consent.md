# US-001 · Clinician records a research consent

> **As** the Clinician
> **I want** to record a patient's verbal consent for research data sharing in under a minute
> **So that** the patient's consent state is portable, auditable, and visible to downstream systems immediately.

**Status:** 🟢 Ready for dev
**Owner (BA):** BA Lead
**Owner (Dev):** _tbd_
**Persona:** [The Clinician](../02-personas.md#-the-clinician-primary-user)

---

## Context

Today the Clinician writes the consent on a paper form, which is later scanned into the patient's EHR. The scan is not machine-readable, so research extracts cannot rely on it. This story replaces that paper form for the **research data sharing** consent type only (see [Overview · In scope](../01-overview.md#in-scope-trial)).

## Acceptance criteria

```gherkin
Feature: Record a research consent

  Scenario: Happy path — clinician captures a fresh consent
    Given the Clinician is logged in via EHR SSO
      And a Patient is selected as the active patient
      And the Patient has no existing research consent on file
     When the Clinician selects "Record consent" → "Research data sharing"
      And confirms the Patient consented verbally with a witness present
      And submits the form
     Then a consent record is created with status "Active"
      And the record is timestamped to the second
      And the record is visible to the Data Custodian API within 15 seconds
      And an audit entry is written with the Clinician's identity and the timestamp

  Scenario: Patient already has an active consent
    Given the Patient has an active research consent recorded yesterday
     When the Clinician opens "Record consent" → "Research data sharing"
     Then they see a notice: "This patient already has an active research consent from 13 May 2026"
      And they are not allowed to create a duplicate
      And they are offered options: "View" or "Withdraw"

  Scenario: SSO unavailable
    Given the EHR SSO service is unreachable
     When the Clinician navigates to "Record consent"
     Then they see a clear message: "Sign-in is temporarily unavailable. Please try again or use the paper backup workflow."
      And no consent can be captured in this state
```

## Non-functional notes

- Page must be usable on a hospital workstation running Edge 110+.
- All consent captures must complete a round-trip in < 2 seconds on the corporate network.
- No PHI in URLs or query strings.

## Linked artefacts

- [ADR-001 · We use EHR SSO, not stand-alone identity](../99-decisions/ADR-001-identity.md)
- Open question: Do we need offline capture? — see [Overview](../01-overview.md#open-questions)
