---
mode: ask
description: Rewrite the selected prose as Gherkin acceptance criteria
---

Take the prose I have selected (or the paragraph nearest my cursor) and rewrite it as Gherkin acceptance criteria.

Rules:
- Use the same style as the existing scenarios in `spec/03-user-stories/US-001-record-consent.md`.
- One Feature, multiple Scenarios. Always include at least one edge case.
- Output inside a fenced ` ```gherkin ` block, ready to paste into a user story.
- If anything in the prose is ambiguous, list it as an "Open question" bullet under the Gherkin block instead of guessing.
- Do not invent NFRs (performance, security) unless the prose explicitly mentions them.
