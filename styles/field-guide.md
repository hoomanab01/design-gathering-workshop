# Field Guide · style guide

A page that reads like a naturalist's field guide: specimen plates, numbered figures, careful labels and hand-drawn lines on pale green paper. Calm, curious and precise. Made for things you explain or collect.

**Best for:** stories told step by step, city guides, recipes, collections, portfolios, "how it works" pages.
**Mood:** curious, calm, careful, quietly charming.
**It is not:** loud, techy, dark, salesy, playful in a cartoon way.

## Colour, by role

| Role | Token | Value | Use |
|---|---|---|---|
| Paper | `--paper` | #E4ECE0 | Page background |
| Plate | `--plate` | #F3F6F1 | Panels that hold a figure or a specimen |
| Ink | `--ink` | #1E3328 | Headlines, body text, drawn lines |
| Muted | `--muted` | #4F6357 | Captions, labels, metadata |
| Rust | `--rust` | #9A4A16 | Links, figure numbers, and one other highlight per section |
| Marigold | `--marigold` | #E9A23B | Fills only: dots on a map, a highlighted shape, a button. Text on it is `--ink` |

No gradients, no shadows. Separation comes from `--plate` panels and 1px `--ink` lines.

## Type

Load from Google Fonts: `Newsreader` (opsz, wght 300 to 600, italic too), `IBM Plex Mono` (400, 500) and `Caveat` (500).

| Level | Font | Size (desktop / phone) | Notes |
|---|---|---|---|
| Display | Newsreader 400 | 80px / 46px | Line height 1.02, one word in italic |
| Heading | Newsreader 500 | 36px / 28px | |
| Body | Newsreader 400 | 20px / 18px | Line height 1.55, max 62 characters wide |
| Label | IBM Plex Mono 400 | 13px | Uppercase, letter-spacing 8%: figure numbers, coordinates, dates |
| Annotation | Caveat 500 | 24px | Hand notes only, at most two per page, in `--rust` |

## Signature moves

- **Figures.** Every visual is a numbered figure: a `--plate` panel with a 1px ink border, the drawing inside, and a caption below in Plex Mono: "FIG. 3 · THE OVEN, 1964".
- **Drawn lines.** Illustrations are SVG line drawings in `--ink` with 1.5px strokes, round caps, no fills except one `--marigold` detail per drawing (on a map, the current or first stop).
- **Leader lines.** Labels connect to the thing they name with a thin dotted line, like a specimen plate.
- **Margin notes.** On desktop, short notes sit in a narrow left column beside the text, in Plex Mono, aligned to the line they comment on. On phones they sit under the paragraph.

## Layout

- A clear reading column (max 680px) with a left margin column for notes and figure numbers on desktop.
- Sections are chapters, each opening with a Plex Mono label ("CHAPTER 2 · THE STREET") and a Newsreader heading.
- Figures may go wider than the text column, up to 1040px. On phones, a wide figure becomes an upright version of itself rather than shrinking; text inside any drawing is never smaller than 12px on screen.
- Checkboxes and progress: ink outlines, marigold when checked or current.
- Buttons: `--marigold` fill, `--ink` text, 1px ink border, 4px radius, Plex Mono label. Links: `--rust`, underlined with 1px offset 3px.

## Motion

- Line drawings draw themselves when they scroll into view (SVG stroke-dashoffset over 1.2s, once).
- Text fades up 8px over 400ms, once.
- Respect `prefers-reduced-motion`: drawings appear complete, no movement.

## Voice

A patient guide who has walked the route many times.
- Do: "Turn left at the bakery. If it smells of cardamom, you are in the right place." Don't: "Discover hidden gems."
- Do: specific nouns, real numbers, real names. Don't: adjectives doing the work ("amazing", "unique").
- Do: one dry joke per page at most. Don't: exclamation marks.

## Never

- Photos with filters, stock images, emoji, icons from icon sets, gradients, drop shadows.
- Marigold as a text colour (it fails contrast).
- Centred body text.

## Craft rules (read these before building)

These separate a designed page from a generic one. They apply on top of everything above.

1. **Real content only.** Build from the content you are given. Never invent facts, numbers, dates, names, quotes, testimonials or features. If something is missing, leave it out or mark it `[like this]`.
2. **Structure comes from the content.** Find the content's own shape first (a sequence, a set of rules, a story, a comparison, a list of options) and build the sections around that shape. Never default to "hero, three feature cards, call to action".
3. **Every decoration carries information.** Each signature move (a sticker, a figure, a glow, a hand note) must hold a real fact from the content: a date, a number, a rule, a warning. If it has nothing to say, remove it.
4. **Use the signature moves sparingly.** Each one once or twice per page, where it matters most. Restraint is what makes the style readable.
5. **One strong idea per section.** One heading, the content it needs, at most one visual. Cut anything that repeats.
6. **Draw real data.** If the content has numbers, a sequence or a place, draw it (a timeline, a profile, a map, a before and after) with the real values as labels.
7. **Copy is short and specific.** Plain words, real names and numbers. No filler ("seamless", "unlock", "elevate", "journey"), no emoji, no exclamation marks.
8. **Typography does the work.** Use the type scale exactly, keep a comfortable reading width, align to a clear left edge, and leave generous space between sections.

## Delivery rules

- One self-contained `index.html`: CSS and JS inline, fonts only from Google Fonts.
- No external image URLs. Draw illustrations in SVG or CSS.
- Works at 390px wide with no sideways scroll; body text at least 16px; buttons at least 44px tall.
- Respect `prefers-reduced-motion`.
- Everything must be visible even if scroll animations never run: if the scroll observer has not started within 2.5 seconds, show all content at once.
- Reveal on scroll when about 15% of an element is visible, never only when it is fully in view (rotated or tall elements never count as fully in view).
- Decorations never cause sideways scrolling: use `overflow-x: clip` on sections, so elements may still overlap a section's top or bottom edge.
