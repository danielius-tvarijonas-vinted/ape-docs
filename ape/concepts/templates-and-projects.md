# Templates and projects

There are two kinds of starting point, and the difference decides what you can do at the end.

|                                 | [Templates](https://app.bloom-ai-poc.svc.vinted.com/templates) | [Projects](https://app.bloom-ai-poc.svc.vinted.com/projects) |
| ------------------------------- | -------------------------------------------------------------- | ------------------------------------------------------------ |
| **Based on**                    | A self-contained scaffold                                      | A real Vinted repo                                           |
| **Starts in**                   | Seconds                                                        | Up to a couple of minutes                                    |
| **Can open a pull request**     | No                                                             | Yes                                                          |
| **Can publish to a public URL** | Yes                                                            | No                                                           |
| **Good for**                    | Concepts, explorations, things you'll show                     | Changes you intend to ship                                   |

## Templates[​](#templates "Direct link to Templates")

![Templates and projects](/ape-docs/assets/images/ape-02-concepts-templates-4be520c870f88e309aa55f1381bef543.png)

[Templates](https://app.bloom-ai-poc.svc.vinted.com/templates) have no upstream repository. Nothing you do in one can affect a real codebase, which makes them the right place to try something new.

| Template                   | What it's for                                                                                                             |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `blank-template`           | Minimal starter for prototyping fresh UI ideas from scratch — just the toolchain and a single landing route.              |
| `vinted-app`               | Mobile-first Vinted consumer app — browse, sell flow, inbox, and auth screens.                                            |
| `agentic-vinted-app`       | Agentic Vinted consumer app — richer component showcase plus Supabase auth/DB scaffolding for end-to-end demos.           |
| `marketplace-web-template` | A marketplace scaffold with the fullest route set – items, orders, settings, playground.                                  |
| `bloom-design-system`      | Blank canvas for building Vinted web experiences with the Bloom design system.                                            |
| `bloom-internal-tools`     | Internal tool template with top-nav, side-nav, and multi-panel layout patterns.                                           |
| `vinted-go-bloom`          | Blank canvas for Vinted Go web experiences with the Bloom design system.                                                  |
| `vinted-go-mobile`         | Touch-friendly Vinted Go mobile UI with Bloom components and patterns.                                                    |
| `vintedgo-internal-tools`  | Vinted Go back-office tooling — top-nav, side-nav, and multi-panel layout patterns for carrier/shipping admin interfaces. |
| `web-admin`                | Admin panel template with data-dense layouts and Bloom design system.                                                     |

Because a template has no upstream, its output is a link rather than a pull request. See [Publishing](/ape-docs/ape/shipping/publishing/.md).

## Projects[​](#projects "Direct link to Projects")

![Templates and projects](/ape-docs/assets/images/ape-02-concepts-projects-c37b6c8515910f6940f749f4d4e92141.png)

[Projects](https://app.bloom-ai-poc.svc.vinted.com/projects) are real Vinted repositories. Your session branches off the repo's actual default branch, and the changes you make can become a pull request.

| Project                        | Worth knowing                                                                                                                                                 |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `marketplace-web`              | Marketplace Web. The largest. Slowest to provision. Styled with SCSS, not Tailwind – the agent knows this, but it's worth knowing too when you write prompts. |
| `vintedgo-ui`                  | Vinted Go website.                                                                                                                                            |
| `recommerce-ui`                | Points at the recommerce sandbox API.                                                                                                                         |
| `svc-shipping-frontend`        | Beta. Needs a separate Okta sign-in **inside** the preview.                                                                                                   |
| `svc-vcarrier-admin-frontend`  | Beta. Needs a separate Okta sign-in **inside** the preview.                                                                                                   |
| `bloom-web-ui-mobile-template` | Beta. It's a real repo that can also be published.                                                                                                            |

**You need a GitHub token to use any of these.** APE clones the repo as you, so session creation fails without one – see [Getting access](/ape-docs/ape/getting-started/getting-access/.md). Templates don't need it.

**Beta** means the prototype experience is still being refined.

The two that require an in-preview sign-in will show a sign-in overlay on the preview when you first open a protected route. That's the app's own Okta, not APE's – sign in there and carry on.

### Choosing a base branch[​](#choosing-a-base-branch "Direct link to Choosing a base branch")

When you create a session on a project, you can pick which branch it starts from. The default branch is at the top and is what you want most of the time. Branch off something else when you're building on work that hasn't merged yet.

## Personal templates[​](#personal-templates "Direct link to Personal templates")

![Templates and projects](/ape-docs/assets/images/ape-02-concepts-personal-templates-50b2bc754e54c97a9a4af807bd2a524e.png)

Any session can become a template. Open the project menu in the header and choose to use it as a template – it then shows up under **Templates** for your teammates, alongside the official ones.

This is the design system workflow. Someone maintains a well-built starting point, other people spin variations off it, and improvements travel in both directions:

* **Merge to template** – you built something in a variation that belongs in the template. This previews the change first and tells you whether it applies cleanly.
* **Sync from template** – the template has moved on and you want those updates in your variation.

Both live in the session's family switcher rather than the Advanced menu.

If a merge conflicts, you'll be told which files. In some cases APE can resolve it by having the agent finish the merge in the template session.

## Where to go next[​](#where-to-go-next "Direct link to Where to go next")

* **[The session screen](/ape-docs/ape/the-workspace/the-session-screen/.md)** – what you get once you've picked something and created a session.
* **[Publishing](/ape-docs/ape/shipping/publishing/.md)** – how a template becomes a link you can send to anyone.
* **[Pull requests](/ape-docs/ape/shipping/pull-requests/.md)** – how work on a real repo gets reviewed and shipped.

***

**Questions, problems, or ideas?** Ask in [#bloom-ape](https://vinted.slack.com/archives/C0B4X98C2R1) on Slack.
