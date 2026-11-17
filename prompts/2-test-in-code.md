# 2 · Test and export in Claude Code

Use this in the **Code** tab of Claude Desktop, with this kit folder open.

## Open the kit folder in Claude Code

1. In Claude Desktop, click the **Code** tab, then **+ New**.
2. Under the prompt box, set the environment to **Local**, then use the **project folder** control to pick the `design-gathering-workshop-main` folder you unzipped.
3. Claude Code reads `CLAUDE.md` in this folder by itself. It already knows what to check.

## The test prompt

Paste this, then paste your page code right after it:

```
Here is my page from Claude Chat. Save it as site/index.html, run every check in CLAUDE.md at phone and desktop width, fix only what fails without changing the design, show it to me in the Browser pane, and report with the table.
```

## If something still fails

```
Fix the checks that still fail. Don't change the design. Show me the page again and the updated table.
```

## When the table is all Pass or Fixed

Move on to `3-put-it-live.md`.
