# Facilitator run-sheet — 90 min hands-on lab

> Audience: BAs (single customer). Mode: virtual facilitator + hopefully one in-person helper. Format: hands-on, follow-along, every attendee on their own laptop.

## Two days before

- [ ] Send PRE-FLIGHT.md to all attendees with a clear deadline: *"Run this by 5pm Thursday or message me."*
- [ ] Confirm at least **one in-person helper** is available — without one, a single stuck laptop derails the lab. The helper walks the room and unblocks people while you present.
- [ ] Verify your Copilot is active and the lab repo URL is accessible from the customer's network.
- [ ] Pre-create a **lab Teams chat** for the day. Add all attendees. This is the "stuck?" channel.

## Morning of

- [ ] Light theme on. Activity bar hidden. Terminal closed. Zoom 1.3×.
- [ ] Open: README.md preview · the lab repo on github.com · this run-sheet on a second screen.
- [ ] Verify Foam graph view loads.
- [ ] Mic check, camera check, screen-share check.
- [ ] Post in the lab chat: *"We start at 11. React 👍 if your pre-flight is green."*

## Hard rules during the lab

- ❌ Never open the terminal.
- ❌ Never say "branch", "commit", "merge", "rebase". Use *draft / save / publish*.
- ❌ Never show a unified diff. Use the side-by-side compare view.
- ✅ Use the Markdown **preview**, not the source, whenever you're explaining content.
- ✅ Pause for the 👍 checkpoint at the end of every section. Don't move on until you see most of the room react.
- ✅ When someone gets stuck, tag the in-person helper, not the whole room. Keep the main channel for content.

---

# 90-minute arc

## 0. Overview & framing — 10 min

**Goal:** lower cognitive resistance, set the contract, get everyone forked.

### 0.1 Pitch (2 min) — see [PITCH.md](./PITCH.md)
- Opening line: *"Today is about your day-to-day, not a tech demo."*
- Three messages: wiki not IDE · specs share a home with code · Copilot is **your** co-author.

### 0.2 Show the wiki illusion (3 min)
- Share screen on the lab repo's `README.md` in **preview**.
- *"This is your space home. If this looks like Confluence, that's the point."*
- Walk down the table. *"Every link is a Markdown page."*
- Open the Foam graph view (`Ctrl+Shift+P` → "Foam: Show Graph"). *"This is your Confluence space map — but it stays accurate forever."*

### 0.3 Everyone forks the repo (5 min)
- Talk them through the **Fork** button on github.com. Choose their own account.
- They land on their fork. They click `.` to open it in github.dev — or click "Code → Open with Codespaces" if they prefer.
- **Checkpoint 👍:** *"React when you can see your forked repo open in your browser."*

> If anyone is stuck here, the helper goes to them. Don't proceed until 90% of tiles have reacted.

---

## 1. Project spaces — 15 min

**Goal:** prove that "the GitHub project space" is just a tidy folder + a board + a list of tickets.

### 1.1 Tour what you got with the fork (3 min)
- Walk through the folder tree: `README.md`, `lab/`, `spec/`, `src/`. Speak as if narrating a Confluence space.
- Open `lab/01-project-spaces/README.md` in preview. *"This is your follow-along instructions for the next 12 minutes."*

### 1.2 Create a Project board (5 min)
- On their fork's GitHub page, click **Projects → New project → Board**.
- Add three columns if not pre-set: Backlog · In progress · Done.
- *"This is the same board view you'd see in Jira or ADO. The difference is — it lives next to the spec."*

### 1.3 Create the first Issue (5 min)
- On the fork: **Issues → New issue**.
- Title: `Migrate "Patient identity verification" requirement to spec`.
- In the body, paste a sample one-paragraph requirement (provided in the lab folder).
- Save. Drag it onto the Project board → "In progress".

### 1.4 Checkpoint 👍 (2 min)
- *"React when you can see your Issue on your Project board."*
- Spot-check 2 attendees by name; ask them to share-screen briefly.

---

## 2. Structured specs (markdown spec kit) — 15 min

**Goal:** show that a "spec kit" is just a folder of templates, and that filling them in feels like Confluence.

### 2.1 Walk the kit (3 min)
- Open `spec/_templates/` in preview. Open each template: `user-story.md`, `decision.md`, `persona.md`. *"This is your blank page library."*
- Open `spec/01-overview.md` and `spec/02-personas.md` for reference — *"This is what good looks like."*

### 2.2 Activity: write your own Overview (10 min)
- Each attendee opens `spec/01-overview.md` in **edit mode** in github.dev.
- They replace the example with the requirement from their Issue (the one they pasted in 1.3).
- *No Copilot yet — pure typing. We want them to feel that "edit a Markdown file" is just typing.*

### 2.3 Checkpoint 👍 (2 min)
- *"React when your Overview has at least 3 sections filled in."*

---

## 3. Refine requirements with Copilot — 20 min ⭐ THE WOW

**Goal:** the moment the BAs decide whether they like this. Don't rush it.

### 3.1 Demo: prose → Gherkin (5 min)
- Share-screen on YOUR fork. Open `spec/03-user-stories/US-002-withdraw-consent.md`.
- Highlight the Context paragraph.
- Copilot Chat: *"Rewrite this as Gherkin acceptance criteria following the style used in US-001."*
- Watch it produce the scenarios. Paste into the file. **Pause.** Let them react.

### 3.2 Demo: Copilot fills the template (3 min)
- Copilot Chat: *"Create a new user story for: clinician views a patient's consent history, using the template."*
- Show how Copilot reads `spec/_templates/user-story.md` + the personas file + existing-style and produces a draft.

### 3.3 Activity: their turn (10 min)
- Each attendee creates a new user story in their fork, on a topic of their choice (or from a list provided in the lab folder).
- They use Copilot Chat: *"Generate a user story for X using the template."*
- Then they highlight the resulting Context and ask: *"Rewrite as Gherkin."*
- The helper walks the room and unblocks people; you stay on the call to answer questions in chat.

### 3.4 Checkpoint 👍 (2 min)
- *"React when you have at least one Copilot-generated story saved in your fork."*
- Ask two volunteers to share-screen and show theirs. **This is the most important social proof of the day.**

---

## 4. Change management — commits & PRs — 15 min

**Goal:** rename git into "draft / save / publish". Show that a PR is just a Confluence-style page review.

### 4.1 Frame the metaphor (2 min)

Show the cheat-sheet on screen:

| GitHub term | What we'll call it today |
|---|---|
| Branch | Draft copy |
| Commit | Save with a note |
| Pull Request | Page review |
| Review comment | Inline comment |
| Merge | Publish |

### 4.2 Demo: edit on a draft copy → review → publish (5 min)
- On your fork, edit a story in github.dev → *"Commit & push"* → it offers to create a Pull Request.
- Use plain English in the PR title. Self-approve and merge. *"Now it's published."*

### 4.3 Activity: their turn (6 min)
- Each attendee makes a small edit (one sentence) in their fork → *Commit & push* → opens a PR → merges.
- Helper unblocks anyone seeing scary-looking diff views. Steer them to the **Rich diff** tab if available.

### 4.4 Checkpoint 👍 (2 min)
- *"React when you've published a change through a PR."*

---

## 5. End-to-end: requirement → spec → artefact — 10 min

**Goal:** the closing wow. Tie Issue ↔ Spec ↔ PR.

### 5.1 Link the loop (5 min)
- On your fork, edit your PR description to add: `Closes #1` (where 1 is the Issue from section 1).
- Merge. The Issue auto-closes. The Project board card moves to "Done".
- *"This trace — requirement → spec → published change → board status — is the structural shift Confluence cannot give you."*

### 5.2 Spec ↔ code, the director moment (3 min)
- Copilot Chat: *"Does the code in /src implement the requirement in spec/03-user-stories/US-001?"*
- Copilot answers honestly (no code yet).
- *"When real code lands here, you'll get a real answer. That's the day Confluence-vs-ADO drift dies."*

### 5.3 Picking the trial mini-project (2 min)
- Open the floor: *"What's one requirement you'd put through this in the next two weeks?"*
- Capture answers in the lab chat.

---

## Q&A and close — 5 min

- Recap the three messages from the pitch.
- Confirm: licences sorted, helper assigned for the trial, follow-up session in 2 weeks.
- *"Stop me whenever it stops looking like Confluence — the whole point is to keep it light."*

---

## If something breaks — facilitator playbook

| Symptom | Mitigation |
|---|---|
| Copilot is rate-limited / slow | Skip the activity timer; let people watch your screen until it recovers. |
| The fork failed for many | Have them open the lab repo in github.dev directly — they can still follow Sections 0–4 read-only. |
| Audio dies | Type the next instruction into the lab chat in real time. The lab repo is self-explanatory enough to keep moving. |
| One attendee dominating chat | Acknowledge once, ask them to take it offline with the helper. |
| Running over time | Cut Section 5.2 (spec ↔ code). It's the only optional piece.

---

## Post-lab

- [ ] Drop the README, PRE-FLIGHT, and the recording link in the lab chat.
- [ ] Email a 5-bullet recap with the trial mini-project shortlist.
- [ ] Schedule the 2-week follow-up.
