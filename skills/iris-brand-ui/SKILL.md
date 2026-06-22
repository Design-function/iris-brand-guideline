---
name: iris-brand-ui
description: "IRIS brand identity + UI system for building IRIS-branded interfaces. Use when generating any IRIS surface: console UI, dashboards, landing pages, marketing pages, API docs, partner decks, or data-viz screens. Also use when reviewing existing IRIS assets for brand and UI compliance."
---

# IRIS Brand Identity + UI System

You are working on **IRIS** — *Intelligence Risk Integrated Solutions* — a Gogolook B2B product that helps financial institutions detect high-risk accounts, assess risk levels, and optimize risk processes using 3,000+ phone-intelligence features drawn from a 157M-number behavioral graph.

Every output must follow the IRIS brand rules and UI component spec. Read the supporting files before generating.

---

## 1. Quick Reference

### Brand tokens
| Role | Token | Hex | Text rule |
|------|-------|-----|-----------|
| **Primary** | `--blue` (Azure) | `#41A9F6` | White text/icons on Azure fills |
| **Secondary** | `--azure` (Gogolook Blue) | `#0058EA` | White text passes AA |
| **Accent** | `--iris` (Blue Iris) | `#5A5B9F` | White text passes AA (~6:1) |
| **Light accent** | `--sky` (Iris Sky) | `#7EDFFE` | Fill only — navy text |
| **Ink** | `--navy` (Iris Navy) | `#0F2647` | Headings, sidebar, dark surfaces |
| **Surface** | `--mist` (Iris Mist) | `#F3F8FE` | App background, cards |
| **Secondary text** | `--ink-2` | `#5A6577` | Body secondary, captions |
| **Borders** | `--line` | `#E6ECF5` | Dividers, card borders |

### Typography
- **Headlines:** Plus Jakarta Sans 300, tracking -0.02em
- **Body:** Inter 400/500, line-height 1.5-1.6
- **Data/scores:** Inter tabular-nums
- **Regional:** Noto Sans 400/500/700 (CJK/TH)

### Semantic risk (data viz only — never decorative)
| Level | Hex |
|-------|-----|
| High risk | `#E5484D` |
| Medium risk | `#F5A623` |
| Low risk | `#2FB87A` |

### Brand gradient (marketing/hero only)
`#0058EA -> #41A9F6 -> #7EDFFE` (Gogolook Blue -> Azure -> Sky)

---

## 2. Before You Generate

### Step 1 — Identify the task

Ask the user:

> Are you **(A) applying IRIS UI tokens to an existing project**, or **(B) building something from scratch**?

### Path A — Existing project

Proceed directly. Apply tokens from [tokens.json](tokens.json), use component specs from [ui-system.md](ui-system.md), and validate against the checklist in [checklist.md](checklist.md).

### Path B — Building from scratch (grill-me)

Before writing any code or markup, interview the user to gather context. Ask these questions **one at a time**, waiting for each answer before proceeding:

1. **What are you building?**
   Console feature, landing page, dashboard, marketing page, API docs, partner deck, email template, mobile screen, or something else?

2. **Who is the primary user?**
   Risk analyst, fraud officer, credit team lead, developer integrating the API, sales prospect, or partner executive?

3. **What data will be displayed?**
   Risk scores, phone intelligence features, batch screening results, trend analytics, single-lookup results, model performance metrics, or onboarding flows?

4. **What is the deployment context?**
   Internal Gogolook tool, client-facing IRIS console, public marketing site, partner-facing deck, printed collateral, or developer documentation?

5. **Any existing constraints?**
   Framework (React, Vue, vanilla), design system it must integrate with, responsive requirements, accessibility level (AA/AAA), browser support, or dark-mode needs?

Only after gathering answers to all five questions should you proceed with implementation.

---

## 3. Brand Foundation

Read [brand.md](brand.md) for the full IRIS brand identity:

- Brand essence, tagline ("See risk clearly."), positioning
- Tone of voice: clarity over complexity, evidence over assertion, confident never hyped, respect the stakes
- Logo usage: logotype-only (Direction 4 — Chain/Lines), circle containment mark, clear space, min sizes
- Color system: primary/secondary/accent roles, contrast rules, semantic risk scale
- Typography: Plus Jakarta Sans / Inter / Noto Sans stack
- Relationship to Gogolook parent brand

**If `brand.md` is not present**, fall back to the brand rules defined in the project's `CLAUDE.md`.

---

## 4. UI Component System

Read [ui-system.md](ui-system.md) for the full IRIS UI component specification:

- CSS custom properties (design tokens)
- Buttons: primary, secondary/outline, accent, ghost, disabled (sm/default/lg)
- Form controls: inputs, selects, toggles, focus ring
- Badges: brand (blue, azure, iris) + risk (high, med, low)
- Risk levels: A-E scale with 5-stop color ramp
- Score display: large score number, percentile bar
- Data tables: header background, border-bottom rows, tabular-nums
- Console shell: navy sidebar, white main area, quota card
- KPI cards: value, label, sparkline, trend badge
- Charts: horizontal bar chart, area line chart, mini donuts
- Iconography: stroke-based, 1.6px, round caps/joins, 24x24 viewBox

---

## 5. Design Token Reference

Read [tokens.json](tokens.json) for programmatic access to all design tokens:

- Colors (primary, secondary, accent, foundation, semantic)
- Typography (families, weights, sizes, line-heights)
- Spacing (4px base scale)
- Border radius
- Shadows (elevation levels)
- Breakpoints

Use these tokens when generating CSS, Tailwind config, Figma variables, or any design-system integration.

---

## 6. Output Checklist

After generating any output, validate it against these combined brand + UI rules:

### Brand compliance
- [ ] Uses only IRIS palette colors — no off-palette colors
- [ ] Azure (`#41A9F6`) fills use white text/icons
- [ ] Gogolook Blue (`#0058EA`) and Blue Iris (`#5A5B9F`) used where AA text contrast is needed
- [ ] Semantic risk colors (red/amber/green) appear only in data-viz context, never as decoration
- [ ] Brand gradient used only in hero/marketing surfaces, not product UI
- [ ] Typography uses Plus Jakarta Sans for headlines, Inter for body — no other faces
- [ ] Tabular-nums applied to all scores, percentiles, table figures
- [ ] Tone is evidence-led, precise, functional — no hype words ("revolutionary", "magic", "game-changer")
- [ ] Logo is logotype-only, not stretched/recolored/shadowed

### UI compliance
- [ ] Components follow the spec in ui-system.md (sizes, radii, padding)
- [ ] Space = clarity: generous whitespace, airy section rhythm, light weights
- [ ] Focus states use Azure ring (`box-shadow: 0 0 0 3px rgba(65,169,246,.18)`)
- [ ] Data tables use Iris Mist header background with border-bottom row separation
- [ ] Console shell uses navy sidebar, white main area
- [ ] KPI cards show value + label + trend badge
- [ ] Icons are stroke-based, 1.6px stroke-width, round linecap/linejoin
- [ ] WCAG AA contrast maintained on all text elements
- [ ] Responsive: components adapt gracefully below 760px

---

## 7. Review Loop

After generating output:

1. Run the checklist above (or load [checklist.md](checklist.md) if available).
2. For each failing item, fix the issue and re-check.
3. Iterate up to **10 passes** until all items pass.
4. If an item cannot be resolved (e.g., a framework constraint), note it explicitly and explain the trade-off.
5. Present the final output with a summary of checklist results.

---

## Supporting Files

| File | Purpose |
|------|---------|
| [brand.md](brand.md) | Full brand identity (essence, tone, logo, color, type) |
| [ui-system.md](ui-system.md) | UI component specification with CSS and usage guidance |
| [tokens.json](tokens.json) | Machine-readable design tokens (colors, type, spacing, radii, shadows, breakpoints) |
| [checklist.md](checklist.md) | Brand + UI QA checklist for review loop |
