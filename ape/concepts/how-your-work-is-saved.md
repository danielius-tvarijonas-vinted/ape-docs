# How your work is saved

Two questions come up before anyone will let an AI agent near a real codebase: *where does my work go if something breaks?* and *can this thing damage our repo?*

Short answers: everything is committed as it happens, and no, it works on a branch.

## Every change the agent makes is a commit[​](#every-change-the-agent-makes-is-a-commit "Direct link to Every change the agent makes is a commit")

The agent is instructed to commit after every change, before it reports back to you. Not at the end of a session, not when you remember to ask – after each coherent unit of work.

This is a hard rule in the agent's instructions rather than a habit it might drift out of, because your whole history depends on it.

Each save gets a short description of what changed, so the list reads like a record of the work rather than a wall of timestamps:

```
Add a "Save for later" button to the item page

Make the pricing cards equal height on mobile

Move the filters into a collapsible panel
```

## Autosave catches everything else[​](#autosave-catches-everything-else "Direct link to Autosave catches everything else")

Not every change comes from the agent. You might edit a file in the Code tab, or SSH in, or work in Cursor. Those get committed too, by a process watching the workspace:

* **30 seconds after you stop changing things**, it commits.
* **Every 5 minutes**, if you're still going, it commits anyway.

Commit messages are written by a small model reading the diff, so the history stays readable rather than filling up with timestamps.

## So every prompt is a restore point[​](#so-every-prompt-is-a-restore-point "Direct link to So every prompt is a restore point")

![How your work is saved](/ape-docs/assets/images/ape-02-concepts-how-work-is-saved-1c92bf42fa44f4cece1847b591bbbaca.png)

Because each change is its own commit, you can move through your session's history the way you'd move through file versions.

Open **History** in the chat panel and you get every commit, grouped by day. From any entry you can **preview** that version – the right pane checks out that point in time and shows you the app as it was – or **revert** to it.

Reverting is itself a commit. If you revert too far, revert the revert.

See [Files and history](/ape-docs/ape/the-workspace/files-and-history/.md) for how to use it.

## Your session is a branch. It is never master.[​](#your-session-is-a-branch-it-is-never-master "Direct link to Your session is a branch. It is never master.")

When you create a session on a real repo, APE branches off that repo's default branch. The branch is named after your session:

```
prototype/session-a1b2c3d4e5
```

Everything – the agent's commits, your edits, autosave – lands there. Nothing is pushed to `master`, and the agent has no path to it.

The **only** way work gets from a session into the real codebase is a pull request that you open deliberately and that a person reviews. It's a normal PR, in the normal place, with the normal checks. It carries an `AI Workspace prototype` label so it's easy to spot in a review queue, and that's the only thing unusual about it.

If nobody opens a PR, the branch simply sits there. Deleting the session deletes the branch.

## What the agent is told not to touch[​](#what-the-agent-is-told-not-to-touch "Direct link to What the agent is told not to touch")

Every project carries its own rules file that constrains the agent on top of the global ones. It's how a team keeps a prototyping tool from wandering into their build config.

`marketplace-web` is a good worked example. Its rules tell the agent:

* Edit the **existing** stylesheet. Never create a new `.scss` file for a component that already has one.
* Make the **smallest possible change** – add or override the specific property asked for, nothing else.
* **Don't change logic, data fetching, or business rules.** Visual and layout changes only.
* **Don't run `pnpm install`.** Don't add packages.
* **Don't modify** `package.json`, `tsconfig.json`, `next.config.*`, or any `.env` file.
* Use conventional commits: `feat:`, `fix:`, `style:`.

Other projects set their own. If your team is onboarding a repo and wants tighter limits, that's the file to write.

## What this means in practice[​](#what-this-means-in-practice "Direct link to What this means in practice")

| If this happens                            | You lose                                                          |
| ------------------------------------------ | ----------------------------------------------------------------- |
| The agent makes a change you hate          | Nothing. Revert to the previous prompt.                           |
| You break something editing files yourself | Nothing. Autosave committed the last good state.                  |
| Your session goes to sleep                 | Nothing. The branch is untouched; the container rebuilds from it. |
| You close the tab mid-run                  | Nothing. The run continues; reopening reattaches to it.           |
| You delete the session                     | The branch, and everything on it. This one is real.               |

The thing you can actually lose is unsaved edits in the Code tab – closing a tab there doesn't warn you. Hit ⌘S, or wait for autosave.

## Where to go next[​](#where-to-go-next "Direct link to Where to go next")

* **[Files and history](/ape-docs/ape/the-workspace/files-and-history/.md)** – how to actually use the history: see what changed, preview an older version, revert.
* **[Pull requests](/ape-docs/ape/shipping/pull-requests/.md)** – the one route from a session into the real codebase.
* **[Sessions](/ape-docs/ape/concepts/sessions/.md)** – what a session is, and what sleep does to it.

***

**Questions, problems, or ideas?** Ask in [#bloom-ape](https://vinted.slack.com/archives/C0B4X98C2R1) on Slack.
