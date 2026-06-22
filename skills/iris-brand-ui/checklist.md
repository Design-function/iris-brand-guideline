# IRIS Brand + UI Compliance Checklist

Use this checklist to review any IRIS-branded UI output. Covers both brand identity
and UI component compliance. Mark each item PASS, FAIL, or N/A.

---

## 1. Color (8 checks)

| # | Check | Result |
|---|-------|--------|
| 1.1 | Azure `#41A9F6` is present as the primary color (actions, links, active states). | |
| 1.2 | White text/icons on Azure (`#41A9F6`) fills. | |
| 1.3 | Gogolook Blue `#0058EA` used as secondary only — not replacing Azure as primary. | |
| 1.4 | Blue Iris `#5A5B9F` used as accent only — muted surfaces, supporting accents. | |
| 1.5 | Iris Sky `#7EDFFE` is fill-only — never used for text. | |
| 1.6 | All hex values match token table. No off-palette colors. | |
| 1.7 | Brand gradient only in hero/marketing — never in product UI. | |
| 1.8 | Semantic risk colors only for risk data — never as decoration. | |

**Critical failures:** 1.2, 1.8.

---

## 2. Typography (6 checks)

| # | Check | Result |
|---|-------|--------|
| 2.1 | Headlines use Plus Jakarta Sans 300, tracking -0.02em. | |
| 2.2 | Body uses Inter 400/500, line-height 1.5–1.6. | |
| 2.3 | All numbers/scores/percentiles use Inter `tabular-nums`. | |
| 2.4 | No unauthorized typefaces. | |
| 2.5 | Font weights within defined ranges. | |
| 2.6 | CJK/regional text uses Noto Sans. | |

**Critical failures:** 2.4.

---

## 3. Logo (5 checks)

| # | Check | Result |
|---|-------|--------|
| 3.1 | Uses official SVG source — not recreation. | |
| 3.2 | Correct variant for background (navy on light, white on dark). | |
| 3.3 | Clear space and minimum size respected. | |
| 3.4 | No misuse (bold, stretch, shadow, recolor). | |
| 3.5 | Gradient logotype only in hero/marketing. | |

**Critical failures:** 3.1, 3.4.

---

## 4. UI Components (10 checks)

| # | Check | Result |
|---|-------|--------|
| 4.1 | Primary button: Azure fill, **white text/icons**. | |
| 4.2 | Secondary/outline button: Gogolook Blue border/text on white. | |
| 4.3 | Button sizes match spec: sm (8px 14px), default (11px 20px), lg (14px 26px). | |
| 4.4 | Form inputs: 1px `--line` border, `--r-md` radius, Azure focus ring. | |
| 4.5 | Badges use correct variants: brand (blue/azure/iris) vs risk (high/med/low). | |
| 4.6 | Risk level scale A-E uses correct 5-stop color ramp. | |
| 4.7 | Data tables: Iris Mist header bg, border-bottom rows, tabular-nums. | |
| 4.8 | Console shell: navy sidebar, white main area. | |
| 4.9 | KPI cards: value + label + trend badge + sparkline. | |
| 4.10 | Icons: stroke-based, 1.6px, round linecap/linejoin, 24x24. | |

**Critical failures:** 4.1.

---

## 5. Layout & Spacing (5 checks)

| # | Check | Result |
|---|-------|--------|
| 5.1 | Space = clarity: generous whitespace, airy rhythm, nothing crowded. | |
| 5.2 | Spacing uses 4px base scale (tokens from tokens.json). | |
| 5.3 | Cards use 24–32px padding, `--r-lg` or `--r-xl` radius. | |
| 5.4 | Content hierarchy clear: headings, body, data are distinct layers. | |
| 5.5 | Responsive: components adapt below 760px. | |

---

## 6. Accessibility (5 checks)

| # | Check | Result |
|---|-------|--------|
| 6.1 | WCAG AA contrast on all text elements. | |
| 6.2 | Azure `#41A9F6` never used as text color on white. | |
| 6.3 | Focus states visible: Azure ring (`box-shadow: 0 0 0 3px rgba(65,169,246,.18)`). | |
| 6.4 | Color not sole indicator — labels/icons supplement color coding. | |
| 6.5 | `prefers-reduced-motion` honored for animations. | |

**Critical failures:** 6.2.

---

## 7. Tone & Copy (4 checks)

| # | Check | Result |
|---|-------|--------|
| 7.1 | Tone matches surface: UI = terse/functional, sales = outcome-led. | |
| 7.2 | No banned words (revolutionary, magic, game-changer, etc.). | |
| 7.3 | Evidence-led claims — metrics, not adjectives. | |
| 7.4 | "WitcherFin" does not appear anywhere. | |

**Critical failures:** 7.2, 7.4.

---

## Scoring

**Total checks:** 43

- **APPROVED:** All PASS or N/A. Zero FAIL.
- **REVISE:** Any FAIL present.
- **BLOCKED:** Any critical failure present.

## Review Verdict

```
BRAND + UI REVIEW VERDICT
Brand:      IRIS
Output type: [UI / dashboard / console / landing / component]
Reviewer:   iris-brand-ui skill
Iteration:  [n/10]

Total:      43 checks
Passed:     ___
Failed:     ___
N/A:        ___
Critical:   [0 / list]

RESULT:     PASS / REVISE / BLOCKED
```

Run up to 10 iterations. Each must show progress. If iteration 10 does not PASS,
report remaining failures with remediation guidance.
