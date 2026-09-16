# Getting help

APE is early. Things will be unclear, and some things will be broken. Both are worth telling us about.

## Slack[​](#slack "Direct link to Slack")

**[#bloom-ape](https://vinted.slack.com/archives/C0B4X98C2R1)** is the place for anything to do with APE – questions, problems, requests, or thinking out loud about whether it's the right tool for what you're doing.

There's no wrong question there. If something in these docs didn't make sense, that's useful to hear too.

## The in-app feedback button[​](#the-in-app-feedback-button "Direct link to The in-app feedback button")

There's a **Feedback** pill in the bottom-right corner of APE. It takes three kinds of thing:

* **Bug** – something is broken or behaving unexpectedly.
* **Idea** – something you'd like APE to do.
* **Other** – anything else.

It records which page you were on, so you don't have to explain where you were. Use it when you want to note something without starting a conversation.

**Rough rule:** Slack if you need an answer, the feedback button if you're reporting something and don't need a reply.

## Before you report a problem[​](#before-you-report-a-problem "Direct link to Before you report a problem")

[Troubleshooting](/ape-docs/ape/reference/troubleshooting/.md) covers the failures people hit most: the wrong VPN, `aiw` not being installed, sessions asleep, previews not loading, builds failing. If your problem is on that list, the fix is usually faster than waiting for a reply.

For setup problems specifically, run:

```
aiw doctor
```

It checks each part of your setup and names the one that's wrong. Pasting its output into Slack is often the whole bug report.

## What to include[​](#what-to-include "Direct link to What to include")

The more of this you can give, the faster it gets sorted:

* **A link to the session.** Copy the URL from your browser. This is the single most useful thing – it identifies the session, the project, and the state it's in.
* **What you expected, and what happened instead.**
* **What you'd done just before.** The prompt you sent, the button you clicked.
* **A screenshot**, if it's visual.

If the session won't load at all, say which project it was on and roughly when you created it.
