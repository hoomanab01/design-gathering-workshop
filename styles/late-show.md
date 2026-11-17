# Late Show · style guide

A page that plays like the opening of a film: dark screen, title cards, slow reveals and one warm light. Every section is a scene. Made for stories with feeling and a moment of reveal.

**Best for:** personal stories, launches with a reveal, portfolios with drama, memorials and anniversaries, anything told in scenes.
**Mood:** cinematic, warm, intimate, slow.
**It is not:** techy dark mode, neon, busy, cheerful, corporate.

## Colour, by role

| Role | Token | Value | Use |
|---|---|---|---|
| Night | `--night` | #120E16 | Page background |
| Screen | `--screen` | #1C1622 | Panels, cards, the second ground |
| Cream | `--cream` | #EFE6D8 | Headlines and body text |
| Muted | `--muted` | #A89DA8 | Captions, credits, scene labels |
| Amber | `--amber` | #E8B04B | The one warm light: key words, the main button, a glow. Text on amber is `--night` |
| Rose | `--rose` | #E08A7E | Second accent, used at most once per section |

One soft glow per scene is allowed: a radial gradient of `--amber` at 18% opacity behind the key element, like a lamp. The glow stays inside its scene and never wider than the screen. No other gradients.

Amber marks at most one key phrase per scene, plus the scene label's time. Illustrations may use darker and lighter shades of these colours (dark plums, warm browns) in flat fills, no gradients.

## Type

Load from Google Fonts: `Cormorant Garamond` (400, 500, 600, italic 400 and 500) and `Manrope` (400, 500, 700).

| Level | Font | Size (desktop / phone) | Notes |
|---|---|---|---|
| Title card | Cormorant Garamond 400 italic | 116px / 60px | Line height 1.0, letter-spacing -1% |
| Heading | Cormorant Garamond 500 | 50px / 36px | Quotes and key lines in Cormorant italic, never smaller than 24px: it is a delicate face |
| Body | Manrope 400 | 19px / 17px | Line height 1.65, max 56 characters wide |
| Credit | Manrope 500 | 13px | Uppercase, letter-spacing 18%: scene labels and credits |

## Signature moves

- **Scenes.** Each section fills at least 80% of the screen height and opens with a credit line: "SCENE 2 · THE NIGHT BUS".
- **Letterbox.** The opening scene sits between two thin black bars (top and bottom, 6vh) like a widescreen frame.
- **Film grain.** A fixed, subtle noise overlay at 6% opacity across the page, made with an SVG `feTurbulence` filter.
- **The reveal.** One sentence per page appears word by word. Use it for the turning point of the story.
- **End credits.** The page ends with a centred credits block in Manrope credits style: who made it, with what, and when. For a made-up story, say it is fictional.

## Layout

- Generous darkness: big empty space around few words. One idea per scene.
- Side margins: 20px on phones, 64px on desktop. Cards and panels sit on `--screen` with no border.
- Text sits left-aligned in a narrow column, except the title card and the end credits, which are centred.
- Images and illustrations sit in a 2.39:1 frame (`aspect-ratio: 2.39 / 1`) on `--screen`, drawn in SVG or CSS.
- Buttons: `--amber` fill, `--night` text, no border, 2px radius, Manrope 700. Secondary: 1px `--cream` outline.

## Motion

- Scenes fade in from black over 900ms as they scroll into view, once.
- The title card fades up slowly (1.4s) on load.
- The word-by-word reveal runs once, 120ms per word.
- The grain stays still. Respect `prefers-reduced-motion`: everything visible at once.

## Voice

A narrator speaking quietly, in the present tense.
- Do: "It is 1:40 am. The bus is empty except for us." Don't: "Join us on an incredible journey."
- Do: short sentences, one image per sentence. Don't: lists of features.
- Do: let silence work, leave space. Don't: exclamation marks, ever.

## Never

- Neon, bright blue, green or purple accents, glassmorphism, emoji, stock photos.
- More than one glow per screen.
- Light backgrounds or white sections.

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
