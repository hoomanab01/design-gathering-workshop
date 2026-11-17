# 1 · Build in Claude Chat

Use these in **Claude Chat**, inside the Project that holds your style guide.

## Before you start

Your Project holds two things: the style guide for your style (in the Project's instructions) and the example page for that style (uploaded as a file from `examples/`). The example shows Claude the level of craft you want.

Bring real content: the text of a real page, a document, or a Wikipedia article you want to restyle. Real content is what makes the page good. If you use someone else's text, credit it at the bottom of the page.

## The build prompt

Fill in the brackets, or use the prompt builder in the starter kit page, which writes this for you.

```
Here is the real content for my page:

[paste the text from your site, a document, or the page you are restyling]

Build [what you are making], for [who it is for]. They should feel [what they should feel]. At the end, they can [what they can do].

Use only this content: don't invent facts, numbers, names or quotes. Find the content's own structure and build the sections around it. Follow the [Riso Club / Field Guide / Late Show] style guide in this Project exactly, including its craft rules. The example page in this Project shows the level of craft I want: match its quality, not its content.

Deliver one self-contained HTML page that works on a phone. Then show me a preview.
```

## One bold move (pick one)

**Motion that tells the story**
```
Add one moment of motion that carries the story: one part should reveal as the reader scrolls to it. Keep the rest of the motion exactly as the style guide sets it, and respect reduced motion.
```

**An opening you can't scroll past**
```
Rewrite the first screen so it says the whole story in one line, with one striking visual drawn in SVG. Follow the style guide.
```

**Something to play with**
```
Add one small interaction the reader can play with: a choice, a slider, or a detail that appears on tap. It must work with a finger on a phone.
```

**Push the signature move**
```
Take the style guide's most distinctive rule and use it twice as boldly. Keep everything around it calm.
```

**A real ending**
```
End the page with something to do: a button, a form or a reveal, with a clear thank-you or result after it. No real sending, just show the result on the page.
```

## The art director pass (do this once, after the bold move)

```
Look at this page as a demanding art director. List the five things that look most generic, clumsy or invented, then fix all five without changing the content. Then go through the craft rules in the style guide one by one and fix anything that breaks them. Give me the whole page again.
```

## Rescue prompts

**It looks generic**
```
This looks like a template. Re-read the style guide and rebuild the page so a designer would recognise the style in one second. Keep my content.
```

**The preview is blank or broken**
```
The preview is blank or broken. Find the error, fix it, and give me the whole page again as one complete HTML file.
```

**It got too long**
```
Cut the page to five sections. Keep the strongest moment and the ending. Give me the whole page again.
```

**I'm out of time**
```
Simplify the page to what works now. Remove anything unfinished, keep it in the style guide, and give me the final file.
```

**Start from the example**

Paste this, followed by your real content:
```
Use the example page in this Project as the starting point. Keep its design, layout and motion exactly. Replace every word, number and drawing with my content below, and remove anything my content doesn't support. Give me the whole page as one HTML file.
```

## When you're happy

Copy the whole page code (the Copy button on the page Claude made) and move on to `2-test-in-code.md`.
