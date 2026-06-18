# Section 1 · Project spaces — repo, project board, first issue

⏱ **15 minutes** · 🎯 Create a Project board and your first Issue in your fork.

## Why this matters

In Confluence, a "space" is your home for one workstream. In GitHub, a **repo + Project + Issues** is the same idea — with the bonus that the spec, the board and the code all share one address.

By the end of this section, your fork will have:

- ✅ A **Project board** (Backlog · In progress · Done)
- ✅ A **first Issue** representing a real requirement
- ✅ The Issue placed on the board in "In progress"

## Step 1 · Create the Project board (5 min)

1. On your fork's GitHub page (in the browser, not github.dev), click **Projects** in the top tabs.
2. Click **New project** → choose the **Board** template → name it `BA Spec Trial`.
3. Confirm you have three columns: **Backlog**, **In progress**, **Done**. If not, add them.

> 🪟 Keep github.com and github.dev open in two browser tabs. You'll switch between them.

## Step 2 · Create the first Issue (5 min)

1. Back on your fork, click the **Issues** tab → **New issue**.
2. **Title:** `Migrate "Patient identity verification" requirement to spec`
3. **Description:** paste the sample requirement below (or paraphrase one of your own).

```
The system must verify a patient's identity before allowing a clinician to record
a new consent. Verification can be by Medicare number plus date of birth, or by
hospital MRN. If both fail, the clinician can override with a witness statement,
which must be captured in the audit trail.
```

4. Click **Submit new issue**. Note the issue number (e.g. `#1`).

## Step 3 · Add it to the board (3 min)

1. Open your Project board in the other tab.
2. Click **+ Add item** in the **In progress** column.
3. Paste `#1` (or whatever number) → press Enter. The Issue card appears.

## Step 4 · Quick tour of what just happened (2 min)

You now have a Confluence-equivalent space:

| What | Confluence equivalent | Where it lives |
|---|---|---|
| Repo | A space | github.com/&lt;you&gt;/copilot-for-bas-lab |
| Project board | A "Roadmap" or "Tasks" macro | Projects tab |
| Issue | A page with a status | Issues tab |
| Spec files (next section) | Pages | `spec/` folder |

## Checkpoint ✅

- [ ] Your Project board exists and is named `BA Spec Trial`.
- [ ] Your first Issue is created and visible on the board in "In progress".
- [ ] React 👍 in the lab chat.

> ➡️ Next: [02 · Structured specs](../02-structured-specs/)
