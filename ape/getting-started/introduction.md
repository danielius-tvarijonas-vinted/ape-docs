# Introduction

![Introduction](/ape-docs/assets/images/ape-hero-introduction-4a7b9b780fed76a29b543a0653a1cda4.png)

**APE** – **the Agentic Prototyping Environment** – is Vinted's internal AI prototyping environment.

You describe what you want. APE builds a working version you can click through, put in front of people, and iterate on – with your colleagues in the same prototype at the same time, not passing files between them. Not a picture of an interface: a running one.

You don't need to start from a blank canvas. APE opens **Vinted's production GitHub repositories** directly – like `marketplace-web` and others – cloned and running, so you can prototype a change to the app that's live today rather than rebuilding an approximation of it first.

When production code isn't the right starting point, there's a **library of templates**: consumer app shells, the Bloom and Vinted Go design systems, marketplace and admin scaffolds, internal-tool patterns. They're generated from production code, so what you build already looks and behaves like Vinted, which is usually the slowest part of getting a prototype to feel real.

## Why it exists[​](#why-it-exists "Direct link to Why it exists")

Product work today is spread across a lot of places. Wireframes and design in one tool, the thinking in a doc somewhere else, user journeys in a third, and a working prototype only if someone finds engineering time to build one.

APE is being built to collapse that into a single continuous flow – the one place product work happens before it reaches production. Discovery and delivery in the same environment, rather than a handoff between them.

## Who it's for[​](#who-its-for "Direct link to Who it's for")

**Designers, PMs, and researchers.** Those are the core users, and the product is shaped around them: you work in prose and by pointing at things, not in a terminal.

Engineers are welcome too, and the tool is built for them to receive work as much as produce it: a prototype comes with real code, a readable commit history, and a pull request when it's worth shipping, so a handoff is a branch to review rather than a specification to interpret.

**Internal Tools** use APE for something different. Rather than prototyping a change to a customer-facing product, they build the internal app itself – admin panels, ops dashboards, the small tools a team needs to do its work. There are templates for exactly that, and because what comes out is real code rather than a mockup, a first working version is a foundation instead of something to be rebuilt properly later.

## Why we built it rather than adopting a third-party tool[​](#why-we-built-it-rather-than-adopting-a-third-party-tool "Direct link to Why we built it rather than adopting a third-party tool")

There are third-party tools that do a version of this. None of them embed with Vinted's infrastructure, workflows, and data the way we need. Control, interoperability, and security aren't things we were willing to trade away.

Owning it means APE can connect to the rest of Vinted in ways a third-party tool can't:

* **Direct access to production repositories.** Not an export or a sync – the real repo, cloned into your session.
* **Templates generated from production code**, so they stay close to the real thing instead of drifting into a parallel design language.
* **Prototypes can talk to real APIs**, so a flow can be tested with real data.

The consequence is that what you build is real source code from the start. Real components, real routing, real styles, which is also why a prototype can become a pull request rather than a specification for one.

## What you can do today[​](#what-you-can-do-today "Direct link to What you can do today")

* **Prototype on a real Vinted codebase**, or on a template if you'd rather start clean.
* **Build an internal tool from nothing** – an admin panel, an ops dashboard, a small app a team has been asking for.
* **Work by pointing.** Click an element in the running app and tell the agent what to change about it.
* **Co-create.** Several people can work in the same session at once, and everyone sees changes as they happen.
* **Collect feedback in place.** Reviewers open a link and leave comments pinned to specific elements – no account setup, no local install.
* **Publish to a URL** that works for anyone, on any device.
* **Open a pull request** when a prototype turns out to be worth shipping.

## Where it's going[​](#where-its-going "Direct link to Where it's going")

APE is early. These are the directions it's being built toward, not things you can do today:

* **The full range of product work in one place** – wireframing, writing docs, and mapping user journeys alongside building UI.
* **Real member experiments**, so prototypes can be tested with Vinted users directly rather than only inside the company.
* **A backend and a database**, so a prototype can store and read real data.
* **Naming who can open a prototype.** Today a published prototype is a public URL, with a shared password at best. Instead you'll list the people who should have access and they'll sign in with their own accounts.
* **Handoff to native mobile.** Web prototypes already hand off as a branch, but native mobile engineers can't use one. A design-system-aware export will translate what you build into something they can implement against in iOS and Android codebases.
* **Design system documentation inline.** Component guidance, usage rules, and the reasoning behind them available inside APE, so choosing the right component doesn't mean leaving the session to go and read about it.
* **Content design system integration**, so that copy in your prototype follows Vinted's content standards as you build rather than being corrected afterwards.
* **Purpose-led design built in.** Vinted's purpose-led design method – working out why something is worth building before deciding what it looks like – available as part of the flow, so the product design workflow is something APE supports rather than something you hold in your head alongside it.

If something in this list is what you actually need right now, that's useful to know – tell us.

## Where to go next[​](#where-to-go-next "Direct link to Where to go next")

* **[Getting access](/ape-docs/ape/getting-started/getting-access/.md)** – two clicks and one command, if you haven't signed in yet.
* **[Quick start](/ape-docs/ape/getting-started/quick-start/.md)** – a working prototype in five minutes.
* **[How your work is saved](/ape-docs/ape/concepts/how-your-work-is-saved/.md)** – read this before pointing an agent at a repo you care about.

***

**Questions, problems, or ideas?** Ask in [#bloom-ape](https://vinted.slack.com/archives/C0B4X98C2R1) on Slack.
