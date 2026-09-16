# The session screen

Two panes. Chat on the left, your app on the right. Everything else hangs off those.

## The header[​](#the-header "Direct link to The header")

![The session screen](/ape-docs/assets/images/ape-03-workspace-header-6a0a066e268977a6f5c77297ae18a24a.png)

From left to right:

* **1. Session menu** – click to navigate back to the dashboard, duplicate current session, or create a template.
* **2. Project name** – click to rename the session. The name is what you'll see in the session switcher and the prototypes list.
* **3. Variation switcher** – create new variations (branches) and jump between them.
* **4. Status badge** – running, sleeping, provisioning, and so on. See [Sessions](/ape-docs/ape/concepts/sessions/.md).
* **5. Share** – copy a read-only link, or invite someone who can edit. Avatars beside it show who's looking right now. See [Sharing](/ape-docs/ape/working-with-others/sharing/.md).
* **6. Advanced** – click to learn more about how to open this session in Cursor or publish it as a prototype/website for others to preview\..

On a session that isn't yours, the header also shows whose it is.

## The left pane: chat[​](#the-left-pane-chat "Direct link to The left pane: chat")

Where you talk to the agent, and to people. Prompts, the agent's steps as it works, image attachments, and the queue if you send more than one thing at a time.

It's also where notes to teammates appear, and where the agent's questions show up as cards you answer. See [Prompting the agent](/ape-docs/ape/the-workspace/prompting-the-agent/.md).

You can collapse the pane entirely if you want the preview full width, useful when you're reviewing rather than building.

## The right pane: three tabs[​](#the-right-pane-three-tabs "Direct link to The right pane: three tabs")

![The session screen](/ape-docs/assets/images/ape-03-workspace-right-pane-3-tabs-73d356d2abac40672d31b4a862fba5d3.png)

**1. Preview** – the running application. See [The live preview](/ape-docs/ape/the-workspace/the-live-preview/.md).

**2. Files** – every file that changed in this session, with its diff. Covers changes from every source, not just the agent.

**3. Code** – a real editor with a file tree and tabs, for when it's faster to fix something yourself than to describe it.

Files and Code are both covered in [Files and history](/ape-docs/ape/the-workspace/files-and-history/.md).

## The floating toolbar[​](#the-floating-toolbar "Direct link to The floating toolbar")

![The session screen](/ape-docs/assets/images/ape-03-workspace-toolbar-2896f5959b2e066c143fa87ba10a80bf.png)

A small draggable bar over the preview with two mutually exclusive modes:

* **Inspect** – hover to identify elements, click to attach one to your next prompt.
* **Comment** – click an element to leave feedback anchored to it, with a screenshot.

Drag it out of the way if it's covering something. See [Pointing at things](/ape-docs/ape/the-workspace/pointing-at-things/.md) and [Comments and notes](/ape-docs/ape/working-with-others/comments-and-notes/.md).

## The Advanced menu[​](#the-advanced-menu "Direct link to The Advanced menu")

Three sections:

* **Connect via SSH** – a copyable `aiw connect` command for opening this session in Cursor. See [CLI and SSH onboarding](/ape-docs/ape/reference/cli-and-ssh-onboarding/.md).
* **Pull request** – create one, or see why the button is disabled. Templates have no upstream, so there's nothing to open a PR against. See [Pull requests](/ape-docs/ape/shipping/pull-requests/.md).
* **Publish** – put the prototype on a public URL. Templates only. See [Publishing](/ape-docs/ape/shipping/publishing/.md).

The project menu, next to the session name, is separate: go to the dashboard, duplicate the session, or mark it as a template.

## Link parameters[​](#link-parameters "Direct link to Link parameters")

Two are worth knowing because they change what the screen does:

* `?viewer=1` – read-only. What people get from a Share link.
* `?path=/some/route` – opens with the preview already on that route. The share link includes this automatically, so a link points at what you were looking at.

## Resizing[​](#resizing "Direct link to Resizing")

Drag the divider between the panes. The layout is remembered per session, so a session you use for reviewing can stay preview-heavy while another stays chat-heavy.

## Where to go next[​](#where-to-go-next "Direct link to Where to go next")

* **[Prompting the agent](/ape-docs/ape/the-workspace/prompting-the-agent/.md)** – what to say to get what you want.
* **[Pointing at things](/ape-docs/ape/the-workspace/pointing-at-things/.md)** – the fastest way to tell the agent which element you mean.
* **[The live preview](/ape-docs/ape/the-workspace/the-live-preview/.md)** – routes, device sizes, and what the splash screens mean.

***

**Questions, problems, or ideas?** Ask in [#bloom-ape](https://vinted.slack.com/archives/C0B4X98C2R1) on Slack.
