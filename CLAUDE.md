# Put It Live kit · instructions for Claude Code

This folder belongs to someone at the "Describe it. Build it. Put it live." workshop. They designed a one-page website in Claude Chat. Your job is to test that page, fix what is broken without changing the design, and leave it ready to drag onto Netlify Drop.

The person is not a developer. Explain what you did in plain words, short and clear.

## The folder

- `site/` is what goes live. When you are done it holds `index.html` and nothing else, unless the page really needs another file (an image the person added).
- `styles/` holds the three style guides: Riso Club, Field Guide, Late Show. The page follows one of them.
- `examples/` holds one finished example page per style guide. Use them as a reference for how a guide looks when done well.
- `prompts/` holds the prompts the person uses. You don't need them.

## When the person pastes their page

1. Save the code they paste as `site/index.html`, exactly as given. If they paste more than one version, use the last one. If the code is not a complete HTML page (no `<html>` or `<body>`), wrap it in a minimal HTML document with a charset and a viewport meta tag.
2. Work out which style guide the page follows from its colours and fonts. If you can't tell, ask: "Which style did you use: Riso Club, Field Guide or Late Show?"
3. Open `site/index.html` in the Browser pane and run the checks below. If there is no Browser pane, use whatever browser preview you have and say so in one line.
4. Fix only what fails. Never change the design, the words, the colours or the layout to suit your taste. If a fix would change how the page looks, ask first.
5. Report back with the table under "How to report".

Keep it quick: the person has about six minutes. Run all checks in one pass, fix, then re-check once. Don't loop.

## The checks

Run every check at 390px wide (phone) and 1440px wide (desktop).

| # | Check | Passes when |
|---|---|---|
| 1 | Errors | The browser console shows no errors. A Google Fonts file that fails only because you are offline doesn't count |
| 2 | Sideways scroll | The page is no wider than the screen at 390px |
| 3 | Text size | Paragraphs and list text are at least 16px on a phone. Labels, captions and credits may use the smaller sizes the style guide sets for them |
| 4 | Tap targets | Buttons, links and form fields are at least 44px tall on a phone |
| 5 | Contrast | Body text has at least 4.5:1 contrast with its background, large headings at least 3:1 |
| 6 | Motion runs | The motion the style guide asks for plays once, starting when the animated element itself is on screen (not just its section), then stops |
| 7 | Nothing stays hidden | Test by disabling the scroll observer: all content must then be fully visible at once by 2.5 seconds. With the observer working, content below the first screen must not be shown before the reader scrolls to it |
| 8 | Reduced motion | With reduced motion switched on, nothing moves and everything is visible |
| 9 | Self-contained | One file: CSS and JavaScript inline, fonts only from Google Fonts, no external images or scripts |
| 10 | Forms and buttons | Every form shows a result on the page after sending (no real sending), and shows errors in words. Every button does something visible |
| 11 | Links | Links to other sites open in a new tab. No links to files that don't exist |
| 12 | Title | The page has a real `<title>` (the name of the thing, not "Untitled") |
| 13 | Style guide | Colours, fonts, type sizes and signature moves match the style guide it follows. List anything that doesn't, but don't change it unless the person agrees |
| 14 | Readable on a phone | Look at the page at 390px, don't only measure it. Text inside drawings and diagrams is at least 12px on screen. Flag anything hard to read and suggest a fix, but ask before changing it |

## How to report

End with this, filled in:

| Check | Result |
|---|---|
| Errors | Pass / Fixed: what you fixed |
| ... | ... |

Then one line: "Your page is ready. Drag the `site` folder onto app.netlify.com/drop." If something still fails, say what and ask how they want to handle it.

## Rules

- No build tools, no npm, no frameworks. The page stays one HTML file.
- Don't add analytics, tracking, cookies or third-party scripts.
- Placeholders in square brackets stay as they are. Never invent names, numbers, testimonials or quotes.
- Never use em dashes in text you add.
