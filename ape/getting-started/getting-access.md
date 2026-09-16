# Getting access

Setup is a one-time process. It takes a few clicks in your browser and a few commands in a terminal app. No prior terminal experience is needed, just follow the steps below.

## Before you start[​](#before-you-start "Direct link to Before you start")

### 1. Connect to the right VPN when working remotely[​](#1-connect-to-the-right-vpn-when-working-remotely "Direct link to 1. Connect to the right VPN when working remotely")

**Connect to `backup-vinted-vpn`. Vinted has two VPNs and APE only works on this one.** **If you're on the other, APE's web app won't load at all.**

### 2. Open Terminal[​](#2-open-terminal "Direct link to 2. Open Terminal")

Terminal is the app where you'll type and run needed commands. On a Mac, open the Terminal app, on Windows open PowerShell.

Each command below can be copied and pasted in. Paste it, press Enter, and wait for it to finish before moving on. Some take a minute and print a lot of text along the way – that's normal.

### 3. Check you have Node[​](#3-check-you-have-node "Direct link to 3. Check you have Node")

Node is the software the APE command-line tool runs on. Copy the below command, paste into the Terminal app, and press Enter:

```
node -v
```

**If you see a version number** like `v22.14.0`, you're set. Move on to step 1 below.

**If you see `command not found`**, or a version lower than `v20`, install it:

1. Go to [nodejs.org/en/download](https://nodejs.org/en/download).
2. Download the version marked **LTS** – that's the stable one.
3. Open the downloaded file and click through the installer, accepting the defaults.
4. **Quit Terminal and open it again** – it won't notice the new install otherwise.
5. Run `node -v` once more. You should now see a version number.

***

## APE setup[​](#ape-setup "Direct link to APE setup")

### Step 1: Sign in[​](#step-1-sign-in "Direct link to Step 1: Sign in")

![Getting access](/ape-docs/assets/images/ape-01-get-started-get-access-sign-in-e47ca25c500c7a680ef6b919a0f15374.png)

Open [APE's web app](https://app.bloom-ai-poc.svc.vinted.com) and click **Sign in with Okta SSO**. Your account is created on first sign-in; there's nothing to request.

You'll land on the **Onboarding** page, which is where the next two steps happen.

### Step 2: Install APE's command-line tool[​](#step-2-install-apes-command-line-tool "Direct link to Step 2: Install APE's command-line tool")

`aiw` is APE's command-line tool. You need it once, to give your machine a key that identifies you to the workspace.

Back in Terminal, paste this and press Enter. It takes a minute or so and prints a lot of text.

```
sudo npm i -g @bloom-ai-workspace/cli --registry=https://nexus.vinted.net/repository/npm-proxy-web
```

Because of the `sudo`, it will ask for your computer's password. **Nothing appears as you type it** – no dots, no cursor movement. That's normal. Type it and press Enter.

### Step 3: Enroll[​](#step-3-enroll "Direct link to Step 3: Enroll")

![Getting access](/ape-docs/assets/images/ape-01-get-started-get-access-step-3-enroll-d88b4b07e04e9debd3182cb9f2fc8f19.png)

In Terminal, paste this and press Enter.

```
aiw enroll --sso
```

It does three things:

1. **Signs you in.** A browser tab opens showing a short code – check it matches the one in your terminal, then click **Confirm**.
2. **Creates a key for your machine.** If you don't already have one, it runs `ssh-keygen` and asks for an optional passphrase. Pressing Enter twice is fine.
3. **Registers the key** with the workspace and opens your browser back at Onboarding.

Then wait about ten seconds. The page shows a progress bar and unlocks itself. Once the page says **You're all set**, the whole app is open to you.

### Step 4: connect GitHub[​](#step-4-connect-github "Direct link to Step 4: connect GitHub")

**Required if you want to work on real Vinted repositories.** Not needed for templates.

![Getting access](/ape-docs/assets/images/ape-01-get-started-get-access-step-4-80a10bb7474a65a013b22136b6575296.png)

APE clones the repo as *you*, which is how per-repo access control works – so without a token, creating a session on `marketplace-web` or any other real project will fail outright. It's also what makes your pull requests open under your own name instead of a shared account.

If you only ever use templates, you can skip this and come back to it later from the settings page.

**Create the token.** On the Onboarding page, follow the GitHub step. The token needs the `repo` scope.

**Then authorise it for Vinted.** This is the step people miss. A token with the right scope still can't reach Vinted's repositories until you grant it SSO access, and the failure looks like the token being wrong rather than unauthorised.

Go to [github.com/settings/tokens](https://github.com/settings/tokens), find the token you just created, and in its row open the **Configure SSO** dropdown. Find the **Vinted** row and click **Authorize**.

***

## Where to go next[​](#where-to-go-next "Direct link to Where to go next")

* **[Quick start](/ape-docs/ape/getting-started/quick-start/.md)** – build something.
* **Engineers:** [CLI and SSH onboarding](/ape-docs/ape/reference/cli-and-ssh-onboarding/.md) covers `aiw create`, `aiw connect`, and working in Cursor over SSH.

If something went wrong, check the [Troubleshooting](/ape-docs/ape/reference/troubleshooting/.md) guide.

***

**Questions, problems, or ideas?** Ask in [#bloom-ape](https://vinted.slack.com/archives/C0B4X98C2R1) on Slack.
