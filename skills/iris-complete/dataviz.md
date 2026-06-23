# IRIS Data Visualization Patterns

Rules and patterns for charts, KPIs, and risk visualizations in any IRIS surface.

---

## 1. Risk Color Scale

Used **only** to represent risk semantics. Never as brand decoration.

| Level | Hex | Meaning | When to use |
|-------|-----|---------|-------------|
| High risk | `#E5484D` | High-risk factor, reject, alert | Risk score E, flagged accounts, reject decisions |
| Medium risk | `#F5A623` | Caution, manual review | Risk score C-D, borderline cases, review queue |
| Low risk | `#2FB87A` | Low risk, approved, safe | Risk score A-B, approved applicants, clean signals |

**Rules:**
- Never use red, amber, or green as brand or decorative color.
- Always pair risk color with a text label or icon — color must not be the sole
  indicator (WCAG, colorblind accessibility).
- In the A-E risk scale, map: A = `#2FB87A` (green), B = `#8FBE52` (olive), C = `#F5A623` (amber), D = `#EE6A45` (orange), E = `#E5484D` (red).

---

## 2. Chart Brand Palette

For non-risk data (feature distributions, trend comparisons, category breakdowns),
use the brand palette in this priority order:

| Priority | Color | Hex | Token |
|----------|-------|-----|-------|
| 1st | Azure | `#41A9F6` | `--blue` |
| 2nd | Gogolook Blue | `#0058EA` | `--azure` |
| 3rd | Blue Iris | `#5A5B9F` | `--iris` |
| 4th | Iris Sky | `#7EDFFE` | `--sky` |
| 5th | Iris Navy | `#0F2647` | `--navy` |

For charts that mix brand data and risk data, use the brand palette for
non-risk series and the risk scale for risk series. Never mix the two systems
within a single series.

---

## 3. KPI Card Pattern

For displaying key performance indicators (Gini uplift, default rate, recovery
rate, screening volume).

```
+---------------------------------------+
|  +7.4%              ▲ 1.2% vs Q3      |
|  Gini uplift                           |
|  ▁▂▃▅▆▇█▆▅▃▅▇  (sparkline)           |
+---------------------------------------+
```

**Structure:**
- **Value:** Plus Jakarta Sans 500, 28-36px, Iris Navy (light bg) or white (dark bg).
  Use `font-variant-numeric: tabular-nums`.
- **Trend badge:** Small pill — green background + white text for positive,
  red background + white text for negative. Arrow icon (up/down) inside.
  Use risk green (`#2FB87A`) / risk red (`#E5484D`).
- **Label:** Inter 400, 12-13px, `#5A6577` (light bg) or `rgba(255,255,255,0.6)` (dark bg).
- **Sparkline:** 64-80px wide, 20-24px tall. Stroke: Azure (`#41A9F6`), 1.5px,
  no fill (or very light Azure fill at 0.08 opacity). Plotted as an SVG polyline.

**Card container:**
- Light bg: white, 1px `#E6ECF5` border, 16px radius, 24-28px padding.
- Dark bg (navy): `rgba(255,255,255,0.06)`, no border, 16px radius, 24px padding.

---

## 4. Donut / Ring Charts

Used for risk distribution and percentage breakdowns.

### Risk Distribution Donut

The primary risk visualization. Shows the distribution of risk levels.

- **Size:** 200-400px diameter
- **Ring width:** 28-36px (stroke-width on SVG circle, stroke-linecap: round)
- **Gap:** 4-6px visual gap between segments (use stroke-dashoffset)
- **Center:** Alert/shield icon (24px, white or navy) above a label
  ("High-risk factors" / "Risk Distribution")
- **Segments:** Ordered clockwise from top: High (red), Medium (amber),
  Low (green), plus any brand-color segments for non-risk categories
- **Legend:** Beside the donut (not overlapping). Each legend row: color dot
  (8px circle) + label + count/percentage.

### Mini Donut Metrics

Compact percentage indicators for key figures.

```
[ (donut) 70%  Risky applicants screened ]
[ (donut) 7.4% Gini uplift              ]
[ (donut) 4.7% Applicants recovered     ]
```

- **Size:** 56-64px diameter
- **Ring:** Azure fill for the value arc, `#E6ECF5` (line color) for the
  remaining arc. Stroke-width 6-8px, round linecap.
- **Value:** Inside or beside the donut — Plus Jakarta Sans 500, 20-22px,
  Iris Navy, tabular-nums.
- **Label:** Below or beside — Inter 400, 12-13px, `#5A6577`.
- **Container:** White card, border, 16px radius (same as KPI card pattern).

---

## 5. Bar Charts

### Horizontal Bar Chart (Risk Levels)

For showing risk level distribution (A-E counts or percentages).

- **Bars:** Horizontal, 12-16px height, 12-14px gap between bars.
- **Colors:** A-E mapped to the risk scale (see Section 1).
- **Labels:** Level letter left of bar (Inter 500, 13px, navy/white).
  Value right of bar or inside if bar is wide enough.
- **Background track:** Light gray (`#E6ECF5` at 0.5 opacity) behind each bar
  to show the full scale.
- **Sort:** Always A (top) to E (bottom) — lowest to highest risk.

### Vertical Bar Chart

For time-series comparisons or category counts.

- **Bars:** 24-40px wide, 8-12px gap.
- **Colors:** Brand palette (Azure primary, Gogolook Blue secondary).
- **X-axis:** Inter 400, 11px, `#5A6577`. Category or date labels.
- **Y-axis:** Inter 400, 11px, `#5A6577`. Numeric scale, tabular-nums.
- **Grid lines:** Horizontal only, `#E6ECF5`, 1px, dashed or solid.

---

## 6. Line Charts

For trend data — risk scores over time, model performance, screening volume.

- **Lines:** 2px stroke, round linecap/linejoin. Primary line: Azure. Secondary
  line: Gogolook Blue. Tertiary: Blue Iris.
- **Area fill:** Optional — Azure at 0.06-0.10 opacity below the line.
- **Dots:** 4-6px circles at data points. Fill matches line color. Show on
  hover or always if fewer than 12 points.
- **Grid:** Horizontal lines only, `#E6ECF5`, 1px.
- **Axes:** Inter 400, 11px, `#5A6577`, tabular-nums on Y-axis.
- **Tooltip:** White card with 1px border, 8px radius, small shadow. Shows
  exact value + date. Plus Jakarta Sans 600 for value, Inter 400 for label.

---

## 7. Accessibility

Data visualization accessibility is non-negotiable for a risk product.

- **Never use color as the sole indicator.** Every colored element must be paired
  with a text label, icon, or pattern.
- **Risk levels** always show the letter (A-E) or word (High/Med/Low) alongside
  the color.
- **Contrast:** Chart labels must meet WCAG AA (4.5:1 for text, 3:1 for large
  text and UI components).
- **Tabular-nums:** All numeric values in charts use `font-variant-numeric:
  tabular-nums` so digits align in columns and are easy to compare.
- **Screen reader:** Provide `aria-label` on chart containers with a text
  summary of the data. SVG charts should include `<title>` and `<desc>` elements.
- **Reduced motion:** Respect `prefers-reduced-motion`. Skip chart entry
  animations when the user prefers reduced motion.
- **Focus indicators:** Interactive chart elements (tooltips, filters) must have
  visible focus states (Azure ring: `box-shadow: 0 0 0 3px rgba(65,169,246,.18)`).

---

## 8. Dark vs. Light Context

| Property | Light (mist/white bg) | Dark (navy bg) |
|----------|-----------------------|----------------|
| Card bg | White, 1px `#E6ECF5` border | `rgba(255,255,255,0.06)`, no border |
| Value text | Iris Navy `#0F2647` | White `#FFFFFF` |
| Label text | `#5A6577` | `rgba(255,255,255,0.6)` |
| Grid lines | `#E6ECF5` | `rgba(255,255,255,0.08)` |
| Sparkline stroke | Azure `#41A9F6` | Azure `#41A9F6` (same) |
| Donut track | `#E6ECF5` | `rgba(255,255,255,0.10)` |

Charts on dark backgrounds (navy) are used in presentation data slides and
console dark panels. Charts on light backgrounds are used in content slides,
console main area, and landing pages.
