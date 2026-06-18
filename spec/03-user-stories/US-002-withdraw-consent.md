# US-002 · Patient withdraws consent

> **As** the Patient
> **I want** to withdraw my research consent at any time
> **So that** my data stops being used for new research from that point forward.

**Status:** 🟡 In refinement — needs acceptance criteria
**Owner (BA):** BA Lead
**Persona:** [The Patient](../02-personas.md#-the-patient)

---

## Context

A patient must be able to withdraw consent through any channel they used to give it (clinician, phone, paper). Withdrawal must propagate to all downstream systems quickly enough that the next research extract cannot include the patient.

## Acceptance criteria

```gherkin
Feature: Withdraw a research consent

  Scenario: Happy path — patient withdraws via clinician channel
    Given the Patient has an active research consent on file
      And the Clinician confirms the Patient's identity
     When the Clinician records a withdrawal request for research consent
     Then the consent status is updated to "Withdrawn"
      And the withdrawal is visible to all downstream systems before the next scheduled research extract starts
      And an audit entry is written with who recorded the withdrawal, when, and through which channel

  Scenario: Withdrawal is accepted through any previously used channel
    Given the Patient has an active research consent on file
      And the Patient has previously used one of these channels: clinician, phone, or paper
     When a withdrawal request is received through that same channel
     Then the withdrawal is accepted and recorded
      And the consent status is updated to "Withdrawn"
      And the withdrawal is visible to all downstream systems before the next scheduled research extract starts

  Scenario: Edge case — withdrawal request is received just before an extract
    Given the Patient has an active research consent on file
      And the next scheduled research extract has not started yet
     When a withdrawal request is recorded
     Then the Patient is excluded from that next research extract
      And the consent status remains "Withdrawn" for future extracts
```

## Open questions

- [ ] Does withdrawal apply retroactively to extracts already produced?
- [ ] Who is notified when a patient withdraws (treating clinician? Research office?)
