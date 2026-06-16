---
name: iris-complete
description: "Complete IRIS design system — brand identity, UI components, data visualization, and presentation skills for Claude Code. The all-in-one bundle for generating any IRIS surface: console UI, dashboards, landing pages, slide decks, data-viz screens, marketing pages, and partner collateral. Chains to iris-brand, iris-brand-ui, presentation, and dataviz sub-skills."
---

# IRIS Complete Design System

The top-level orchestrator for all IRIS design work. This skill chains to every
sub-skill in the IRIS system so you never have to remember which one to load.

**IRIS** — *Intelligence Risk Integrated Solutions* — is a Gogolook B2B product
for financial institutions. It detects high-risk accounts and assesses credit risk
using 3,000+ phone-intelligence features drawn from a 157M-number behavioral graph.

---

## 1. What's Included

| Sub-skill | Path | When to use |
|-----------|------|-------------|
| **iris-brand** | `../iris-brand/SKILL.md` | Brand identity, tone of voice, logo usage, color system, typography rules. Use for brand reviews, marketing copy, asset generation, brand compliance checks. |
| **iris-brand-ui** | `../iris-brand-ui/SKILL.md` | UI components, design tokens, console shell, KPI cards, form controls, data tables, icons. Use for building any IRIS interface — dashboards, console features, landing pages. Includes grill-me interview flow for scratch builds. |
| **presentation** | `presentation.md` | Slide deck generation — cover, agenda, section break, content, data dashboard, risk distribution, two-column, and summary/CTA slides. Use for pitch decks, partner presentations, internal reviews. |
| **dataviz** | `dataviz.md` | Data visualization patterns — risk color scale, chart palette, KPI cards, donut/ring charts, bar charts, line charts, mini donut metrics, accessibility rules. Use for any data-heavy screen or chart. |
| **checklist** | `checklist.md` | Comprehensive QA checklist covering brand + UI + presentation + dataviz. Run after every generation. |

---

## 2. Quick Start — Routing Logic

When the user requests IRIS work, detect the task type and route accordingly.

### Decision tree

```
User request
  |
  |-- Brand work (logo, colors, tone review, brand compliance)?
  |     -> Load ../iris-brand/SKILL.md
  |
  |-- UI work (components, dashboard, console, landing page)?
  |     -> Load ../iris-brand-ui/SKILL.md
  |     -> If building from scratch: run grill-me interview (5 questions)
  |     -> For data-heavy screens: also load dataviz.md
  |
  |-- Presentation / slide deck?
  |     -> Load presentation.md
  |     -> Also load dataviz.md if deck includes data slides
  |
  |-- Data visualization (charts, KPIs, risk distribution)?
  |     -> Load dataviz.md
  |     -> Also load ../iris-brand-ui/SKILL.md for component specs
  |
  |-- Mixed / unclear?
  |     -> Ask the user to clarify, then route
  |     -> For complex tasks, load all sub-skills
  |
  v
  After generation -> Run checklist.md review loop (up to 10 passes)
```

### Quick palette reminder

| Role | Token | Hex | Text rule |
|------|-------|-----|-----------|
| **Primary** | `--blue` (Azure) | `#41A9F6` | Accent/fill only — navy text on Azure, never white |
| **Secondary** | `--azure` (Gogolook Blue) | `#0058EA` | White text passes AA |
| **Accent** | `--iris` (Blue Iris) | `#5A5B9F` | White text passes AA (~6:1) |
| **Light accent** | `--sky` (Iris Sky) | `#7EDFFE` | Fill only — navy text |
| **Ink** | `--navy` (Iris Navy) | `#0F2647` | Headings, sidebar, dark surfaces |
| **Surface** | `--mist` (Iris Mist) | `#F3F8FE` | App background, cards |
| **Secondary text** | `--ink-2` | `#5A6577` | Body copy, captions |
| **Borders** | `--line` | `#E6ECF5` | Dividers, card borders |

Semantic risk (data viz only): High `#E5484D`, Med `#F5A623`, Low `#2FB87A`.

---

## 3. Skill Chain Map

```
iris-complete (this file)
  |
  +-- iris-brand/SKILL.md ............. identity, voice, logo, review
  |     +-- brand.md .................. full brand rules
  |     +-- voice.md .................. copy & tone rules
  |     +-- logo.md ................... logo usage rules
  |
  +-- iris-brand-ui/SKILL.md .......... components, tokens, grill-me
  |     +-- ui-system.md .............. component specs & CSS
  |     +-- tokens.json ............... machine-readable tokens
  |     +-- checklist.md .............. UI QA checklist
  |
  +-- presentation.md ................. slide deck rules (8 types)
  |
  +-- dataviz.md ...................... chart patterns & risk viz
  |
  +-- checklist.md .................... comprehensive QA (all domains)
```

When a sub-skill file is not yet present, fall back to the rules defined in the
project's `CLAUDE.md` (the IRIS brand source of truth).

---

## 4. Comprehensive Review Loop

After generating any output, run the full review:

1. **Load** `checklist.md` (or use the inline checklist from Section 5 below).
2. **Evaluate** every item. Mark PASS or FAIL with a specific note.
3. **Fix** each failing item immediately.
4. **Re-check** — iterate up to **10 passes** until all items pass.
5. **If an item cannot pass** (framework constraint, scope limitation), note it
   explicitly with the reason and trade-off.
6. **Present** the final output with a checklist summary.

### Inline comprehensive checklist

When `checklist.md` is not available, use this combined checklist.

#### Brand compliance
- [ ] Uses only IRIS palette colors — no off-palette colors
- [ ] Azure (`#41A9F6`) used as accent/fill only — navy text on Azure, never white
- [ ] Gogolook Blue (`#0058EA`) and Blue Iris (`#5A5B9F`) where AA contrast is needed
- [ ] Semantic risk colors only in data-viz context, never as decoration
- [ ] Brand gradient only in hero/marketing surfaces
- [ ] Plus Jakarta Sans for headlines, Inter for body — no other faces
- [ ] Tabular-nums on all scores, percentiles, table figures
- [ ] Tone is evidence-led, precise, functional — no hype
- [ ] Logo is logotype-only, correct clear space, not distorted

#### UI compliance
- [ ] Components follow iris-brand-ui specs (sizes, radii, padding)
- [ ] Space = clarity: generous whitespace, airy rhythm, light weights
- [ ] Focus states use Azure ring
- [ ] Console shell: navy sidebar, white main area
- [ ] WCAG AA contrast on all text
- [ ] Responsive below 760px

#### Presentation compliance (if applicable)
- [ ] Slide backgrounds follow type rules (navy/mist/white per slide type)
- [ ] Footer on every content slide (IRIS wordmark + confidentiality)
- [ ] Max one decorative element per slide
- [ ] Slide navigation works (arrow keys, click)
- [ ] Works as file:// without server

#### Data visualization compliance (if applicable)
- [ ] Risk colors used only for risk semantics — not decorative
- [ ] Chart brand palette: Azure, Gogolook Blue, Blue Iris for non-risk data
- [ ] Color never sole indicator — always paired with labels/icons
- [ ] Tabular-nums on all numeric values
- [ ] Chart labels readable at target size

---

## 5. Install

One install gets every IRIS sub-skill. Copy or symlink the entire `skills/`
directory from this repository into your project:

```bash
# Option A: symlink (recommended for active development)
ln -s /path/to/iris-brand-guideline/skills/iris-brand    ~/.claude/skills/iris-brand
ln -s /path/to/iris-brand-guideline/skills/iris-brand-ui ~/.claude/skills/iris-brand-ui
ln -s /path/to/iris-brand-guideline/skills/iris-complete ~/.claude/skills/iris-complete

# Option B: copy (for distribution)
cp -r /path/to/iris-brand-guideline/skills/iris-brand    ~/.claude/skills/
cp -r /path/to/iris-brand-guideline/skills/iris-brand-ui ~/.claude/skills/
cp -r /path/to/iris-brand-guideline/skills/iris-complete ~/.claude/skills/
```

After install, invoke with `/iris-complete` or let Claude Code auto-detect from
the skill description when working on IRIS tasks.

---

## 6. Relationship to Gogolook

IRIS is part of the Gogolook B2B anti-scam suite. When co-branding with the
Gogolook corporate logo, use "Gogolook IRIS" lockup. All IRIS material is
**Confidential & Copyright of Gogolook Co., Ltd.**
