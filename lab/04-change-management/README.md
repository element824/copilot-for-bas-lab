# Section 4 · Change management — commits & pull requests

⏱ **15 minutes** · 🎯 Save your change, open a "page review" (PR), and publish it.

## The translation guide

Forget the engineering words. Use these:

| GitHub term | What we'll call it today |
|---|---|
| Branch | **Draft copy** — a private workspace for your edits |
| Commit | **Save with a note** — a snapshot you can comment on later |
| Pull Request (PR) | **Page review** — your draft put forward for approval |
| Review comment | **Inline comment** — same as Confluence |
| Merge | **Publish** — your change is now the live version |

If anyone says "branch" or "merge", just nod and translate it in your head.

## Step 1 · Make a small edit on a draft copy (5 min)

1. In github.dev, open the user story you created in section 3.
2. Add one sentence to the Context — anything. e.g. *"This story addresses the gap raised in last week's BA review."*
3. Save (`Ctrl+S`).
4. Click the **Source Control** icon in the left sidebar (it looks like a Y / branch glyph).
5. You'll see your file under "Changes". Type a short note in the message box: `Add review-context note`.
6. Click the **✓ Commit & Push** button.

> 🪪 If asked "do you want to create a new branch?", say **yes** and accept the suggested name. That's your "draft copy".

## Step 2 · Open the page review (5 min)

After the commit, github.dev offers a button: **Create Pull Request**. Click it.

1. **Title:** something plain-English, e.g. `Add patient-history user story`.
2. **Description:** one or two sentences. *"Adds US-XXX. Context refined with Copilot."*
3. Click **Create**.
4. You'll see the PR page. Note the **Files changed** tab — click it, then look for the **Rich diff / Rendered** toggle. Switch to **Rendered**. The page now looks like Confluence track-changes.

## Step 3 · Publish (3 min)

1. Back on the **Conversation** tab of your PR.
2. Click **Merge pull request** → **Confirm merge**.
3. Click **Delete branch** when offered. (It just tidies up your draft copies.)
4. Your change is now on the main page. Visit your fork's repo home — see the file updated.

## Why this is better than Confluence "track changes"

- The PR is a **conversation** — comments live on individual lines forever, not in a sidebar that disappears on save.
- The PR can require **approvals** before publishing — a real governance gate, not a polite "please review" email.
- Every published change has a **reason and a reviewer** attached, not just a timestamp.

## Checkpoint ✅

- [ ] You opened, reviewed and merged a Pull Request in your fork.
- [ ] Your change is now visible on the main page of the file.
- [ ] React 👍 in the lab chat.

> ➡️ Next: [05 · End-to-end](../05-end-to-end/) — close the loop.
