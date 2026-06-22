# IRIS Complete — Comprehensive QA Checklist

The all-domains checklist for the iris-complete bundle. Covers brand, UI, presentation,
and data visualization. Run after generating any IRIS output.

---

## 1. Brand Compliance (9 checks)

| # | Check | Result |
|---|-------|--------|
| 1.1 | Azure `#41A9F6` present as primary. White text/icons on Azure fills. | |
| 1.2 | All hex values match token table. No off-palette colors. | |
| 1.3 | Semantic risk colors only in data-viz — never decorative. | |
| 1.4 | Brand gradient only in hero/marketing surfaces. | |
| 1.5 | Plus Jakarta Sans for headlines, Inter for body. No other faces. | |
| 1.6 | Tabular-nums on all scores, percentiles, table figures. | |
| 1.7 | Tone is evidence-led, precise — no hype words. | |
| 1.8 | Logo uses official SVG, correct variant, proper clearspace. | |
| 1.9 | "WitcherFin" does not appear. Rebrand complete. | |

**Critical failures:** 1.1 (Azure text color rule), 1.3, 1.9.

---

## 2. UI Compliance (8 checks)

| # | Check | Result |
|---|-------|--------|
| 2.1 | Primary button: Azure fill, white text/icons. | |
| 2.2 | Components match iris-brand-ui specs (sizes, radii, padding). | |
| 2.3 | Space = clarity: generous whitespace, airy rhythm. | |
| 2.4 | Focus states use Azure ring. | |
| 2.5 | Console shell: navy sidebar, white main area. | |
| 2.6 | Icons: stroke-based, 1.6px, round caps/joins. | |
| 2.7 | WCAG AA contrast on all text. | |
| 2.8 | Responsive below 760px. | |

**Critical failures:** 2.1, 2.7.

---

## 3. Presentation Compliance (7 checks)

| # | Check | Result |
|---|-------|--------|
| 3.1 | Slide backgrounds follow type rules (navy for cover/section, mist for content). | |
| 3.2 | Footer on every content slide: IRIS wordmark + "Confidential & Copyright of Gogolook Co., Ltd." | |
| 3.3 | Max one decorative element per slide. | |
| 3.4 | Cover slide has IRIS logotype, tagline, title, date, presenter. | |
| 3.5 | Data slides use semantic risk colors only for risk data. | |
| 3.6 | Slide navigation works (arrow keys, click). | |
| 3.7 | Works as file:// without a server. | |

**Critical failures:** 3.2.

---

## 4. Data Visualization Compliance (6 checks)

| # | Check | Result |
|---|-------|--------|
| 4.1 | Chart brand palette order: Azure, Gogolook Blue, Blue Iris, Sky, Navy. | |
| 4.2 | Risk colors only for risk semantics — not decorative. | |
| 4.3 | A-E risk scale uses correct 5-stop ramp (#2FB87A → #8FBE52 → #F5A623 → #EE6A45 → #E5484D). | |
| 4.4 | Color never sole indicator — always paired with labels/icons. | |
| 4.5 | Tabular-nums on all chart/KPI numeric values. | |
| 4.6 | Chart labels readable at target size. | |

**Critical failures:** 4.2.

---

## 5. Accessibility (4 checks)

| # | Check | Result |
|---|-------|--------|
| 5.1 | WCAG AA contrast on all text. Azure never as text color on white. | |
| 5.2 | Focus states visible on all interactive elements. | |
| 5.3 | `prefers-reduced-motion` honored. | |
| 5.4 | Color supplemented with labels, icons, or patterns. | |

**Critical failures:** 5.1.

---

## Scoring

**Total checks:** 34

- **APPROVED:** All PASS or N/A. Zero FAIL.
- **REVISE:** Any FAIL present.
- **BLOCKED:** Any critical failure present.

Mark N/A for sections not applicable (e.g., skip Presentation checks for a dashboard).

## Review Verdict

```
IRIS COMPLETE REVIEW VERDICT
Brand:      IRIS
Output type: [UI / deck / dashboard / landing / data-viz / mixed]
Reviewer:   iris-complete skill
Iteration:  [n/10]

Total:      34 checks (minus N/A)
Passed:     ___
Failed:     ___
N/A:        ___
Critical:   [0 / list]

RESULT:     PASS / REVISE / BLOCKED
```

Run up to 10 iterations. Each must show measurable progress. Halt if a new iteration
introduces more failures than it fixes.
