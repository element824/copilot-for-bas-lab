# Section 3 · Refine requirements with Copilot ⭐

⏱ **20 minutes** · 🎯 Generate a user story end-to-end with Copilot, including Gherkin acceptance criteria.

## What you'll do

1. Watch the facilitator demo prose → Gherkin (5 min).
2. **You drive:** generate a brand-new user story using Copilot + the template (10 min).
3. **You drive:** highlight prose and ask Copilot to rewrite it as Gherkin (3 min).
4. Checkpoint and one or two volunteers share-screen (2 min).

## The two prompts that change everything

### Prompt A — generate a story from scratch

Open Copilot Chat (`Ctrl+Alt+I` in VS Code, or the chat icon in the sidebar) and paste:

```
Create a new user story for: "<your topic here>".

Use the template at spec/_templates/user-story.md.
Use a persona from spec/02-personas.md.
Match the voice and Gherkin style of spec/03-user-stories/US-001-record-consent.md.

Save it as spec/03-user-stories/US-XXX-<short-kebab-title>.md (pick the next free number).
```

> Replace `<your topic here>` with something like *"clinician views a patient's consent history"* or pick from the [topic ideas](#topic-ideas-if-you-need-one) below.

### Prompt B — turn prose into Gherkin

Highlight a paragraph of context in any user story and ask Copilot:

```
Rewrite this as Gherkin acceptance criteria following the style used in
spec/03-user-stories/US-001-record-consent.md.

Include at least one happy path and one edge case.
If anything is ambiguous, list it as an "Open question" bullet under the
Gherkin block instead of guessing.
```

## What to look for

- **Copilot reads your repo.** It uses your template, your persona names, your existing voice. It is not generating generic content.
- **It surfaces ambiguity, not invents answers.** If you give it loose prose, it will list "open questions" rather than make assumptions. That's the BA-grade behaviour you want.
- **It can be wrong.** Treat the output like a junior BA's first draft — review every line. Edit. Make it yours.

## Topic ideas (if you need one)

- Clinician views a patient's consent history
- Patient withdraws consent via a phone call
- Data custodian runs a research extract that excludes withdrawn consents
- Clinician records a witness statement for an identity-verification override
- Audit officer exports the full audit log for a date range

## Step-by-step (10-minute hands-on)

1. Pick a topic.
2. Open Copilot Chat.
3. Paste **Prompt A** with your topic filled in. Press Enter.
4. Wait for Copilot to write the file. It may stream the response — watch it appear.
5. Open the new file in the file tree. Read it. Edit one or two sentences so it's *your* document, not Copilot's.
6. Save.
7. Highlight the **Context** paragraph. Paste **Prompt B**. Press Enter.
8. Paste the Gherkin block back into the file under "Acceptance criteria". Save.

## Common gotchas

| You see | Why | What to do |
|---|---|---|
| Copilot makes up a persona | Your file didn't load into context | Open `spec/02-personas.md` once, then re-run |
| Output is too generic | Topic was too vague | Add 1–2 lines of context to your prompt |
| Copilot "saved" the file but it's not in the tree | It actually proposed code, not saved | Click "Apply" or copy/paste manually |

## Checkpoint ✅

- [ ] You have a new user-story file in `spec/03-user-stories/` with your name on the topic.
- [ ] It has Gherkin acceptance criteria, including at least one edge case.
- [ ] You edited at least one line so it's truly yours.
- [ ] React 👍 in the lab chat.

> ➡️ Next: [04 · Change management](../04-change-management/) — make it a "page review".
