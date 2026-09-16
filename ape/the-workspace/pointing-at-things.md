# Pointing at things

Describing a UI element in words is harder than it sounds. "The button at the top right of the search page" is four things the agent has to guess correctly before it even opens a file.

Clicking it removes the guessing.

## Inspect[​](#inspect "Direct link to Inspect")

Turn on **Inspect** from the floating toolbar over the preview.

Hover, and each element highlights with a label telling you what it is – the component name and the file it comes from. This is useful on its own, as a way to learn a codebase you don't know.

Click, and that element is attached to your next prompt. You'll see it as a chip above the composer. Now you can write:

> make this taller

...and the agent knows exactly which element, in which file, on which route.

Inspect stays on until you turn it off, so you can click, prompt, look, and click again without toggling.

### Why it works better[​](#why-it-works-better "Direct link to Why it works better")

Without it, the agent searches for something matching your description and picks the most likely candidate. Usually right, sometimes not, and on a large codebase "not" costs you a whole turn.

With it, the agent gets the component and the source file directly. The difference is biggest on projects like `marketplace-web`, where a component name might appear in a dozen places.

## Taking a screenshot[​](#taking-a-screenshot "Direct link to Taking a screenshot")

This one starts from the chat, not the toolbar. Click the **+** in the message box and choose **Take screenshot**.

Then drag a box over any part of the preview. The crop lands in your message as an image, ready to send with whatever you type.

Useful when the problem is visual and awkward to name:

> the spacing in this section is inconsistent – make it even

Two things worth knowing:

* The capture is of the **live page**, so open modals, dropdowns and hover states are included. If you can see it, you can capture it.
* It captures what's in the viewport, so scroll to what you want first.

## Using both together[​](#using-both-together "Direct link to Using both together")

Inspect and screenshots are separate controls, so nothing stops you using both on one message: grab a screenshot of the problem, turn on Inspect, click the element, and send them together.

That combination – a picture of what's wrong plus the exact file it lives in – is about as much context as you can hand over in one message.

## Attaching images from elsewhere[​](#attaching-images-from-elsewhere "Direct link to Attaching images from elsewhere")

You don't have to capture from the preview. Paste or drag any image into the chat, up to four per message.

A Figma export works well as a target:

> match this layout, using the components we already have

The agent can see the image. It can't open a Figma link, so export first.

## Where to go next[​](#where-to-go-next "Direct link to Where to go next")

* **[Prompting the agent](/ape-docs/ape/the-workspace/prompting-the-agent/.md)** – what to say once you've pointed at something.
* **[Comments and notes](/ape-docs/ape/working-with-others/comments-and-notes/.md)** – the same click, but leaving feedback for a person instead of an instruction for the agent.
* **[Files and history](/ape-docs/ape/the-workspace/files-and-history/.md)** – checking the agent changed what you meant.

***

**Questions, problems, or ideas?** Ask in [#bloom-ape](https://vinted.slack.com/archives/C0B4X98C2R1) on Slack.
