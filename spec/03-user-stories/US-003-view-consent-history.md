# US-003 · Clinician views a patient's consent history

> **As** the Clinician
> **I want** to view a patient's consent history in one place
> **So that** I can explain the current consent state and prior changes clearly at the point of care.

**Status:** 🟡 Draft
**Owner (BA):** BA Lead
**Owner (Dev):** _tbd_
**Persona:** [The Clinician](../02-personas.md#-the-clinician-primary-user)

---

## Context

Today, consent details are split across screens and scanned notes, so the Clinician cannot quickly confirm what happened and when. This creates delays and uncertainty when discussing consent with the Patient. This story provides a single, readable history view for research consent events so the Clinician can make decisions confidently in real time.

## Acceptance criteria

```gherkin
Feature: View a patient's consent history

  Scenario: Happy path - clinician sees full consent timeline
    Given the Clinician is logged in via EHR SSO
      And a Patient is selected as the active patient
      And the Patient has at least one research consent event on file
     When the Clinician opens "Consent history"
     Then they see a timeline of research consent events in reverse chronological order
      And each event shows status, channel, who recorded it, and timestamp
      And the current consent state is clearly shown at the top

  Scenario: Edge case - patient has no consent history
    Given the Clinician is logged in via EHR SSO
      And a Patient is selected as the active patient
      And the Patient has no research consent events on file
     When the Clinician opens "Consent history"
     Then they see a clear message: "No research consent history is recorded for this patient"
      And they are offered the option to "Record consent"
```

## Non-functional notes

- Consent history must load in under 2 seconds on the hospital network.
- The timeline must be readable on standard hospital workstation screens.
- No patient identifiers are shown in URLs.

## Linked artefacts

- [US-001 · Clinician records a research consent](./US-001-record-consent.md)
- [US-002 · Patient withdraws consent](./US-002-withdraw-consent.md)
- [ADR-001 · We use EHR SSO, not stand-alone identity](../99-decisions/ADR-001-identity.md)

## Open questions

- [ ] Should the history include who witnessed a verbal consent event?
- [ ] Should clinicians be able to export or print the consent history for the patient record?
