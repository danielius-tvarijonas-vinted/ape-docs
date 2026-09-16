# Prompting the agent

The agent is Claude Code, running inside your session's container. It can read and write files, search the codebase, run commands, and check its own work against the running app.

What you get out of it depends mostly on how you ask.

## Writing a good prompt[​](#writing-a-good-prompt "Direct link to Writing a good prompt")

**Name the thing and the place.**

> Add a "Save for later" button to the item page, next to the Buy button.

Not:

> add a save button

**Say what shouldn't change.** The agent errs toward minimal changes, but being explicit removes any doubt.

> Change only the spacing. Don't touch the copy or the colours.

**One outcome per prompt.** Three unrelated changes in one message means three chances for one of them to be misread, and a single commit you can't partially undo. Send them separately.

**Point instead of describing** where you can. Clicking an element with Inspect is worth more than a paragraph of description – see [Pointing at things](/ape-docs/ape/the-workspace/pointing-at-things/.md).

**Say what's wrong, not how to fix it,** unless you know the codebase. "The cards are uneven heights on mobile" gets a better result than a guess at the CSS.

## Ask for a plan on big requests[​](#ask-for-a-plan-on-big-requests "Direct link to Ask for a plan on big requests")

The agent is instructed to plan before building when a request is large – three or more screens, a multi-step flow, a feature with both UI and state, an open-ended redesign.

**In practice it often doesn't.** If your request is clear enough to act on, it will usually just build the whole thing in one long run, which can take several minutes and lands as a single commit.

So if you want a plan, ask for one:

> Before you build anything, give me a numbered plan and wait for me to confirm it.

Add that to a large request and you'll get a list of slices – normally three to six, each one a coherent piece of work – and a question about how far to go before it starts.

### Why bother[​](#why-bother "Direct link to Why bother")

* **A checkpoint between pieces.** A wrong direction costs one slice, not the whole feature.
* **One commit per slice**, so you can revert part of the work instead of all of it.
* **Shorter runs.** A single run doing everything is more likely to fail partway through, and you wait longer to see anything.

The trade is speed. If you're confident in the request and happy to revert the lot if it's wrong, letting it build in one go is faster.

### Small requests[​](#small-requests "Direct link to Small requests")

A copy change, one component, moving a row – it just does it, and that's right. Asking for a plan on something that size is overhead.

## Tell it to ask you questions[​](#tell-it-to-ask-you-questions "Direct link to Tell it to ask you questions")

The agent can stop and ask you things, and it's genuinely useful – but it almost never does it on its own. Given a vague request it decides everything itself and starts building.

The fix is one sentence at the end of your prompt:

> build me a coffee shop site. Ask me anything you're unsure about before you start.

That reliably gets you questions instead of a finished guess. They appear as a card in the chat, the run pauses until you answer, and the card survives a page refresh if you need to go and think about it.

Worth making a habit at the start of anything open-ended. The questions are usually the ones you'd want to be asked – which screens matter, what style, where the data comes from – and answering three of them costs less than reverting a build that went the wrong way.

### Or just be specific[​](#or-just-be-specific "Direct link to Or just be specific")

If you already know what you want, say it and skip the back-and-forth:

> Build a landing page for a coffee shop – hero with a photo, opening hours, and a contact form. Warm and minimal, not corporate. Use placeholder content.

rather than:

> build me a coffee shop site

Either way, the thing to avoid is the vague prompt with no invitation to ask. That's the one where every gap becomes a choice made for you.

## Runs have a step budget[​](#runs-have-a-step-budget "Direct link to Runs have a step budget")

A run gets roughly 80 steps. Reading a file, writing one, running a command – each counts.

A run that hits the limit stops cleanly and shows a **Continue** pill. That's not an error and nothing is lost; the work so far is committed. Click Continue, or type your own instruction to redirect.

If you hit it often, your prompts are probably too big. Let the planning behaviour do its job rather than asking for everything at once.

## Sending while it's working[​](#sending-while-its-working "Direct link to Sending while it's working")

You don't have to wait. Anything you send while a run is going joins a **queue** and runs in order when the current one finishes.

The queue shows above the composer. You can remove individual items, or pause it if you want to see how the current change lands before the next one starts.

**Stop** aborts the current run. Work already committed stays.

## Attaching images[​](#attaching-images "Direct link to Attaching images")

Paste or drag up to four images per message. Screenshots, Figma exports, a photo of a whiteboard. The **+** next to the message box does the same thing if you'd rather pick a file.

That menu also has **Take screenshot**, which lets you drag a box over the preview and attach the crop – see [Pointing at things](/ape-docs/ape/the-workspace/pointing-at-things/.md).

## Talking to people instead[​](#talking-to-people-instead "Direct link to Talking to people instead")

Start a message with `@` and someone's name and it becomes a **note** – it goes to that person, not the agent, and doesn't start a run. See [Comments and notes](/ape-docs/ape/working-with-others/comments-and-notes/.md).

So Enter does one of three things depending on context: send a prompt, answer a pending question, or post a note. The composer changes colour to tell you which.

## Cost[​](#cost "Direct link to Cost")

Hover any of the agent's messages to see the tokens it used and a rough cost.

The numbers include *cache* tokens, which is why a first message in a session can look expensive relative to the ones after it – the agent is reading the codebase into its working memory once and reusing it. Long sessions get cheaper per prompt, not more expensive.

The figures are estimates against public list pricing. See [Reference](/ape-docs/ape/reference/reference/.md).

## When it gets stuck[​](#when-it-gets-stuck "Direct link to When it gets stuck")

* **It changed the wrong thing.** Revert to the previous prompt rather than asking it to undo. See [Files and history](/ape-docs/ape/the-workspace/files-and-history/.md).
* **It says it's done but the preview is broken.** Tell it. It has a screenshot tool that sees browser console errors, which is how it finds problems that don't appear in the terminal.
* **It's going in circles.** Stop the run, revert to the last good state, and re-prompt with more constraint. Continuing to add instructions on top of a confused state rarely recovers.

## Where to go next[​](#where-to-go-next "Direct link to Where to go next")

* **[Pointing at things](/ape-docs/ape/the-workspace/pointing-at-things/.md)** – clicking an element beats describing it, and it's the single biggest improvement to your prompts.
* **[Files and history](/ape-docs/ape/the-workspace/files-and-history/.md)** – checking what the agent changed, and going back when it's wrong.
* **[Comments and notes](/ape-docs/ape/working-with-others/comments-and-notes/.md)** – talking to people in the same chat, without starting a run.

***

**Questions, problems, or ideas?** Ask in [#bloom-ape](https://vinted.slack.com/archives/C0B4X98C2R1) on Slack.
