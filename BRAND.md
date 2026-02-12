# BRAND.md

Brand system documentation for [mo-maali.vercel.app](https://mo-maali.vercel.app).

---

## Brand Essence

> **Research to production. No shortcuts.**

This site represents a personal engineering portfolio with a **Dark Deco** visual identity — Art Deco geometry filtered through noir aesthetics. The design language is precise, structural, and atmospheric. No startup pastels. No playful energy. Precision, craft, restraint.

---

## Color Palette

| Name         | Hex         | CSS Variable       | Usage                                      |
|--------------|-------------|---------------------|---------------------------------------------|
| Matte Black  | `#1A1A1A`   | `--black`           | Primary background                          |
| Black Light  | `#222222`   | `--black-light`     | Card surfaces, terminal blocks              |
| Black Surface| `#2A2A2A`   | `--black-surface`   | Hover states, elevated surfaces             |
| Deep Purple  | `#6B21A8`   | `--purple`          | Accent borders, ambient glow, stack tags    |
| Purple Dim   | `#4C1D95`   | `--purple-dim`      | Subtle purple tones                         |
| Gold         | `#C9A84C`   | `--gold`            | Structural accents, nav, borders, links     |
| Gold Bright  | `#D4AF5A`   | `--gold-bright`     | Hover state for gold elements               |
| Gold Dim     | `#A8893A`   | `--gold-dim`        | Section numbers, labels, low-emphasis gold  |
| White        | `#F5F5F5`   | `--white`           | Primary text, headings                      |
| White Dim    | `60% opacity`| `--white-dim`      | Body text, secondary content                |
| White Faint  | `25% opacity`| `--white-faint`    | Metadata, timestamps, de-emphasized text    |
| Crimson      | `#8B0000`   | `--crimson`         | Reserved — emergency/alert contexts only    |

### Rules
- Gold is **structural**, not decorative. Use for borders, rules, labels, and links. Never for body text or backgrounds.
- Purple is **atmospheric**. Ambient glows, subtle border tints, tag backgrounds at low opacity. Never dominant.
- Crimson is **emergency only**. Reserved for critical states. Do not use casually.

---

## Typography

| Role       | Font             | Weight     | Usage                                 |
|------------|------------------|------------|----------------------------------------|
| Display    | Bebas Neue       | 400        | Section titles, hero name, nav labels  |
| Body       | DM Sans          | 300–500    | Paragraphs, card details, general text |
| Monospace  | JetBrains Mono   | 300–500    | Code, terminal blocks, metadata, tags  |
| Accent     | Playfair Display | 400 italic | Pull quotes, single impactful lines    |

### Rules
- Display type is **always uppercase**, always letterspaced (`2–8px` depending on size).
- Body type is **never bold** in running text. Use `font-weight: 500` for emphasis, not `700`.
- Monospace is used for anything technical, meta, or system-level. Version numbers, dates, labels, code.
- Playfair Display is used **sparingly** — one pull quote per page maximum. Always italic.
- No script fonts. No handwriting. No rounded/playful typefaces. Ever.

---

## Logo Marks

Three marks exist in the brand system. SVG source files live in `/assets/brand/`.

| Mark        | Description                                      | Context                              |
|-------------|--------------------------------------------------|--------------------------------------|
| **Primary** | SR-71 silhouette with integrated skeleton key     | Site header, favicon, watermark      |
| **Secondary** | Golden crescent moon over atmospheric pyramid  | Personal/editorial content           |
| **Tertiary** | MM geometric Art Deco monogram                  | Professional contexts, footer, email |

### Usage Rules
- Marks are rendered on `--black` backgrounds only. Never on white or light surfaces.
- The MM monogram is the default for inline/small usage (favicon, nav corner).
- Minimum clear space around any mark: 1× the mark's height on all sides.
- Do not recolor marks. Gold + white on black is the only approved treatment.

---

## Section Architecture

Each content section follows a consistent structure:

```
┌─────────────────────────────────────────────┐
│  [number]  SECTION TITLE  ────────────────  │
│                                             │
│  Body text (max-width: 640px)               │
│                                             │
│  [Cards / Grid / Content block]             │
│                                             │
│         ────── ◆ ──────                     │
└─────────────────────────────────────────────┘
```

- **Section number**: Bebas Neue, `2.8rem`, gold-dim at `40%` opacity.
- **Section title**: Bebas Neue, uppercase, letterspaced.
- **Section rule**: Gold gradient line, fades to transparent.
- **Deco divider**: Diamond ornament with flanking lines between sections.

---

## Component Patterns

### Credential Cards
- `1px` border in gold at `12%` opacity.
- On hover: border brightens to `30%`, background shifts to `--black-surface`.
- Label in mono uppercase, value in Bebas Neue, detail in DM Sans.

### Stack Tags
- Mono font, `0.72rem`, purple border at `30%` opacity.
- On hover: border goes full purple, text brightens.
- No background fill — just border + text.

### Terminal Blocks
- Purple-tinted header bar with three dots (gold, diminishing opacity).
- Body in JetBrains Mono. Prompt in gold. Output in purple. Comments in white-faint.

### Contact Links
- Gold border at `20%` opacity. Arrow (`→`) translates `3px` right on hover.
- No background fill by default. Subtle gold tint on hover.

### Pull Quotes
- `2px` left border in gold-dim.
- Playfair Display italic, `1.25rem`.
- Citation in mono uppercase below.

---

## Voice & Tone (for copy)

- **Concise.** Short sentences. No filler words. No "passionate about" or "driven individual."
- **Authoritative without performing.** State facts. Don't hedge with "I think maybe."
- **Technical precision.** Use correct terminology. Never dumb down for style points.
- **Zero self-promotion language.** No "guru," "ninja," "rockstar," "10x." Let the work speak.
- **No emoji in professional copy.** Exception: the key (🔑) in social contexts only.

---

## Do's and Don'ts

### Do
- Maintain the dark background everywhere. This is a dark-mode-only brand.
- Use gold for structure and purple for atmosphere.
- Keep body text at `max-width: 640px` for readability.
- Maintain generous vertical spacing between sections (`4–5rem`).
- Use Art Deco geometric dividers between sections.

### Don't
- Use light/white backgrounds. Ever.
- Mix in startup-style colors (teal, coral, pastel blue).
- Use rounded corners. Everything is sharp/angular.
- Add gradients to text.
- Use more than one pull quote per page.
- Add animations beyond subtle hover transitions (`0.2–0.3s ease`).
- Use stock photography or generic illustrations.

---

## File Structure

```
/
├── index.html          # Single-page site
├── BRAND.md            # This file
├── README.md           # Project readme
└── assets/
    └── brand/
        ├── mark-primary.svg
        ├── mark-secondary.svg
        └── mark-tertiary.svg
```

---

## Fonts (External)

Loaded via Google Fonts CDN:

```
https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:ital,wght@0,300;0,400;0,500;0,700;1,400&family=JetBrains+Mono:wght@300;400;500&family=Playfair+Display:ital,wght@0,400;0,700;1,400&display=swap
```

---

*Last updated: 2026-02-12*
