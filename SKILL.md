---
name: think41-design
description: Use this skill to generate well-branded interfaces and assets for Think41, an AI-native engineering company. Contains essential design guidelines, brand colors and type, the Think41 logo, client logos, 9 slide templates, 5 tiered deck templates (L1–L5), and 6 case studies for prototyping decks, marketing assets, and product mocks in Think41's visual language.
user-invocable: true
---

Read the README.md file within this skill, and explore the other available files.

**Think41 visual identity in 30 seconds:**
- **Primary blue:** `#0060C7` — used for headlines, active nav, accent rules.
- **Deep blue:** `#003D82` — accent bars and contrast moments.
- **Logo mark:** vertical gradient cyan → mid-blue → violet (reserved for the mark; never used elsewhere).
- **Neutrals:** Tailwind gray scale (`#F9FAFB` → `#1A1A1A`).
- **Font:** Open Sans — weights 400, 600, 700, 800.
- **Brand wordmark:** "Think" in black, "41" as superscript in blue. Always.
- **Surfaces:** flat. White default, gray-50 for nested cards, solid blue for section dividers.
- **Cards:** 8–12px radius, 1px gray-200 border, no shadow by default.

**Slide chrome (1920×1080):**
- Nav strip across top: `Who We Are · Our Offerings · Case Study · Engagement Models · Team`. Active section highlighted in T41 blue.
- 80px outer margins. 56px top to nav, 140px to content start.
- Footer: Think⁴¹ wordmark left, section label right.
- Slide number top-right with blue numeral and "/ NN" total.

**Voice:**
- Confident, technical, results-oriented.
- Sentence case throughout, except UPPERCASE +0.14em eyebrows.
- Brand always rendered Think⁴¹ — never "Think 41" or "THINK41".
- No emoji. No vague enterprise vocabulary.

**If creating visual artifacts** (slides, mocks, throwaway prototypes):
- Copy assets out of `assets/` and slide templates from `slides/`.
- Duplicate the closest template in `slides/01-…` through `slides/09-…`.
- Reference tokens from `colors_and_type.css` — never hardcode hex.

**If working on production code:**
- Copy `colors_and_type.css` and follow the rules in README.md.
- The `--t41-*` CSS vars are the canonical tokens.

**Deck levels (in `decks/`)** — five tiered, full-deck templates built on the `<deck-stage>` runtime (keyboard nav, slide rail, print-to-PDF, editable PPTX export). Pick by reading commitment:
- **L1 Intro** (3 slides, ~60s) — airy, no nav strip. Identity drop.
- **L2 Pitch** (7 slides, ~5m) — standard 5-section nav. External sales pitch.
- **L3 Solutions** (9 slides, ~10m) — sub-section markers, service-line deep dive + 2 case studies.
- **L4 Partnership** (11 slides, ~15m) — deep-blue (#003D82) accent chrome, governance + pod model + team.
- **L5 SOW** (13 slides, ~25m) — phase-based nav (Phase 1/2/3), project name in chrome, investment summary, sign-off page.
- All levels share the brand system; they differ in structure + chrome, not visual language. To make a new deck, duplicate the closest level and edit content.

**Case studies (in `case-studies/`)** — six standalone 1920×1080 slides extracted from the master deck: Philips MRI, Honeywell CLSS, Atomicwork, Global Fashion Retailer (BigQuery), Top-5 Global Bank (voice), Mastercard. Each uses the blue-solution-panel + 2×2 capability-tile pattern. Drop any into a deck level as needed.

**Common slide patterns:**
- Hero: big black headline with one blue accent word + lede + client strip.
- 3-pillar layout: signature service-line pattern with eyebrow, icon, blue heading, bullet list, blue divider with key metric.
- Case study: solid blue solution panel (left, 5/12 width) + 2×2 capability tiles (right).
- Section divider: full-bleed blue, huge numeral, big sans heading.

If the user invokes this skill without other guidance, ask what they want to build, ask 3–5 focused questions (audience, length, deck or product, brand variants needed), then act as an expert Think41 designer who outputs HTML artifacts or production code.
