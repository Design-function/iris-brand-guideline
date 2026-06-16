# IRIS Brand Foundation

> This file is the brand identity reference for the iris-brand-ui skill chain.
> It mirrors the rules from `../iris-brand/SKILL.md` — the single source of truth.

---

## Brand Essence

- **Full name:** IRIS — Intelligence Risk Integrated Solutions
- **Tagline:** See risk clearly.
- **Personality:** expert · precise · trustworthy · clear
- **Positioning:** the expert risk lens for financial institutions — turning thousands
  of behavioral signals into clear, explainable decisions.
- **Core idea:** the iris of an eye — perception, focus, clarity. IRIS brings risk
  into focus.

---

## Color System

### Primary, Secondary & Accents

| Role | Token | Name | Hex | Text Rule |
|------|-------|------|-----|-----------|
| **Primary** | `--blue` | Azure | `#41A9F6` | Accent/fill only — navy text on Azure fills, never white |
| **Secondary** | `--azure` | Gogolook Blue | `#0058EA` | White text passes AA |
| **Accent** | `--iris` | Blue Iris | `#5A5B9F` | White text passes AA (~6:1) |
| **Light accent** | `--sky` | Iris Sky | `#7EDFFE` | Fill only — navy text |

### Foundations

| Token | Name | Hex | Use |
|-------|------|-----|-----|
| `--navy` | Iris Navy | `#0F2647` | Ink, headings, sidebar, dark surfaces |
| `--mist` | Iris Mist | `#F3F8FE` | App background, cards |
| `--white` | White | `#FFFFFF` | Content surfaces |
| `--ink-2` | — | `#5A6577` | Secondary text |
| `--line` | — | `#E6ECF5` | Borders, dividers |

### Brand Gradient

`#0058EA → #41A9F6 → #7EDFFE` (Gogolook Blue → Azure → Sky) — hero/marketing only.

### Semantic Risk Scale (data viz only)

| Level | Hex | Meaning |
|-------|-----|---------|
| High risk | `#E5484D` | High-risk factor / reject |
| Medium risk | `#F5A623` | Caution / manual review |
| Low risk | `#2FB87A` | Low risk / approved |

Never use red/amber/green as brand or decorative color.

---

## Typography

| Role | Font | Weights | Use |
|------|------|---------|-----|
| Primary | Plus Jakarta Sans | 300–800 | Headlines (700/800), logotype (300–500) |
| Secondary | Inter | 400/500/600 | Body copy, tabular-nums for all figures |
| Regional | Noto Sans | 400/500/700 | CJK + multilingual body |

- Headlines: Plus Jakarta Sans, tracking -0.02em, weight 700/800.
- Body: Inter 400/500, line-height 1.5–1.6.
- Numbers: Inter `font-variant-numeric: tabular-nums` — always.
- Do not introduce other typefaces.

---

## Logo

- **Logotype-only** brand — no pictorial symbol.
- SVG files: `assets/IRIS_logo_Dark_RGB.svg` (navy), `assets/IRIS_logo_White_RGB.svg` (white).
- viewBox: `0 0 1088.38 409.56`.
- Navy on light backgrounds; white on dark; gradient fill for hero/marketing only.
- Circle containment for app mark (console, avatar, favicon).
- Clear space: cap-height on all sides. Min size: 64px wide; circle mark 28px.
- Never bold, condense, stretch, add effects, recolor off-palette.

---

## Voice & Tone

IRIS speaks like a **trusted risk expert**: calm, precise, evidence-led.

1. **Clarity over complexity** — plain language, define terms on first use.
2. **Evidence over assertion** — lead with metrics (Gini, default rate, percentile).
3. **Confident, never hyped** — no "revolutionary", "magic", "game-changer".
4. **Respect the stakes** — exact about scores, limits, explainability.

**Voice by surface:** product UI = terse/functional, sales = outcome-led, docs = exact/imperative.

---

## Layout Principle

**Space = clarity.** Generous whitespace, airy section rhythm, light type weights,
wide-tracked headlines. The layout itself is the visual proof of the promise.

---

## Relationship to Gogolook

IRIS is part of the Gogolook B2B anti-scam suite. Co-brand with the Gogolook logo
in sales/partner contexts ("Gogolook IRIS"). All IRIS material is **Confidential &
Copyright of Gogolook Co., Ltd.**
