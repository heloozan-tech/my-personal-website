# DESIGN.md — Fauzan Ardhiansyah, personal site

Direction: **quiet editorial**. Studied from pools.capital (type, color, grid, sharp corners)
and dhikaendi.com (how work is displayed: big image cards, small mono meta, one "view all").
Nothing is copied: no logos, copy, images or fonts from either site.

Feeling: a calm, expensive print magazine. Restraint over decoration.

## Color

| Token | Light | Dark | Role |
|---|---|---|---|
| `--bg` | `#F6F5F1` | `#0E0F11` | Page (warm paper) |
| `--surface` | `#FFFFFF` | `#16181B` | Cards, panels |
| `--ink` | `#121417` | `#ECEAE4` | Main text, solid buttons |
| `--ink-2` | `#2A2C30` | `#C9C6BE` | Secondary strong text |
| `--muted` | `#6A675F` | `#8E8A80` | Supporting text, second line of headings |
| `--line` | `rgba(18,20,23,.10)` | `rgba(236,234,228,.10)` | Grid lines, borders |
| `--dark` | `#0C0E11` | `#08090A` | Dark sections (reviews, footer) |
| `--amber` | `#C2772F` | `#D58A44` | The one accent: dots, step numbers, live badge |

Rule: the accent is only ever a small mark (a 6px dot, a number, a crop corner). Never a fill.

## Typography (free fonts, Google Fonts)

- **Display:** Newsreader, weight 300–400, letter-spacing −0.025em, line-height 1.02–1.06.
  Two-tone headings: second line in `--muted`.
- **Body:** Inter Tight 400/500, 15–17px, line-height 1.55.
- **Label:** Geist Mono 400, 11–12px, uppercase, letter-spacing +0.14em.

Scale (ratio ~1.375): 12 · 13 · 15 · 17 · 22 · 33 · 45 · 74 (hero, clamp on mobile).

## Space & layout

- Max width 1308px, gutter `clamp(16px, 4vw, 48px)`.
- Sections bounded by visible 1px `--line` rules (blueprint feel). Vertical rhythm 96–160px.
- **Radius: 0 everywhere.**

## Components

- **Button:** sharp box, 44px tall, 0 18px padding. Light (white on dark) or solid (ink).
  Hero CTA has amber crop-mark corners and an arrow cell split by a dashed rule.
- **Work card:** image (4:3) on top, footer bar below: name (Display 22) · category (Label) · 32px arrow box.
  Hover: image scales 1.03, arrow box fills ink.
- **Filter tabs:** label-style chips in a bordered strip; active = ink fill.
- **Section head:** `01` number + label left, two-tone serif heading, short muted paragraph right.
- **Live site row:** domain (mono) · name (Display) · one-line description · ↗.

## Motion

Easing `cubic-bezier(.2,.7,.1,1)`, 500–700ms. Reveal-on-scroll (fade + 12px rise).
All motion off under `prefers-reduced-motion`.
