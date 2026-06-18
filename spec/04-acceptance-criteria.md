# Acceptance criteria — index

Each user story owns its own Gherkin scenarios. This page is just an index so QA can find them all in one place.

| Story | Scenarios |
|---|---|
| [US-001 Record consent](./03-user-stories/US-001-record-consent.md) | Happy path · Duplicate consent · SSO unavailable |
| [US-002 Withdraw consent](./03-user-stories/US-002-withdraw-consent.md) | _to be drafted_ |

---

## Conventions

- Use **Gherkin** (`Given / When / Then`) inside a fenced ` ```gherkin ` block. This renders nicely and is parseable by test tools.
- One **Feature** per user story file.
- Every **Scenario** must be runnable as a manual test by a human reading only the spec.
- Never reference UI widgets ("the blue button") — describe the user's intent ("submits the form").
