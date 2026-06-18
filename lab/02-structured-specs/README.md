# Section 2 · Structured specs (markdown spec kit)

⏱ **15 minutes** · 🎯 Use the templates to write your Overview and your first Persona, by hand. No Copilot yet.

## Why we start without Copilot

You'll meet Copilot in section 3. We start by hand for one minute so you feel that **editing a Markdown file is just typing in a wiki page**. Once that's anchored, the AI feels like an assistant, not a black box.

## What's in the spec kit

Open these files in github.dev (left-side file tree) and look at each one:

| File | What it's for |
|---|---|
| `spec/_templates/user-story.md` | Blank user-story template |
| `spec/_templates/decision.md` | Blank ADR template |
| `spec/_templates/persona.md` | Blank persona template |
| `spec/01-overview.md` | Example Overview ("what good looks like") |
| `spec/02-personas.md` | Example personas |
| `spec/03-user-stories/US-001-record-consent.md` | Example fully-formed story |
| `spec/99-decisions/ADR-001-identity.md` | Example architecture decision |

## Step 1 · Replace the example Overview with your own (8 min)

1. In github.dev, open `spec/01-overview.md`.
2. **Replace** the example content with content describing the requirement from your Issue (the one you pasted in section 1).
3. Keep the structure (problem · in scope · out of scope · success measures · open questions) — this discipline is what makes a spec useful to devs and QA later.
4. Save (`Ctrl+S`). The preview updates live.

> 💡 **Tip:** open the Markdown preview alongside the source (`Ctrl+Shift+V`) — you write on the left, the rendered page appears on the right. Same as Confluence's edit/view modes.

## Step 2 · Add a new Persona (5 min)

1. Open `spec/02-personas.md`.
2. Add a new section using `## ` and the persona template. Pick one of the personas from your real org if you can.
3. Save.

## Step 3 · Notice what you've gained (2 min)

- Your spec is **versioned** — every save is tracked.
- It's **searchable** — `Ctrl+Shift+F` finds anything across all pages.
- It's **linkable** — type `[[` and pick another page (Foam wiki-links work in your fork too).
- It's **portable** — anyone with access to your repo sees the same thing.

## Checkpoint ✅

- [ ] `spec/01-overview.md` is filled with your own requirement.
- [ ] `spec/02-personas.md` has at least one new persona you wrote.
- [ ] React 👍 in the lab chat.

> ➡️ Next: [03 · Refine with Copilot](../03-refine-with-copilot/) — the part you came for.
