---
mode: agent
description: Compare the spec in /spec to the code in /src and report gaps
---

Compare the requirements in `spec/` to the implementation in `src/` and produce a short gap report.

Steps:
1. List every acceptance criterion scenario in `spec/03-user-stories/` (search for ` ```gherkin ` fences).
2. For each scenario, search `src/` for code that appears to implement it.
3. Produce a Markdown table with columns: **Story | Scenario | Implemented? | Evidence | Gap**.
4. Highlight any scenario that has no matching code as 🔴 and any code in `src/` with no matching spec as 🟡.

Do not modify any files. This is read-only analysis.
