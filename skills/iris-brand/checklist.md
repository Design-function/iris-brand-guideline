# IRIS Brand Compliance Checklist

Use this checklist to review any IRIS-branded output. Walk through every item.
Mark each as PASS, FAIL, or N/A. A single critical failure blocks approval.

---

## 1. Color (10 checks)

| # | Check | Result |
|---|-------|--------|
| 1.1 | Azure `#41A9F6` is present as the primary brand color (actions, links, active states, key accents). | |
| 1.2 | Navy text (`#0F2647`) is used on Azure fills — **never** white text on Azure. | |
| 1.3 | Gogolook Blue `#0058EA` is used only as secondary (highlights, data-viz, icons) — not replacing Azure as primary. | |
| 1.4 | Blue Iris `#5A5B9F` is used only as accent (muted surfaces, supporting accents) — not as primary or secondary. | |
| 1.5 | Iris Sky `#7EDFFE` is fill-only — never used for text. | |
| 1.6 | All hex values match the token table exactly. No approximations, no off-palette colors introduced. | |
| 1.7 | Brand gradient (`#0058EA -> #41A9F6 -> #7EDFFE`) appears only in hero/marketing contexts — never in product UI. | |
| 1.8 | Semantic risk colors (High `#E5484D`, Med `#F5A623`, Low `#2FB87A`) are used only for risk data — **never** as brand decoration, status badges unrelated to risk, or accent color. | |
| 1.9 | Red and amber never appear as brand or decorative color anywhere in the output. | |
| 1.10 | Foundation colors are correct: Navy `#0F2647`, Mist `#F3F8FE`, White `#FFFFFF`, secondary text `#5A6577`, borders `#E6ECF5`. | |

**Critical failures:** 1.2 (white text on Azure), 1.8 (risk colors as decoration), 1.9 (red/amber as brand color).

---

## 2. Typography (8 checks)

| # | Check | Result |
|---|-------|--------|
| 2.1 | Headlines use **Plus Jakarta Sans** weight 700 or 800 with tracking -0.02em. | |
| 2.2 | Body copy uses **Inter** weight 400 or 500 with line-height 1.5-1.6. | |
| 2.3 | All numbers, scores, percentiles, and table figures use Inter with `font-variant-numeric: tabular-nums`. | |
| 2.4 | Regional/CJK text uses **Noto Sans** (400/500/700) — not a different CJK face. | |
| 2.5 | No unauthorized typefaces introduced (no serif, decorative, condensed, or monospace for body). | |
| 2.6 | Light type weights (300-500) are used for logotype rendering and highlighted paragraphs to maintain the airy feel. | |
| 2.7 | Font weights are within the defined ranges — Plus Jakarta Sans 300-800, Inter 400/500/600, Noto Sans 400/500/700. | |
| 2.8 | Numeric data in tables and charts is visually aligned (tabular figures, not proportional). | |

**Critical failures:** 2.5 (unauthorized typefaces).

---

## 3. Logo (7 checks)

| # | Check | Result |
|---|-------|--------|
| 3.1 | Logo uses the official SVG source (`IRIS_logo_Dark_RGB.svg` or `IRIS_logo_White_RGB.svg`) — not a recreation or approximation. | |
| 3.2 | Correct variant selected: navy logotype on light backgrounds, white logotype on dark backgrounds. | |
| 3.3 | Gradient fill logotype appears only in hero/marketing contexts — not in product UI or documents. | |
| 3.4 | Clear space maintained: minimum cap-height of the letters on all four sides. | |
| 3.5 | Minimum size respected: logotype >= 64px wide, circle mark >= 28px. | |
| 3.6 | No misuse: logo is not bolded, condensed, stretched, shadowed, outlined, or recolored off-palette. | |
| 3.7 | Circle containment mark (if used) has a thin stroke and tight letter-spacing — letters are not bolded to fill. | |

**Critical failures:** 3.1 (unofficial logo), 3.6 (logo misuse).

---

## 4. Tone & Copy (10 checks)

| # | Check | Result |
|---|-------|--------|
| 4.1 | Tone matches the output surface: product UI = terse/functional, sales = outcome-led/evidence-based, docs = exact/imperative. | |
| 4.2 | Claims are backed by specific evidence (Gini lift, default rate, percentile, recovery rate) — not bare adjectives. | |
| 4.3 | No banned words: "revolutionary", "magic", "game-changer", "supercharges", "next-gen AI", "black-box", "cutting-edge", "disruptive", "unprecedented", "state-of-the-art", "limitless", "guaranteed". | |
| 4.4 | Technical terms are defined on first use. Jargon is not assumed. | |
| 4.5 | Score meanings and model limitations are stated explicitly where relevant — no vague implications of certainty. | |
| 4.6 | The tagline "See risk clearly." is used correctly (not modified, not paraphrased as a different claim). | |
| 4.7 | IRIS is referred to by name (not "the platform", "our solution", or "the product" without prior IRIS mention). | |
| 4.8 | "WitcherFin" does not appear anywhere. The rebrand is complete. | |
| 4.9 | Copyright notice present where required: "Confidential & Copyright of Gogolook Co., Ltd." | |
| 4.10 | Gogolook co-brand is included in sales/partner contexts ("Gogolook IRIS") but not in product UI. | |

**Critical failures:** 4.3 (banned words), 4.8 (WitcherFin reference).

---

## 5. Layout & Spacing (6 checks)

| # | Check | Result |
|---|-------|--------|
| 5.1 | "Space = clarity" principle is evident: generous whitespace, airy section rhythm, nothing feels crowded. | |
| 5.2 | Section gaps are 64-120px between major sections, 32-48px between sub-sections. | |
| 5.3 | Spacing uses multiples of 8px. Cards use 24px or 32px padding. | |
| 5.4 | Headlines use wide tracking and light weights where appropriate — reinforcing the clarity feel. | |
| 5.5 | Content hierarchy is clear: headings, body, and data are visually distinct layers. | |
| 5.6 | No dense walls of text. Information is broken into digestible segments with breathing room. | |

**Critical failures:** None (but consistent 5.1 failure indicates a fundamental brand misunderstanding).

---

## 6. Data Visualization (6 checks)

| # | Check | Result |
|---|-------|--------|
| 6.1 | Primary data series uses Azure `#41A9F6`. Secondary uses Gogolook Blue `#0058EA`. | |
| 6.2 | Supporting series follow the palette order: Blue Iris `#5A5B9F`, then Iris Sky `#7EDFFE`. | |
| 6.3 | Risk indicators/heatmaps use only the semantic risk scale (High `#E5484D`, Med `#F5A623`, Low `#2FB87A`). | |
| 6.4 | All figure labels use Inter tabular-nums. | |
| 6.5 | Chart backgrounds are white (`#FFFFFF`) or Iris Mist (`#F3F8FE`) — never colored. | |
| 6.6 | Axis labels use secondary text color (`#5A6577`). Grid lines use border color (`#E6ECF5`). | |

**Critical failures:** 6.3 (risk colors misused).

---

## 7. Accessibility (6 checks)

| # | Check | Result |
|---|-------|--------|
| 7.1 | WCAG AA contrast ratio met for all text on its background. | |
| 7.2 | Azure `#41A9F6` is never used as a text color on white — it fails AA contrast for text. | |
| 7.3 | Gogolook Blue `#0058EA` and Blue Iris `#5A5B9F` pass AA on white for text — confirmed if used as text. | |
| 7.4 | Iris Navy `#0F2647` is used for primary text on light backgrounds (passes AAA). | |
| 7.5 | Interactive elements have visible focus states. | |
| 7.6 | Color is not the sole indicator of meaning — icons, labels, or patterns supplement color coding. | |

**Critical failures:** 7.2 (Azure as text color on white).

---

## 8. Brand Integrity (4 checks)

| # | Check | Result |
|---|-------|--------|
| 8.1 | No Gogolook parent brand voice, tone, or messaging pattern mixed into IRIS output (IRIS has its own identity). | |
| 8.2 | No other sub-brand palette (Whoscall green, ScamAdviser red, Watchmen colors) appears in the output. | |
| 8.3 | The output is clearly identifiable as IRIS — Azure-led, cool blue palette, expert/precise tone. | |
| 8.4 | If co-branded with Gogolook, the IRIS identity leads and the Gogolook logo is secondary/supporting. | |

**Critical failures:** 8.2 (other sub-brand palette mixed in).

---

## Scoring

**Total checks:** 57

Count results:
- **PASS:** ___
- **FAIL:** ___
- **N/A:** ___

**Pass rate:** ___ / (total - N/A) = ___%

### Approval Criteria

- **APPROVED:** All checks are PASS or N/A. Zero FAIL.
- **REVISE:** Any FAIL present. Must fix and re-review.
- **BLOCKED:** Any critical failure present. Must fix critical items before re-review.

### Critical Failures Summary

List any critical failures here:

| Check | Issue | Required Fix |
|-------|-------|-------------|
| | | |

---

## Brand Review Verdict

```
BRAND REVIEW VERDICT
Brand:      IRIS
Output type: [UI / copy / visual / deck / code / data-viz]
Reviewer:   iris-brand skill
Iteration:  [n/10]

Total:      57 checks
Passed:     ___
Failed:     ___
N/A:        ___
Critical:   [0 / list]

RESULT:     PASS / REVISE / BLOCKED
```

### Review Loop Protocol

1. Run this checklist against the generated output.
2. If the result is **REVISE** or **BLOCKED**, fix all FAIL items (critical items first).
3. Re-run the checklist. This is iteration n+1.
4. Repeat until **PASS** or until iteration 10.
5. If iteration 10 is reached without PASS, report the remaining failures to the user with specific remediation guidance.

**Maximum iterations:** 10. Each iteration must show measurable progress (fewer failures than the previous pass). If an iteration introduces new failures, halt and report to the user.
