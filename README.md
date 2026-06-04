# Think41 Design System

A design system for **Think41**, an AI-native engineering company based in Bangalore (est. 2024). The founders previously scaled HashedIn by Deloitte from ~600 to 3,500+ engineers; Think41 is their GenAI-specialized follow-on, building enterprise-grade AI for clients including Honeywell, Mastercard, Philips, Harvey, Atomicwork, SpotDraft, and others.

This system was reverse-engineered from the master overview/portfolio deck and contains: brand colors and type tokens, the Think41 logo, client logos, a component library, and **9 slide templates** matching the source deck's visual language.

---

## Sources

- **Master deck:** `[MASTER] Think41 - Overview and Portfolio.pptx` (49 slides, 81 media assets)
- **GitHub:** [uttaranbiswas-code/Design-System-PPT](https://github.com/uttaranbiswas-code/Design-System-PPT)
- **Brand site:** [www.think41.com](https://www.think41.com)
- All raw extractions live in `uploads/` (slides text dump, theme XML, full media folder)

### Substitutions (flagged)

| Element | Source uses | This system uses | Why |
|---|---|---|---|
| Body font | Roboto family | **Open Sans** | User override — Roboto remains in source XML as reference |
| Icons | Flat-fill stock icons (Material/Iconfinder style) | **Lucide** outline icons, 1.75px stroke | Stock icons in the source are inconsistent in style and pixelated; Lucide gives a coherent line system |

If Think41 has licensed brand fonts/icons, swap them in `colors_and_type.css` and `preview/brand-iconography.html`.

---

## Index

```
/
├── README.md                    ← you are here
├── SKILL.md                     ← Agent Skill manifest
├── colors_and_type.css          ← tokens + element styles
├── image-slot.js                ← <image-slot> drop target
│
├── assets/
│   ├── think41-logo.png         ← original from deck (with grid bg)
│   ├── think41-logo-cropped.png ← clean lockup
│   ├── think41-mark.png         ← icon-only mark
│   └── clients/                 ← Deloitte, Atomicwork, Honeywell, Mastercard
│
├── preview/                     ← Design System tab cards
│
├── slides/                      ← Individual slide templates (1920×1080)
│   ├── index.html               ← gallery of all 9 templates
│   ├── slide-frame.css          ← shared chrome
│   ├── slide-fit.js             ← viewport scaler
│   └── 01-title.html … 09-closing.html
│
├── decks/                       ← Full deck templates by reading-level
│   ├── index.html               ← L1→L5 overview
│   ├── deck-stage.js            ← presentation runtime (rail, keyboard, print)
│   ├── L1-intro.html            ←  3 slides ·   60 sec  · airy, no nav
│   ├── L2-pitch.html            ←  7 slides ·  ~5 min  · standard pitch
│   ├── L3-solutions.html        ←  9 slides · ~10 min  · service-line deep dive
│   ├── L4-partnership.html      ← 11 slides · ~15 min  · deep blue, partnership
│   └── L5-sow.html              ← 13 slides · ~25 min  · phase-nav, SOW
│
└── case-studies/                ← Standalone case studies from master deck
    ├── index.html               ← gallery of all 6
    ├── philips-medtech.html     ← Life Cycle Engineering Copilot
    ├── honeywell-clss.html      ← Voice agent navigates CLSS platform
    ├── atomicwork.html          ← Universal AI Agent (Slack-native)
    ├── fashion-bigquery.html    ← 8-agent NL → BigQuery SQL
    ├── global-bank-voice.html   ← Voice multi-agent in regulated banking
    └── mastercard.html          ← Real-time analytics + ML anomaly detection
```

## Deck levels

Five distinct deck templates, calibrated for different reading commitments — all sharing the Think41 system (brand blue, Open Sans, 3-pillar offerings) but structurally distinct.

| Level | File | Length | Distinct chrome | Use case |
|---|---|---|---|---|
| **L1 Intro** | `decks/L1-intro.html` | 3 slides · ~60 sec | No nav strip, airy white space | Identity drop / business-card moment |
| **L2 Pitch** | `decks/L2-pitch.html` | 7 slides · ~5 min | Standard 5-section nav | External sales pitch |
| **L3 Solutions** | `decks/L3-solutions.html` | 9 slides · ~10 min | Sub-section markers | Service-line deep dive |
| **L4 Partnership** | `decks/L4-partnership.html` | 11 slides · ~15 min | Deep-blue (#003D82) accents, partnership framing | Engagement / governance proposal |
| **L5 SOW** | `decks/L5-sow.html` | 13 slides · ~25 min | Phase-based nav (Phase 1/2/3), project name in chrome | Concrete project SOW + investment |

All decks built on the `<deck-stage>` web component — keyboard navigation, slide rail, print-to-PDF, and editable PPTX export work out of the box.

## Case studies

Six standalone case-study slides (each 1920×1080), extracted from the master deck:

| Slide | Industry | Outcome |
|---|---|---|
| Philips MRI | Healthcare | Lifecycle change engineering: weeks → days |
| Honeywell CLSS | Industrial | Voice AI navigates platform · 35% L1 deflection |
| Atomicwork | Deep Tech | Universal AI Agent · 500+ DAU in Slack |
| Global Fashion Retailer | E-commerce | 8-agent NL → SQL · −35% BigQuery cost |
| Top-5 Global Bank | BFSI | Voice multi-agent in banking · ~40% faster |
| Mastercard | BFSI | Real-time analytics · 24 hr → 5 min detection |

Browse them all at `case-studies/index.html`. Each can be inserted into any deck level as needed.

---

## Content fundamentals

**Voice.** Confident, technical, results-oriented. Sentences are short. The deck mixes punchy headlines ("Operations on autopilot") with precise descriptions ("Multi-agent orchestration at enterprise scale"). Avoids vague enterprise vocabulary — no "synergize," no "leverage." Everything is concrete.

**Person.** First-person plural — "we" / "our" — for Think41. The reader is "you" / "your team." No "I."

**Casing.** Sentence case for headlines and body. Eyebrows and section labels are UPPERCASE with +0.14em–0.18em tracking. Section markers are numbered: **01**, **02**, **03**.

**Title patterns.** Two dominant styles, used consistently:
- **Action-result titles** that name what the work does: *"MedTech's compliance documentation that took days now starts already 80% done."*
- **Topic noun-phrases** for section headers: *"Our Offerings"*, *"Who We Are"*, *"Engagement Models"*.

**Brand name.** Always rendered with **41** as a superscript in blue: `Think⁴¹`. Never "Think 41" with a space, never "THINK41" all caps.

**Punctuation.** Em-dashes used liberally — for asides and emphasis. The phrase "Voice AI Enabled" appears on case studies as a labeled tag. Numbers always use digits (40%, 10×, $XXXk, 120+).

**Emoji.** Not used. The system uses iconography for visual accents.

**Tone examples.**

> ✅ "From strategy → Agent Implementation → Scale."
> ✅ "We are an AI-first engineering firm built to push enterprises beyond experimentation into real-world impact."
> ❌ "We're super excited to leverage AI to transform your business 🚀"

---

## Visual foundations

### Color

The brand revolves around a single signature blue, **#0060C7**, used for: headlines, the active nav chip, key buttons, accent rules, and stat numbers. It carries the brand. The deeper **#003D82** is used for accent bars and contrast moments (the case study label band). A blue tint scale (`#EFF5FE` → `#B7CFE9`) supports washes and chip backgrounds.

Neutrals follow the **Tailwind gray scale** — verified across 556 occurrences of `#374151` and similar tokens in the source XML. Text body is `#374151` (gray-700), secondary text `#6B7280` (gray-500), borders `#E5E7EB` (gray-200). Pure black is avoided in favor of `#1A1A1A`.

The logo mark itself uses a **vertical gradient** — cyan `#3DBEFE` (top) → mid blue `#3F5DF4` (45%) → violet `#6B3FE4` (base). This gradient does **not** appear elsewhere in the system — it's reserved for the mark.

### Typography

**Open Sans** is the brand face (per direction). Weight range used: 300 / 400 / 600 / 700 / 800. The deck originally specified Roboto + Roboto Condensed + Roboto Black + Open Sans; we standardize on Open Sans across.

- **Headlines and slide titles** — 44–80px, weight 700, color: T41 blue
- **Hero cover** — 128px+, weight 800, black with blue accent word
- **Body** — 18–22px, weight 400, gray-700
- **Eyebrows / nav** — 12–18px, weight 600, +0.14em tracking, UPPERCASE
- **Numerals (stat blocks)** — weight 800, blue, tight letter-spacing

Italic is used sparingly — only for short attribution lines and engagement-model taglines ("We own it. You get outcomes.").

### Backgrounds, imagery, and surfaces

- **White (#FFFFFF) is the default canvas** for content slides.
- **Gray-50 (#F9FAFB)** is used for nested card backgrounds and the soft gradient on the title slide.
- **Solid Think41 blue** (#0060C7) is used for the section divider slide (full bleed) and for the solution-callout panel on case study slides.
- **Gradient tinted backgrounds** appear only on the title slide: a soft `linear-gradient(135deg, #FFFFFF → #EFF5FE → #C9DAF8)` with a subtle grid overlay (80px lines @ 5% opacity blue).
- **No photography** anywhere in the source deck — the brand operates in flat surfaces + type + logos.
- **No emoji,** no hand-drawn illustrations, no decorative SVGs beyond the logo mark itself.

### Animation

Source deck is static (Google Slides export). For the HTML system:
- Transitions: **400ms** at `cubic-bezier(0.16, 1, 0.3, 1)` (expo-out).
- Hover: 200ms standard easing.
- No bounces, no scale-on-hover, no spring physics.

### Hover & press

- Primary button (T41 blue): on hover → `--t41-blue-deep` (#003D82). No transform.
- Outline button: on hover → `--t41-blue-50` (#EFF5FE) wash.
- Ghost button: on hover → `--gray-100` wash + `--black` text.
- Focus: 2px solid `--t41-blue` outline at 2px offset.

### Borders, rules, shadows

- **Hairline borders** dominate — 1px `--gray-200` (#E5E7EB) on cards.
- **Rule under section heads**: 2px solid `--t41-blue`.
- **Shadow scale** exists (`--shadow-1/2/3`) but the deck uses them sparingly. Prefer rules and color separation to drop shadows.
- **No inner shadows**, no neumorphism.

### Corner radii

- **Default 8px** (`--r-md`) for cards, buttons, chips, icon containers.
- **12px** (`--r-lg`) for the larger pillar tiles and solution panels.
- **4px** (`--r-sm`) for the active nav chip — tight, almost square.
- **Pill** (999px) for inline tag capsules.

### Transparency & blur

- No backdrop blur in source. None added.
- White-on-blue uses `rgba(255,255,255,0.7–0.85)` for secondary text on dark surfaces.
- The grid overlay on the title and section slides uses ~5% opacity.

### Layout — slide grid

Slides are **1920×1080**. Layout convention from the deck:
- **80px outer margin** (left & right)
- **56px top** for the nav strip
- **140px** from the top edge to the content start (below nav)
- **56px bottom** padding before footer
- **Footer at bottom 28px** — Think⁴¹ wordmark + section/page label
- **32px gutter** for grid columns

The signature **section nav strip** lives at top of every content slide: 5 sections (`Who We Are · Our Offerings · Case Study · Engagement Models · Team`), active chip filled with T41 blue, slide number top-right with the blue numeral and "/ NN" total.

### Cards

The deck's card style is consistent:
- 1px solid `--rule` border
- 8px or 12px radius
- White background (or `--gray-50` for secondary cards)
- Generous internal padding (28–40px)
- No drop shadow by default; shadow only on hover

The **solution callout** is a notable variant — solid T41 blue background, white text, with chip tags in the footer.

---

## Iconography

- **System:** Lucide (lucide.dev) — outline style, **1.75px stroke**, rounded caps & joins.
- **Substitution flag:** ⚠️ Source deck uses flat-filled bitmap icons (looks like Material Icons / Iconfinder stock). Lucide is a cleaner, more cohesive replacement.
- **Sizes:** 24px (inline), 28px (in pillar tiles), 56px container tiles with 6–12px radius.
- **Color:** T41 blue at low surface, white on dark.
- **Emoji:** never.
- **Unicode glyphs as icons:** only `→`, `↑`, `↓`, `×`, `+`, `·`, `—` used inline in text. Not used decoratively.

If Think41 has a licensed icon set, drop SVGs into `assets/icons/` and replace the Lucide CDN references in `preview/brand-iconography.html`.

---

## How to use

1. **Slides:** start from the closest template in `slides/`. Each file is self-contained. Reference `colors_and_type.css` + `slide-frame.css` + `slide-fit.js`.
2. **Slide chrome:** every content slide includes `.slide-nav` (top) + `.slide-pad` (content area) + `.slide-footer` (bottom). Mark the active section by adding `class="active"` to the right nav item.
3. **Tokens:** all colors, type, spacing, radii, motion live as CSS variables in `colors_and_type.css`. Never hardcode hex.
4. **Logo:** prefer `assets/think41-logo-cropped.png` (clean lockup). Use `assets/think41-mark.png` for icon-only contexts (favicon, small footer marks, dark surface placements).
5. **New case studies:** copy `slides/04-case-study.html`; keep the blue solution panel on the left and a 2×2 capability grid on the right.

---

## Caveats & open questions

- **Logo file:** the lockup is a PNG extracted from the deck. Vector (SVG) would be much better for crisp scaling — **ask Think41 for the SVG source**.
- **Font:** Open Sans selected per user direction. Source deck mixed Roboto, Roboto Condensed, and Roboto Black. If a brand font is owned, swap in `colors_and_type.css`.
- **Iconography:** stock icons in source replaced with Lucide. Confirm with brand team if there's an authoritative icon library.
- **Client logos:** only Honeywell, Mastercard, Atomicwork, and Deloitte are imported. The deck mentions many more (Philips, Harvey, SpotDraft, H&M, JPMC, Entero, Fireside Ventures) — import on demand from `uploads/think41-media/`.
- **No UI kit beyond slides.** The source is a deck, not a web product. If Think41's marketing site or product UI needs to be modeled, that's a follow-on ask.
- **Photography:** none in source, none added. If the brand uses imagery in other channels, add a photography section to this guide.
