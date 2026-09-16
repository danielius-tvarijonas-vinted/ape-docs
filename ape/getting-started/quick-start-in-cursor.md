# Quick start in Cursor

Your session runs on a server, not in your browser. The web interface is one window onto it. Cursor is another.

One command opens the same session in Cursor, working on the same files, against the same running app. Nothing is copied or downloaded – you're editing the container directly, and changes flow both ways.

You don't have to choose. The web session and Cursor can be open at the same time, and each sees what the other does.

## Why you might want this[​](#why-you-might-want-this "Direct link to Why you might want this")

The web interface gives you the agent, the preview, comments, and sharing. Cursor gives you everything else you already use:

* **Your own MCP servers** – Vinted's, like V-Assist, or anything else you've connected.
* **Cursor extensions** – whatever's in your setup.
* **AI skills and rules** – your own prompts, workflows, and conventions.
* **A real editor and a terminal**, for the things the in-app Code tab deliberately doesn't do: creating and renaming files, find-and-replace, running commands.

APE's own project rules come along too, so the agent in Cursor works under the same constraints as the agent in the web app.

## Before you start[​](#before-you-start "Direct link to Before you start")

* You've been through [Getting access](/ape-docs/ape/getting-started/getting-access/.md) – VPN on, `aiw` installed and enrolled.
* **Cursor is installed.** If it isn't, install it and re-run `aiw enroll --sso` so APE can find it.

## 1. Create the session in APE[​](#1-create-the-session-in-ape "Direct link to 1. Create the session in APE")

Open APE in your browser and create a session as normal – from **Templates**, **Projects**, or **Explore**. Wait for it to reach **running**.

The session has to exist before you can connect to it. This is the part Cursor can't do for you.

## 2. Copy the connect command[​](#2-copy-the-connect-command "Direct link to 2. Copy the connect command")

![Quick start in Cursor](/ape-docs/assets/images/ape-01-get-started-quick-start-08-310826cea81997bfed61105393220d4b.png)

In the session header, open the **Advanced** menu in the top right.

Under **Connect via SSH** there's a command that looks like this:

```
aiw connect 9db46916 --open
```

The `9db46916` part is your session's ID, so it's different every time. Click **Copy**.

## 3. Paste it into Terminal[​](#3-paste-it-into-terminal "Direct link to 3. Paste it into Terminal")

Open Terminal, paste, and press Enter.

The first time on a new session it takes a few seconds – it's setting up the connection and putting a key in place. Then Cursor opens on the session's files.

That's it. You're in.

## 4. Preview the prototype inside Cursor[​](#4-preview-the-prototype-inside-cursor "Direct link to 4. Preview the prototype inside Cursor")

You don't need to keep flipping to your browser to see what you've changed. Cursor can show the running prototype in a tab next to your code.

1. In Cursor, click the **ellipsis (…)** in the top-right corner.
2. Choose **Open Browser**.
3. Go back to APE in your web browser and copy the session URL from the address bar.
4. Paste it into the Cursor browser's address bar and press Enter.

The prototype loads in Cursor. Edit on one side, watch it update on the other, without leaving the window.

Worth doing once and leaving open – the tab stays where it is, so it's there the next time you come back to the session.

## Working there[​](#working-there "Direct link to Working there")

**Files sync both ways.** Edit in Cursor and the preview updates and the change appears in the web session's Files tab. Prompt the agent in the web app and the files change under you in Cursor.

**Your work is still saved the same way.** Autosave commits what you do in Cursor, same as everything else, so it shows up in the session history and can be reverted. See [How your work is saved](/ape-docs/ape/concepts/how-your-work-is-saved/.md).

**The session won't sleep while you're connected.** An open SSH connection counts as activity, so it won't wind down mid-task.

**Reconnecting is the same command.** If the container restarts or you come back tomorrow, run it again – it's safe to repeat and fixes itself if anything drifted.

## Skipping the browser entirely[​](#skipping-the-browser-entirely "Direct link to Skipping the browser entirely")

Once you're comfortable, you don't need the web app to start a session at all:

```
aiw create
```

That creates one and opens it in Cursor in a single step. `aiw list` shows your sessions if you need an ID.

## If it doesn't work[​](#if-it-doesnt-work "Direct link to If it doesn't work")

The most common causes are the wrong VPN, Cursor not being installed when you enrolled, or a stale entry left behind by a deleted session.

```
aiw doctor
```

That checks each part of the setup and tells you which one is wrong. For the SSH details underneath all of this – the jump host, key handling, and a fuller troubleshooting table – see [CLI and SSH onboarding](/ape-docs/ape/reference/cli-and-ssh-onboarding/.md).

## Where to go next[​](#where-to-go-next "Direct link to Where to go next")

* **[Quick start](/ape-docs/ape/getting-started/quick-start/.md)** – the web walkthrough, if you haven't done it.
* **[CLI and SSH onboarding](/ape-docs/ape/reference/cli-and-ssh-onboarding/.md)** – how the connection works, and every `aiw` flag.
* **[Files and history](/ape-docs/ape/the-workspace/files-and-history/.md)** – how edits made in Cursor show up back in the web session.

***

**Questions, problems, or ideas?** Ask in [#bloom-ape](https://vinted.slack.com/archives/C0B4X98C2R1) on Slack.
