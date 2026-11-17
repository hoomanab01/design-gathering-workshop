# Riso Club · style guide

A page that looks printed on a risograph in a small studio: two fluorescent inks on cool paper, slightly off-register, loud and friendly. Made for things that should feel handmade and fun.

**Best for:** invitations, zines, launch pages for playful products, event and club pages, personal projects.
**Mood:** playful, warm, handmade, a little noisy.
**It is not:** corporate, minimal, glossy, dark mode, gradient-heavy.

## Colour, by role

| Role | Token | Value | Use |
|---|---|---|---|
| Paper | `--paper` | #EEF0EC | Page background |
| Ink | `--ink` | #1F1A2E | All body text and headlines |
| Pink | `--pink` | #FF48B0 | Big fills, shapes, stickers, highlights. Never text on paper |
| Blue | `--blue` | #0067A5 | Second ink: links, labels, shapes, text on paper is fine |
| Overprint | `mix-blend-mode: multiply` | | Where pink and blue shapes overlap, let them multiply into a third colour |

Text on pink is always `--ink`. Text on blue is always `--paper`. No other colours, no shadows except the off-register offset below, and no gradients except the halftone dots (the one allowed exception).

## Type

Load from Google Fonts: `Bricolage Grotesque` (wght 400 to 800) and `Space Mono` (400, 700).

| Level | Font | Size (desktop / phone) | Notes |
|---|---|---|---|
| Display | Bricolage Grotesque 800 | 96px / 52px | Tight line height 0.95, letter-spacing -2% |
| Heading | Bricolage Grotesque 700 | 44px / 32px | |
| Body | Bricolage Grotesque 400 | 20px / 18px | Line height 1.5, max 60 characters wide |
| Label | Space Mono 700 | 14px | Uppercase, letter-spacing 6%, for stickers, dates, prices |

## Signature moves

- **Off-register headline.** The display headline has a text-shadow of 4px 4px 0 `--pink` (3px on phones), as if the second ink slipped.
- **Halftone.** One large shape per section filled with a dot pattern: `radial-gradient(var(--blue) 1.5px, transparent 1.6px)` at `background-size: 10px 10px`. Place it behind a card or at the section's edge, never under running text. On a blue band, use a pink box with blue dots and no multiply.
- **Stickers.** Small labels in Space Mono on a pink or blue rectangle, rotated between -6° and 6°, overlapping an edge of a section. At most one sticker per section edge; on phones they stay fully inside the screen.
- **Overprint shapes.** Circles and blobs are not allowed; use rectangles, stars drawn in SVG and thick 6px underlines. Overlap one pink and one blue shape with multiply.

## Layout

- Wide margins (min 24px phone, 64px desktop), content up to 1100px.
- Sections alternate between a full-bleed pink or blue band and plain paper. Never two coloured bands in a row.
- Grids are allowed to feel collaged: one item per section may break the grid by 24px (12px on phones) or rotate up to 3°.
- Buttons: ink rectangle, paper text, 3px ink border, square corners, offset shadow 4px 4px 0 `--pink`. On press, the shadow disappears and the button moves 4px. On a pink band, the offset shadow is blue.

## Motion

- On load: the pink offset of the headline settles from 10px to 4px over 600ms, as if the print lines up.
- Stickers wobble once (rotate ±3°) when they scroll into view.
- Nothing loops. Respect `prefers-reduced-motion`: no motion at all.

## Voice

Chatty and warm, like a friend handing you a flyer.
- Do: "Bring snacks. We bring the music." Don't: "Refreshments will be provided."
- Do: short lines, one joke per section at most. Don't: exclamation marks everywhere (one per page).
- Do: name real things: the street, the time, the dish. Don't: "an unforgettable experience".

## Never

- Gradients (other than the halftone dots), glass, soft shadows, rounded pill buttons, emoji as decoration, stock photos.
- Pink text on paper (it fails contrast).
- Display and heading on the same screen. Labels don't count toward this.

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
