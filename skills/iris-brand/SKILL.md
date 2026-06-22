---
name: iris-brand
description: "IRIS B2B brand — visual identity, voice, color, typography, logo, layout. Use when generating any IRIS-branded content: product UI, sales decks, marketing copy, data visualizations, API docs, partner materials, or web pages. Also use when reviewing existing IRIS assets for brand compliance."
---

# IRIS B2B Brand Identity

You are working on brand assets for **IRIS** (Intelligence Risk Integrated Solutions) — a Gogolook B2B fintech product that helps financial institutions detect high-risk accounts and assess credit risk using 3,000+ phone-intelligence features drawn from a 157M-number behavioral graph. Every output must reflect the IRIS identity: expert, precise, trustworthy, and clear. Read the relevant sections below before generating.

## Quick Reference

- **Primary color:** `#41A9F6` (Azure — CSS `--blue` — primary actions, links, active states. White text/icons on Azure fills)
- **Secondary color:** `#0058EA` (Gogolook Blue — CSS `--azure` — secondary highlights, data-viz, icons. White text passes AA)
- **Accent:** `#5A5B9F` (Blue Iris — CSS `--iris` — muted surfaces, supporting accents. Ties to the name. White text passes AA ~6:1)
- **Light accent:** `#7EDFFE` (Iris Sky — CSS `--sky` — tints, hover fills, chart-light, glows on dark. Fill-only)
- **Navy:** `#0F2647` (Iris Navy — CSS `--navy` — ink, headings, sidebar, dark surfaces)
- **Mist:** `#F3F8FE` (Iris Mist — CSS `--mist` — app background, cards, lightest surface)
- **Secondary text:** `#5A6577` (CSS `--ink-2`)
- **Borders:** `#E6ECF5` (CSS `--line`)
- **Brand gradient:** `#0058EA -> #41A9F6 -> #7EDFFE` (hero/marketing only)
- **Headings font:** Plus Jakarta Sans 700/800, -0.02em tracking
- **Body font:** Inter 400/500, 1.5-1.6 line-height
- **Data/figures font:** Inter tabular-nums (always for scores, percentiles, tables)
- **Regional font:** Noto Sans 400/500/700 (CJK + multilingual)
- **Tagline:** See risk clearly.
- **Personality:** expert . precise . trustworthy . clear
- **Tone:** Trusted risk expert — calm, precise, evidence-led
- **Never:** "revolutionary", "magic", "game-changer", "supercharges", "black-box", "next-gen AI"

## Before You Generate

1. **Confirm this is IRIS** — not the Gogolook parent brand, not Whoscall, not ScamAdviser, not Watchmen, not any other sub-brand.
2. **Identify the output type** — product UI, marketing/sales, documentation/API, or data visualization. Voice and emphasis shift by surface.
3. **Check the brand essence** — IRIS is about *clarity*. The iris of an eye: perception, focus, bringing risk into focus. "Space = clarity" is the core design principle.
4. **Remember the audience** — risk, fraud, and credit teams at banks, BNPL, leasing, and fintech companies. They distrust hype. Lead with evidence.
5. **Co-branding** — in sales/partner contexts, co-brand with the Gogolook corporate logo ("Gogolook IRIS"). Never merge the IRIS visual identity into the Gogolook parent palette.

## Core Rules

### Color

- **Azure `#41A9F6`** is the primary. It leads every composition — primary actions, links, active states, key brand accents.
- **Critical rule:** White text/icons on Azure fills.
- **Gogolook Blue `#0058EA`** is the secondary — secondary highlights, data-viz accent, icons. White text on Gogolook Blue passes WCAG AA.
- **Blue Iris `#5A5B9F`** is the accent — muted surfaces, supporting accents, subtle differentiation. White text passes AA (~6:1). This color ties to the IRIS name.
- **Iris Sky `#7EDFFE`** is the light accent — tints, hover fills, chart-light, glows on dark backgrounds. Fill-only, never for text.
- **Iris Navy `#0F2647`** is the ink — headings, sidebar, dark surfaces.
- **Iris Mist `#F3F8FE`** is the lightest surface — app background, cards.
- **Brand gradient** (`#0058EA -> #41A9F6 -> #7EDFFE`) is for hero sections and marketing only. Never in product UI.
- **Semantic risk colors** (High `#E5484D`, Medium `#F5A623`, Low `#2FB87A`) are for data visualization only. Never use red/amber/green as brand or decorative color.
- WCAG AA compliance: `#0058EA`, `#5A5B9F`, and `#0F2647` pass on white for text. Azure (`#41A9F6`) uses white text/icons on its fills.

### Typography

- **Headlines:** Plus Jakarta Sans, weight 700 or 800, tracking -0.02em. Favor light weights (300-500) for logotype and highlighted paragraphs to maintain the airy, clear feel.
- **Body:** Inter 400 or 500, line-height 1.5-1.6.
- **Numbers/data:** Inter with `font-variant-numeric: tabular-nums` for all scores, percentiles, table figures, and financial data. This is non-negotiable — the product is score- and figure-heavy.
- **Regional:** Noto Sans 400/500/700 for CJK and multilingual body (TC/JP/KR/TH).
- **Do not** introduce other typefaces. No serif, decorative, or condensed faces.
- **Space = clarity:** generous whitespace, wide-tracked headlines, light type weights. The layout itself should *feel* like seeing clearly. Never crowd.

### Logo

- IRIS is a **logotype-only** brand. No pictorial symbol. The name does the work.
- Official SVG files: `assets/IRIS_logo_Dark_RGB.svg` (navy fill) and `assets/IRIS_logo_White_RGB.svg` (white fill). viewBox: `0 0 1088.38 409.56`.
- **Navy** logotype on light backgrounds. **White** logotype on dark backgrounds.
- **Gradient fill** (Gogolook Blue -> Azure -> Sky) is permitted for hero/marketing use only.
- **Circle containment** (app mark): logotype centered in a thin-stroke circle — for console top bar, avatar, favicon. Keep stroke thin, letter-spacing tight. Never bold the letters to fill the circle.
- **Clear space:** minimum = cap-height of the letters on all sides.
- **Minimum size:** logotype 64px wide; circle mark 28px.
- **Misuse:** never bold, condense, stretch, add effects/shadows, recolor off-palette, or place the gradient logotype on busy imagery.

### Voice & Tone

IRIS speaks like a **trusted risk expert**: calm, precise, evidence-led.

**Four principles:**
1. **Clarity over complexity** — plain language; explain the signal, not the plumbing. Define a term the first time it appears.
2. **Evidence over assertion** — lead with numbers, lift, and outcomes. Cite the metric (Gini, default rate, percentile), not adjectives.
3. **Confident, never hyped** — no "revolutionary", "magic", "game-changer". State what IRIS does and what it delivers.
4. **Respect the stakes** — these are lending and fraud decisions. Be exact about what a score means and its limits (explainability, scope, market coverage).

**Banned words/phrases:** revolutionary, magic, game-changer, supercharges, next-gen AI, black-box, cutting-edge, disruptive, unprecedented, state-of-the-art, limitless, guaranteed.

**Voice scales by surface:**
- **Product UI:** terse, functional, neutral. Labels, not sentences.
- **Sales/marketing:** outcome-led, still evidence-based. Numbers first, narrative second.
- **Docs/API:** exact, imperative. "Send a POST request..." not "You can send..."

**Do / Don't examples:**
- YES: "IRIS lifted Gini value by 7.4% for thin-file applicants."
- NO: "IRIS supercharges your risk engine with next-gen AI."
- YES: "A high-risk label means the number interacts with known loan-shark numbers."
- NO: "Our black-box model just knows."
- YES: "Recover 4.7% of rejected applicants while holding default rate at 1.3%."
- NO: "Approve more, lose less — guaranteed."

### Layout & Spacing

- **Space = clarity** is a first-class design principle, not decoration. The layout itself is the visual proof of the promise.
- Generous whitespace between sections. Airy section rhythm.
- Light type weights and wide-tracked headlines reinforce the "clarity" feel.
- Never crowd elements. When in doubt, add more space.
- Use multiples of 8px for spacing. Cards use 24px or 32px padding.
- Section gaps: 64-120px between major sections. 32-48px between sub-sections.

## CSS Custom Properties

```css
:root {
  /* Brand */
  --blue: #41A9F6;       /* Primary — Azure */
  --azure: #0058EA;      /* Secondary — Gogolook Blue */
  --iris: #5A5B9F;       /* Accent — Blue Iris */
  --sky: #7EDFFE;        /* Light accent — Iris Sky */

  /* Foundations */
  --navy: #0F2647;       /* Ink, headings, dark surfaces */
  --mist: #F3F8FE;       /* App background, lightest surface */
  --white: #FFFFFF;      /* Content surfaces */
  --ink-2: #5A6577;      /* Secondary text */
  --line: #E6ECF5;       /* Borders, dividers */

  /* Semantic risk (data-viz only) */
  --risk-high: #E5484D;
  --risk-med: #F5A623;
  --risk-low: #2FB87A;

  /* Typography */
  --sans-display: 'Plus Jakarta Sans', sans-serif;
  --sans-body: 'Inter', -apple-system, sans-serif;
  --sans-regional: 'Noto Sans', 'Noto Sans TC', 'Noto Sans JP', sans-serif;
}
```

## Output Patterns

### Marketing Content (landing pages, one-pagers, social)

- Open with the tagline ("See risk clearly.") or a metric-led headline.
- Use the brand gradient for hero backgrounds. Navy text on gradient fills.
- Lead with proof points: +7.4% Gini, 4.7% recovery, 2-3% default rate, 157M-number graph.
- Plus Jakarta Sans 700 for headlines. Inter for supporting body.
- Generous whitespace. Never crowd. The clarity principle is especially visible here.
- Co-brand with the Gogolook logo where appropriate.

### Product UI (console, dashboards, API responses)

- Azure for primary actions (buttons, links, active states). White text/icons on Azure fills.
- Gogolook Blue for secondary highlights and data-viz accent.
- Inter for all text. Tabular-nums for every number.
- Iris Mist `#F3F8FE` for background, white for cards.
- Terse, functional copy. Labels over sentences. Imperative mood.
- Risk colors (red/amber/green) only for risk states — never decorative.
- Circle-contained logotype for the top bar / favicon.

### Documentation & API

- Exact, imperative tone. "Send a POST request" not "You might want to send..."
- Inter body, tabular-nums for all code/data examples.
- Navy headings, Inter 600 for section headers.
- Iris Mist code blocks with navy text.
- Define every term on first use. Explain what a score means and its limits.

### Sales Materials (decks, case studies, partner collateral)

- Outcome-led, evidence-based. Numbers first.
- Brand gradient on cover/hero slides only.
- Plus Jakarta Sans for slide headlines, Inter for body.
- Include the Gogolook co-brand lockup.
- Proof points front and center: Gini lift, recovery rate, default rate reduction.
- Never promise guarantees. State outcomes with context.
- "Confidential & Copyright of Gogolook Co., Ltd." on every page.

### Data Visualization

- Primary data series: Azure `#41A9F6`. Secondary: Gogolook Blue `#0058EA`.
- Supporting series: Blue Iris `#5A5B9F`, then Iris Sky `#7EDFFE`.
- Risk heatmaps/indicators use the semantic risk scale ONLY (High `#E5484D`, Med `#F5A623`, Low `#2FB87A`).
- All figure labels in Inter tabular-nums.
- Chart backgrounds: white or Iris Mist. Never colored backgrounds.
- Axis labels in `#5A6577` (secondary text). Grid lines in `#E6ECF5`.

## Output Checklist

Run before delivering any IRIS asset:

- [ ] Azure `#41A9F6` is present as the primary color for actions/accents.
- [ ] White text/icons on Azure fills.
- [ ] All hex values match the token table exactly.
- [ ] Semantic risk colors (red/amber/green) used only for risk data — never decorative.
- [ ] Headlines use Plus Jakarta Sans 700/800. Body uses Inter.
- [ ] All numbers/scores use Inter with `tabular-nums`.
- [ ] Tone is evidence-led — no hype words, no banned phrases.
- [ ] Logo uses the official SVG with correct variant for the background.
- [ ] Clear space and minimum size rules respected for logo.
- [ ] Layout follows "space = clarity" — generous whitespace, airy rhythm.
- [ ] No Gogolook parent brand voice or other sub-brand palette mixed in.
- [ ] WCAG AA contrast met — white text/icons on Azure fills.

## Review Loop

After generating any IRIS-branded output, run the brand compliance review defined in [checklist.md](checklist.md). Iterate and fix violations — up to **10 passes** — until the checklist returns **PASS**. If it does not pass after 10 iterations, flag the remaining violations to the user.

## Out of Scope — Escalate to Humans

- Brand strategy and positioning shifts.
- New brand identity or sub-brand creation.
- Cross-brand campaigns mixing IRIS with Gogolook/Whoscall/ScamAdviser visual systems.
- Changes to the logo design itself (coordinate with Konno / design team).
- Final approval on any public-facing output.
- All IRIS material is **Confidential & Copyright of Gogolook Co., Ltd.**

## Install

To install the IRIS brand skill globally:

```bash
# From the IRIS brand guideline repo root:
mkdir -p ~/.claude/skills/iris-brand
cp skills/iris-brand/SKILL.md ~/.claude/skills/iris-brand/SKILL.md
cp skills/iris-brand/checklist.md ~/.claude/skills/iris-brand/checklist.md
```

Then add to your `.claude/settings.json` or project settings:

```json
{
  "skills": ["iris-brand"]
}
```

Invoke with `/iris-brand` before generating any IRIS-branded content.
