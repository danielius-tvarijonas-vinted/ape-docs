# Quick start

This is a test run. The point isn't to build anything you'll keep – it's to go once round the loop APE is built on, so the rest of the docs make sense: start a session, ask for a change, point at what's wrong, and share the result.

We'll use the blank template rather than a real Vinted repo. It starts in seconds, there's nothing to break, and you can throw the session away afterwards.

This assumes you've been through [Getting access](/ape-docs/ape/getting-started/getting-access/.md). If you haven't, do that first – it takes about a minute.

## 1. Start a session[​](#1-start-a-session "Direct link to 1. Start a session")

![Quick start](/ape-docs/assets/images/ape-01-get-started-quick-start-01-61587971380833c641a20f387d03d1e9.png)

On the [home screen](https://app.bloom-ai-poc.svc.vinted.com), click **Explore**. That creates a session on the blank template and opens it.

## 2. Wait for it to boot[​](#2-wait-for-it-to-boot "Direct link to 2. Wait for it to boot")

![Quick start](/ape-docs/assets/images/ape-01-get-started-quick-start-02-bffb67b62d4c8a2e2e54a6f119a68b01.png)

The right pane shows a splash while the session comes up, moving through **provisioning** → **installing** → **running**. The line under the spinner tells you what's happening.

Templates use a pre-built image, so this takes about five to ten seconds. A real repo like `marketplace-web` takes a couple of minutes the first time.

When the preview appears, the app is running.

## 3. Ask for something[​](#3-ask-for-something "Direct link to 3. Ask for something")

![Quick start](/ape-docs/assets/images/ape-01-get-started-quick-start-03-99d3b0da1a85c6d5a6fe3c44b996b69d.png)

Type into the chat on the left and press Enter.

Be specific about what you want and where it goes:

> Create a pricing page with three tiers – Free, Plus, and Pro. Use cards in a row, with the middle one highlighted.

Rather than:

> make a pricing page

You'll see the agent's steps appear as it works – reading files, writing them, running checks. When it finishes, the preview refreshes and the change is already committed.

## 4. Point at what's wrong[​](#4-point-at-whats-wrong "Direct link to 4. Point at what's wrong")

![Quick start](/ape-docs/assets/images/ape-01-get-started-quick-start-04-7b12f753ee91aab4a6ef6c117546732e.png)

This is the part worth learning early.

Find the floating toolbar over the preview and turn on **Inspect**. Hover the preview – each element highlights and shows what it is and which file it comes from. Click the middle pricing card.

Now type:

> make this one taller and add more space around the price

The agent knows which element you mean, because you told it by clicking rather than describing. It goes straight to the right file.

[Pointing at things](/ape-docs/ape/the-workspace/pointing-at-things/.md) covers the rest.

## 5. Check it on mobile[​](#5-check-it-on-mobile "Direct link to 5. Check it on mobile")

![Quick start](/ape-docs/assets/images/ape-01-get-started-quick-start-05-44b269e583c1db844d8112af9bdd325d.png)

In the preview's URL bar there's a device switcher – desktop, tablet, mobile. Switch to mobile.

This genuinely re-renders the app at 390 × 844 rather than scaling a picture, so what you see is what the app does at that width. If it breaks, say so in chat.

## 6. Go back if you need to[​](#6-go-back-if-you-need-to "Direct link to 6. Go back if you need to")

![Quick start](/ape-docs/assets/images/ape-01-get-started-quick-start-06-e89e91c433189974cf9e7b600948c798.png)

Every prompt you sent is a commit. On any change card in the chat, click **Details** to open the history view, then **Preview** to see the app as it was at that point, or revert to it.

Nothing you do is one-way. See [How your work is saved](/ape-docs/ape/concepts/how-your-work-is-saved/.md).

## 7. Share it[​](#7-share-it "Direct link to 7. Share it")

![Quick start](/ape-docs/assets/images/ape-01-get-started-quick-start-07-70d984e71937408384ffed2b03dce858.png)

Click **Share** in the header to copy a link. Anyone on `backup-vinted-vpn` who opens it gets a read-only view – they can click through the prototype and leave comments pinned to specific elements, but they can't change anything.

To let someone drive the agent too, invite them as a collaborator from the same dialog.

## There's a second way in[​](#theres-a-second-way-in "Direct link to There's a second way in")

![Quick start](/ape-docs/assets/images/ape-01-get-started-quick-start-08-310826cea81997bfed61105393220d4b.png)

Everything above happens in the browser, and for a lot of work that's all you need. But your session isn't a web page – it's a live environment running on a server, and you can connect to it from **Cursor** instead. Same session, same files, same running app, with your preferred MCP servers, extensions, and AI skills available alongside.

It takes one command, copied from the **Advanced** menu in the session header. See **[Quick start in Cursor](/ape-docs/ape/getting-started/quick-start-in-cursor/.md)**.

You don't have to pick one. Both can be open at once, and each sees what the other does.

## Where to go next[​](#where-to-go-next "Direct link to Where to go next")

* Opening the same session in your own editor → [Quick start in Cursor](/ape-docs/ape/getting-started/quick-start-in-cursor/.md)
* Prototyping on a real Vinted repo instead of a template → [Templates and projects](/ape-docs/ape/concepts/templates-and-projects/.md)
* Getting better results out of the agent → [Prompting](/ape-docs/ape/the-workspace/prompting-the-agent/.md)
* Putting it on a URL you can send to anyone → [Publishing](/ape-docs/ape/shipping/publishing/.md)
* Turning it into a pull request → [Pull requests](/ape-docs/ape/shipping/pull-requests/.md)

***

**Questions, problems, or ideas?** Ask in [#bloom-ape](https://vinted.slack.com/archives/C0B4X98C2R1) on Slack.
