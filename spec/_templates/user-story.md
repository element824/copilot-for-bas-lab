# US-XXX · {{Short title in present tense}}

> **As** {{persona — link to /spec/02-personas.md}}
> **I want** {{capability in user-facing language}}
> **So that** {{measurable outcome / value}}

**Status:** 🟡 Draft
**Owner (BA):** {{name}}
**Owner (Dev):** _tbd_
**Persona:** [{{persona name}}](../02-personas.md)

---

## Context

{{2–4 sentences. What is the current pain? What part of the [Overview](../01-overview.md) does this address?}}

## Acceptance criteria

```gherkin
Feature: {{Feature name matching the story title}}

  Scenario: {{Happy path name}}
    Given {{precondition}}
     When {{action}}
     Then {{observable outcome}}
      And {{additional observable outcome}}

  Scenario: {{Edge case or error path}}
    Given {{precondition}}
     When {{action}}
     Then {{observable outcome}}
```

## Non-functional notes

- {{Performance / accessibility / security constraints, if any}}

## Linked artefacts

- {{Link to ADRs, related stories, mockups}}

## Open questions

- [ ] {{Question 1}}
