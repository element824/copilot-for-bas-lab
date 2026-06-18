# Section 5 · End-to-end — requirement → spec → artefact

⏱ **10 minutes** · 🎯 Tie your Issue, Spec and PR together so the loop is closed.

## The closing wow

The structural shift Confluence cannot give you is **traceability across the whole loop**. By the end of this section your fork will demonstrate:

```
Issue (#1)  ──linked-to──▶  Spec page (US-XXX)  ──published-via──▶  PR  ──auto-closes──▶  Issue
```

When your **Issue closes itself** because a **PR merged**, you've crossed a line: the requirement, the spec and the change record are no longer three documents — they're one trace.

## Step 1 · Link your PR to your Issue (3 min)

1. Open the PR you merged in section 4.
2. Click **Edit** on the description.
3. Add a line: `Closes #1` (replace `1` with your Issue number from section 1).
4. Save the description.

> If you already merged before adding this, no problem — open the Issue and **manually close it**. In future PRs, add `Closes #N` upfront and GitHub does it for you.

## Step 2 · Watch the board update (2 min)

1. Open your **Project board**.
2. Refresh. The Issue card should have moved to **Done**.
3. *That movement happened because of a Markdown change. Your board status now reflects spec reality, automatically.*

## Step 3 · Spec ↔ Code, the director moment (3 min)

This is what you'll show the director when they ask "is this real?".

1. Open Copilot Chat.
2. Paste:

```
Does the code in /src implement the requirement in
spec/03-user-stories/US-001-record-consent.md?

Be honest. List gaps. Don't invent code that doesn't exist.
```

3. Copilot will tell you the spec exists but no implementing code is present (because `/src/` is empty for the lab).
4. **In your real trial**: when devs add real code to `/src/`, this same prompt becomes a **gap report** — surfacing places where spec says X but code does Y.

> 🎯 *That answer — never possible in Confluence — is the case to your director.*

## Step 4 · Pick a real mini-project (2 min)

Open the lab chat. The facilitator will ask:

> *"What's one requirement from your real backlog you'd put through this in the next two weeks?"*

Drop one line in the chat. We'll capture all suggestions and propose a shortlist before you leave.

## Checkpoint ✅

- [ ] Your Issue is closed (and on the board in "Done").
- [ ] You ran the Copilot "spec ↔ code" prompt and saw an honest gap answer.
- [ ] You dropped one mini-project candidate in the lab chat.
- [ ] React 👍 in the lab chat.

---

## What you take home

- A **forked repo** with everything you built today, ready to share with your team.
- The **lab itself** as a take-home guide — run it again with anyone.
- Re-usable **prompts** in [.github/prompts/](../../.github/prompts/) — wired into Copilot via slash-commands.
- A **2-week trial plan** drafted by the room.

> 💡 **Take it home today.** Star this fork in your account so you can find it again. Show it to your manager this afternoon.
