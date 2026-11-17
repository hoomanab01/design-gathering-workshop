# Put It Live kit

Everything for the workshop **Describe it. Build it. Put it live.** by Hooman Abbasi, Raise Studio.

You design a one-page website in **Claude Chat**, test it and get it ready in **Claude Code**, then put it live on **Netlify**. No coding needed.

## Download it

You don't need Git. On this page, click the green **Code** button, then **Download ZIP**. Unzip it somewhere you can find it, like your Desktop. The folder is called `design-gathering-workshop-main`.

## Start here

Double-click `start-here.html` in the folder. It opens the starter kit in your browser: the five steps with checklists, the style picker, the prompt builder and every prompt, ready to copy.

## What's inside

| Folder or file | What it is |
|---|---|
| `start-here.html` | The starter kit page: every step, checklist and prompt |
| `styles/` | Three style guides. Pick one and paste it into a Claude Project |
| `examples/` | One finished page per style guide, so you can see what good looks like |
| `prompts/` | The prompts for each step, ready to copy |
| `site/` | The folder that goes live on Netlify. Claude Code puts your page here |
| `CLAUDE.md` | Instructions Claude Code reads by itself: what to test and how to get your page ready |

## The three styles

| Style | Feels | Best for | Example |
|---|---|---|---|
| [Riso Club](styles/riso-club.md) | Playful, handmade, two inks | Events, campaigns, launches | Wiki Loves Monuments' "Join the contest" page, restyled |
| [Field Guide](styles/field-guide.md) | Calm, careful, drawn | Guides, trails, how it works | The National Park Service's Mist Trail guide for Yosemite, restyled |
| [Late Show](styles/late-show.md) | Cinematic, dark, slow reveals | Case studies, stories | A GOV.UK blog post about a Home Office service redesign, restyled |

To see an example, download the kit and double-click a file in `examples/`. It opens in your browser.

The examples restyle real, openly licensed web pages so you can see each style on real content. Each one credits its source and licence at the top and bottom. They are workshop demos and are not affiliated with those organisations.

## Before the workshop

- [ ] A paid Claude plan (Pro or higher)
- [ ] **Claude Desktop** installed and signed in. You use two tabs in it: **Chat** and **Code**
- [ ] This kit downloaded and unzipped
- [ ] A Netlify account, and you are signed in
- [ ] Optional test: drag the `site` folder onto **app.netlify.com/drop**. If you see "Your page goes here." at the link Netlify gives you, you are ready

## The steps on the day

### 1 · Set up (5 minutes)
1. In Claude, open **Settings**, then **Capabilities**, and switch on **Create and edit files**. Then open **Customize**, then **Skills**, and switch on `frontend-design`. If you like, also `web-artifacts-builder`, `theme-factory`, `canvas-design` and `algorithmic-art`. Help: [Use skills in Claude](https://support.claude.com/en/articles/12512180).
2. In the **Chat** tab, create a new **Project**. Name it after your idea.
3. Open the style guide you want from `styles/`, copy all of it, and paste it into the Project's instructions.
4. Upload the example page for your style from `examples/` to the Project as a file.
5. Have your real content ready: the text of a real page or document you want to turn into a page.

### 2 · Build in Claude Chat (17 minutes)
Start a chat inside your Project and use the build prompt in [`prompts/1-build-in-chat.md`](prompts/1-build-in-chat.md). Then add one bold move, then run the art director pass, both in the same file. When you're happy, copy the whole page code.

### 3 · Test and export in Claude Code (6 minutes)
Open the **Code** tab, start a new session on this kit folder, and use the prompt in [`prompts/2-test-in-code.md`](prompts/2-test-in-code.md). Claude Code saves your page into `site/`, checks it on phone and desktop, fixes what's broken and reports back.

### 4 · Put it live (5 minutes)
Drag the `site` folder onto **app.netlify.com/drop**. Steps in [`prompts/3-put-it-live.md`](prompts/3-put-it-live.md).

## Stuck?

The rescue prompts are at the bottom of [`prompts/1-build-in-chat.md`](prompts/1-build-in-chat.md). Last resort: start from the example for your style and swap in your own content.
