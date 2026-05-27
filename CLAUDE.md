# IRIS — Brand Guideline (Project Instructions)

> The single source of truth for the IRIS brand. Any content, UI, deck, or asset
> produced for IRIS must follow this file. The visual companion is
> `iris-brand-guideline.html` (open in a browser).

## Global Memory

Read ~/.claude/CLAUDE.md for memory rules and topic files.

---

## 1. What IRIS Is

**IRIS** — *Intelligence Risk Integrated Solutions*.

A Gogolook **B2B** product. IRIS sits on the **financial-flow** side of the scam
journey (sibling to *Watchmen Reputation Protection* and *Anti-Scam Intelligence*).
It helps financial institutions **detect high-risk accounts, assess risk levels,
and optimize existing risk processes** using 3,000+ phone-intelligence features
drawn from a 157M-number behavioral graph.

- **Buyers / users:** risk, fraud, and credit teams at **banks, BNPL, leasing, and
  fintech** companies. Primary markets: Taiwan, Thailand, wider SEA.
- **Two core use cases:** **Mule Account Detection** and **Credit Risk Assessment**
  (account opening + loan application).
- **Delivery:** scoring API, risk-level binning (A–E), single-feature percentiles;
  expert-built, high-explainability models hosted and monitored by Gogolook.
- **Proof points:** ~70% of risky applicants screened, **+7.4% Gini** uplift,
  **4.7%** of rejected applicants safely recovered, default rate cut to 2–3%.

IRIS is the rebrand of the product formerly called **WitcherFin**. Replace all
"WitcherFin" naming and its purple/magenta accent with IRIS naming and the palette
below.

---

## 2. Brand Essence

- **Idea:** *the iris of an eye* — perception, focus, clarity. IRIS brings risk
  into focus.
- **Tagline:** **See risk clearly.**
- **Positioning:** the expert risk lens for financial institutions — turning
  thousands of behavioral signals into clear, explainable decisions.
- **Personality:** expert · precise · trustworthy · clear.

### Mission
> Help financial institutions see and stop fraud and credit risk before it costs
> them — by turning 3,000+ behavioral signals into clear, explainable risk
> decisions they can act on with confidence.

---

## 3. Tone of Voice

IRIS speaks like a **trusted risk expert**: calm, precise, evidence-led. We sell to
analysts and risk officers who distrust hype.

**Four principles**
1. **Clarity over complexity** — plain language; explain the signal, not the
   plumbing. Define a term the first time it appears.
2. **Evidence over assertion** — lead with numbers, lift, and outcomes. Cite the
   metric (Gini, default rate, percentile), not adjectives.
3. **Confident, never hyped** — no "revolutionary", "magic", "game-changer".
   State what IRIS does and what it delivers.
4. **Respect the stakes** — these are lending and fraud decisions. Be exact about
   what a score means and its limits (explainability, scope, market coverage).

**Do / Don't**
- ✅ "IRIS lifted Gini value by 7.4% for thin-file applicants."
  ❌ "IRIS supercharges your risk engine with next-gen AI."
- ✅ "A high-risk label means the number interacts with known loan-shark numbers."
  ❌ "Our black-box model just knows."
- ✅ "Recover 4.7% of rejected applicants while holding default rate at 1.3%."
  ❌ "Approve more, lose less — guaranteed."

Voice scales by surface: **product UI** = terse, functional, neutral. **Sales /
marketing** = outcome-led, still evidence-based. **Docs / API** = exact, imperative.

---

## 4. Color

Sampled from the Gogolook palette. IRIS is a **cool, blue-led** brand. Warm tones
appear **only** as semantic risk signals in data, never as brand decoration.

### Brand
| Token | Hex | Use |
|-------|-----|-----|
| `--iris-blue` (Primary) | `#0058EA` | Primary actions, links, brand blue, key accents |
| `--iris-navy` (Dark) | `#0F2647` | Dark surfaces, console sidebar, headings on light |
| `--iris-teal` (Intelligence accent) | `#01D3B8` | Data/insight highlights, charts, secondary accent |
| `--iris-green` (Positive) | `#30FF85` | Success, "recovered" / approved states — use sparingly |

### Neutrals
| Token | Hex | Use |
|-------|-----|-----|
| `--ink` | `#0F2647` | Primary text |
| `--ink-2` | `#48566B` | Secondary text |
| `--line` | `#E3E8F0` | Borders, dividers |
| `--surface` | `#F5F8FC` | App background, cards |
| `--white` | `#FFFFFF` | Cards, content surfaces |

### Semantic risk scale (data viz only)
| Level | Hex | Meaning |
|-------|-----|---------|
| High risk | `#E5484D` | High-risk factor / reject |
| Medium risk | `#F5A623` | Caution / manual review |
| Low risk | `#30FF85` / `#01D3B8` | Low risk / approved |

Rules: never use red/amber as brand or decorative color — reserve for risk
semantics. Maintain WCAG AA: `#0058EA` and `#0F2647` pass on white for text.

---

## 5. Typography

| Role | Font | Weights | Use |
|------|------|---------|-----|
| Primary | **Plus Jakarta Sans** | 800 / 700 / 600 | Headlines and highlighted paragraphs only. Carries brand personality. |
| Secondary | **Inter** | 400 / 500 / 600 | Body copy across digital and print. Use `font-variant-numeric: tabular-nums` for all scores, percentiles, and table figures. |
| Regional | **Noto Sans** | 400 / 500 / 700 | CJK + multilingual body (TC/JP/KR/TH). Ensures regional readability. |

- Headlines: Plus Jakarta Sans, tight tracking (-0.02em), weight 800/700.
- Body: Inter 400/500, 1.5–1.6 line-height.
- Numbers/data: Inter tabular-nums (the product is score- and figure-heavy).
- Do not introduce other typefaces.

---

## 6. Logo

IRIS is a **logotype-only** brand — no pictorial symbol. The name does the work.

- **Logotype:** `IRIS` set in **Plus Jakarta Sans, light weight (400–500)** with
  **wide letter-spacing (~0.25em)**. The thin, airy treatment reads precise,
  modern, and timeless — a lens of clarity, not a heavy badge.
- **Color:** `--iris-navy` on light backgrounds; white on dark; a single
  blue→teal gradient fill is permitted for hero/marketing use only.
- **Circle containment (app mark):** the logotype centered inside a thin-stroke
  circle — used where a compact, contained mark is needed (console top bar,
  avatar, favicon). Replaces the old "W" badge. Keep the stroke thin and the
  letter-spacing tight enough to fit; never bold the letters to fill the circle.
- **Clear space:** minimum = the cap-height of the letters on all sides.
- **Min size:** logotype 64px wide; circle mark 28px.
- **Misuse:** don't bold or condense the letters, stretch, add effects/shadows,
  recolor off-palette, or place the gradient logotype on busy imagery.

---

## 7. Relationship to Gogolook

IRIS is part of the Gogolook B2B anti-scam suite. Co-brand with the Gogolook
corporate logo in sales/partner contexts ("Gogolook IRIS"). Inherits the Gogolook
type stack and palette; differentiated by the iris mark and blue/teal identity.

All IRIS material is **Confidential & Copyright of Gogolook Co., Ltd.**

---

## 8. Deliverables in this project

- `CLAUDE.md` — this brand guideline (the IRIS brand skill).
- `iris-brand-guideline.html` — single-page visual guideline (logo, color,
  type, mission, tone). Open in a browser.
- *(planned)* IRIS design system / UI spec — documents the console (app shell,
  sidebar, quota card, data tables, query screens, risk viz) on the IRIS palette.
