# IRIS UI Component System

The IRIS UI system is built for **financial risk intelligence surfaces** — consoles, dashboards, score displays, and data tables where precision, legibility, and trust are paramount. Every component follows the principle: **space = clarity**.

---

## Design Principles

1. **Space = clarity.** Generous whitespace, airy section rhythm, light type weights, wide-tracked headlines. The layout itself should feel like seeing clearly. Never crowd.
2. **Functional and neutral.** Product UI is terse, legible, and score-friendly. No decorative flourish.
3. **Azure drives primary actions.** Gogolook Blue carries secondary/data accents. Blue Iris is the muted supporting accent.
4. **Semantic risk colors are functional only.** Red, amber, and green appear exclusively in risk data — never as brand decoration or UI chrome.
5. **Tabular numbers everywhere.** Scores, percentiles, currency, counts, and table figures all use `font-variant-numeric: tabular-nums`.

---

## CSS Custom Properties

```css
:root {
  /* ---- Brand colors ---- */
  --blue: #41A9F6;          /* Primary — Azure */
  --azure: #0058EA;         /* Secondary — Gogolook Blue */
  --iris: #5A5B9F;          /* Accent — Blue Iris */
  --sky: #7EDFFE;           /* Light accent — Iris Sky */

  /* ---- Foundations ---- */
  --navy: #0F2647;          /* Ink / dark surfaces */
  --mist: #F3F8FE;          /* Surface — lightest background */
  --white: #FFFFFF;         /* Content surface */
  --ink-2: #5A6577;         /* Secondary text */
  --line: #E6ECF5;          /* Borders, dividers */

  /* ---- Semantic (data viz only) ---- */
  --success: #2FB87A;       /* Low risk / positive */
  --risk-high: #E5484D;     /* High risk / reject */
  --risk-med: #F5A623;      /* Medium risk / caution */

  /* ---- Typography ---- */
  --display: "Plus Jakarta Sans", system-ui, sans-serif;
  --body: "Inter", system-ui, sans-serif;
  --regional: "Noto Sans", "Noto Sans TC", system-ui, sans-serif;

  /* ---- Spacing (4px base) ---- */
  --sp-1: 4px;
  --sp-2: 8px;
  --sp-3: 12px;
  --sp-4: 16px;
  --sp-5: 20px;
  --sp-6: 24px;
  --sp-8: 32px;
  --sp-10: 40px;
  --sp-12: 48px;
  --sp-16: 64px;
  --sp-20: 80px;
  --sp-24: 96px;

  /* ---- Radius ---- */
  --r-sm: 8px;
  --r-md: 10px;
  --r-lg: 16px;
  --r-xl: 18px;
  --r-2xl: 20px;
  --r-full: 999px;

  /* ---- Shadows ---- */
  --shadow-sm: 0 1px 3px rgba(15, 38, 71, 0.06);
  --shadow-md: 0 6px 20px rgba(15, 38, 71, 0.08);
  --shadow-lg: 0 10px 40px rgba(15, 38, 71, 0.10);
  --shadow-xl: 0 20px 60px rgba(15, 38, 71, 0.14);
}
```

---

## 1. Buttons

Azure drives primary actions. Gogolook Blue carries secondary/outline. Blue Iris is the accent. Ghost is chromeless. Disabled is muted.

### Variants

| Variant | Background | Text color | Border | Hover |
|---------|-----------|------------|--------|-------|
| **Primary** | `var(--blue)` (#41A9F6) | `#FFFFFF` | none | `#2B8FD4` (darken ~12%) |
| **Secondary / Outline** | `#FFFFFF` | `var(--azure)` (#0058EA) | 1.5px solid `var(--azure)` | `rgba(0,88,234,.06)` bg |
| **Accent** | `var(--iris)` (#5A5B9F) | `#FFFFFF` | none | `#4A4B87` (darken) |
| **Ghost** | transparent | `var(--ink-2)` (#5A6577) | none | `var(--mist)` bg, `var(--navy)` text |
| **Disabled** | `#E6ECF5` | `#9AA6B6` | none | cursor: not-allowed |

### Sizes

| Size | Padding | Font size | Class |
|------|---------|-----------|-------|
| Small | `8px 14px` | 13px | `.btn-sm` |
| Default | `11px 20px` | 14px | `.btn` |
| Large | `14px 26px` | 15px | `.btn-lg` |

### Base styles

```css
.btn {
  font-family: var(--body);
  font-weight: 600;
  font-size: 14px;
  border-radius: var(--r-md);   /* 10px */
  padding: 11px 20px;
  border: 1px solid transparent;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 8px;
  transition: 0.15s;
  line-height: 1;
}
```

### Usage guidance

- Primary buttons: one per section/card. Use for the main CTA ("Run Score", "Export", "Apply Filter").
- Secondary/outline: secondary actions adjacent to a primary ("Cancel", "Reset", "View Details").
- Accent: special actions tied to IRIS-specific flows ("Analyze", "Enrich").
- Ghost: tertiary or inline actions within dense layouts.
- Never stack two primary buttons side by side.

---

## 2. Form Controls

### Text inputs

```css
.input {
  font-family: var(--body);
  font-size: 14px;
  padding: 11px 14px;
  border: 1px solid var(--line);
  border-radius: var(--r-md);   /* 10px */
  background: var(--white);
  color: var(--navy);
  outline: none;
  width: 100%;
  transition: 0.15s;
}
.input::placeholder { color: #9AA6B6; }
.input:focus {
  border-color: var(--blue);
  box-shadow: 0 0 0 3px rgba(65, 169, 246, 0.18);
}
```

### Labels and hints

```css
.field label {
  font-size: 13px;
  font-weight: 600;
  color: var(--navy);
}
.hint {
  font-size: 12px;
  color: var(--ink-2);
}
```

### Toggles

- Track: 44px wide, 26px tall, border-radius full
- On state: `var(--blue)` background
- Off state: `#CDD6E4` background
- Knob: 20px circle, white, with subtle shadow

### Select dropdowns

- Follow the same border, radius, padding, and focus ring as text inputs.
- Dropdown chevron: stroke icon, `var(--ink-2)` color, 16px.

---

## 3. Badges

### Brand badges

| Variant | Background | Text |
|---------|-----------|------|
| **Blue** | `rgba(65, 169, 246, 0.12)` | `var(--blue)` |
| **Azure** | `rgba(0, 88, 234, 0.12)` | `#0049A0` |
| **Iris** | `rgba(90, 91, 159, 0.14)` | `var(--iris)` |

### Risk badges

| Variant | Background | Text |
|---------|-----------|------|
| **High** | `rgba(229, 72, 77, 0.12)` | `#C53B3F` |
| **Medium** | `rgba(245, 166, 35, 0.18)` | `#A96E10` |
| **Low** | `rgba(47, 184, 122, 0.16)` | `#1F8F5D` |

### Base styles

```css
.badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-weight: 600;
  font-size: 12px;
  padding: 5px 11px;
  border-radius: var(--r-full);  /* 999px — pill shape */
  line-height: 1;
}
```

### Usage guidance

- Brand badges: feature labels, category tags, status indicators (non-risk).
- Risk badges: exclusively for risk-related status — never use as decorative labels.
- Badges can include a leading dot or small icon (max 12px).

---

## 4. Risk Levels (A-E)

The IRIS risk scale uses a 5-stop color ramp from safe (A) to dangerous (E). These colors are used **only** in risk-level UI — never as general brand colors.

| Level | Color | Hex | Meaning |
|-------|-------|-----|---------|
| **A** | Green | `#2FB87A` | Low risk — auto-approve |
| **B** | Lime | `#8FBE52` | Below average risk — lean approve |
| **C** | Amber | `#F5A623` | Medium risk — manual review |
| **D** | Orange | `#EE6A45` | Elevated risk — lean reject |
| **E** | Red | `#E5484D` | High risk — auto-reject |

### Visual spec

```css
.lv b {
  width: 50px;
  height: 50px;
  border-radius: 13px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--display);
  font-weight: 700;
  font-size: 20px;
  color: #FFFFFF;
}
```

### Usage guidance

- Display as a row of 5 colored squares with the letter centered.
- In compact contexts (table cells), use a smaller 28px square or a colored dot + letter.
- Always pair the letter grade with the color — do not use color alone for accessibility.
- The 5-stop ramp (A-E) is distinct from the 3-stop semantic scale (high/med/low).

---

## 5. Score Display

The primary way IRIS surfaces a single risk score and its percentile rank.

### Large score

```css
.score {
  font-family: var(--display);
  font-weight: 800;
  font-size: 52px;
  color: var(--blue);
  font-variant-numeric: tabular-nums;
  letter-spacing: -0.02em;
  line-height: 1;
}
.score small {
  font-size: 18px;
  color: var(--ink-2);
  font-weight: 600;
  margin-left: 4px;
}
```

### Percentile bar

```css
.pct-track {
  height: 10px;
  border-radius: var(--r-full);
  background: var(--line);   /* #E6ECF5 */
  position: relative;
  overflow: hidden;
}
.pct-fill {
  position: absolute;
  left: 0; top: 0; bottom: 0;
  border-radius: var(--r-full);
  background: linear-gradient(90deg, var(--blue), var(--azure));
}
.pct-meta {
  display: flex;
  justify-content: space-between;
  font-size: 12px;
  color: var(--ink-2);
  margin-top: 9px;
  font-variant-numeric: tabular-nums;
}
```

### Usage guidance

- Score value is always displayed in Azure with tabular-nums.
- The `/100` or `/1000` suffix uses secondary text color and smaller weight.
- Percentile bar fills left-to-right with the brand gradient (Azure to Gogolook Blue).
- Below the bar, show "0th" on the left and "100th" on the right.

---

## 6. Data Tables

Designed for phone-number lookups, feature lists, and batch results.

```css
.tbl {
  width: 100%;
  border-collapse: collapse;
  font-size: 14px;
}
.tbl th {
  text-align: left;
  font-family: var(--display);
  font-weight: 600;
  font-size: 11px;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--ink-2);
  padding: 14px 18px;
  background: var(--mist);        /* #F3F8FE */
  border-bottom: 1px solid var(--line);
}
.tbl td {
  padding: 15px 18px;
  border-bottom: 1px solid var(--line);
  color: var(--navy);
  font-variant-numeric: tabular-nums;
}
.tbl tr:last-child td {
  border-bottom: 0;
}
```

### Container

```css
.tbl-wrap {
  background: var(--white);
  border: 1px solid var(--line);
  border-radius: var(--r-lg);    /* 16px */
  overflow: hidden;
}
```

### Usage guidance

- Header row: Iris Mist background, uppercase labels in Plus Jakarta Sans.
- Row separation: 1px bottom border (never alternating row stripes).
- Phone numbers: use Inter with `letter-spacing: 0.02em` for legibility.
- Numeric columns: right-align with tabular-nums.
- Sortable columns: append a 12px chevron icon (stroke, `var(--ink-2)`).
- Wrap the table in `.tbl-wrap` for rounded corners and border.

---

## 7. Console Shell

The IRIS console layout: a navy sidebar with a white content area.

### Sidebar

```css
.console-side {
  background: var(--navy);        /* #0F2647 */
  padding: 22px 16px;
  display: flex;
  flex-direction: column;
  gap: 4px;
  width: 210px;
}
```

### Navigation items

```css
.nav-i {
  font-size: 15px;
  padding: 11px 14px;
  border-radius: var(--r-sm);   /* 8px */
  color: #C3CFE8;
  cursor: default;
}
.nav-i.on {
  background: rgba(65, 169, 246, 0.22);
  color: #FFFFFF;
  font-weight: 600;
}
```

### Quota card (sidebar widget)

```css
.quota {
  background: rgba(255, 255, 255, 0.06);
  border: 1px solid rgba(255, 255, 255, 0.14);
  border-radius: 12px;
  padding: 18px;
  text-align: center;
}
.quota .q {
  font-family: var(--display);
  font-weight: 800;
  font-size: 36px;
  color: #FFFFFF;
  font-variant-numeric: tabular-nums;
  line-height: 1;
}
.quota .ql {
  font-size: 13px;
  color: #AEBFDA;
  margin-top: 8px;
}
```

### Main area

```css
.console-main {
  padding: 24px;
  background: var(--white);
}
.console-main h5 {
  font-family: var(--display);
  font-weight: 700;
  font-size: 16px;
  color: var(--navy);
}
```

### Usage guidance

- Sidebar brand mark: the IRIS circle containment logo at the top.
- Active nav item gets the Azure-tinted background.
- Sidebar collapses to an icon rail below 680px.
- Main area holds page-specific content (tables, scores, KPIs, charts).
- The quota card shows API call balance — always tabular-nums.

---

## 8. KPI Cards

For dashboard-level metrics: total queries, hit rate, average score, etc.

```css
.kpi {
  background: var(--white);
  border: 1px solid var(--line);
  border-radius: var(--r-lg);    /* 16px */
  padding: 22px 24px;
}
.kpi-label {
  font-size: 12px;
  color: var(--ink-2);
  font-weight: 500;
  margin-bottom: 10px;
}
.kpi-val {
  font-family: var(--display);
  font-weight: 700;
  font-size: 32px;
  color: var(--navy);
  font-variant-numeric: tabular-nums;
  line-height: 1;
  letter-spacing: -0.02em;
}
```

### Trend badge

```css
.kpi-trend {
  display: inline-flex;
  align-items: center;
  gap: 4px;
  font-size: 12px;
  font-weight: 600;
  margin-top: 10px;
  padding: 3px 8px;
  border-radius: var(--r-full);
}
.kpi-trend.up   { background: rgba(47, 184, 122, 0.14); color: #1F8F5D; }
.kpi-trend.down { background: rgba(229, 72, 77, 0.12);  color: #C53B3F; }
.kpi-trend.flat { background: rgba(90, 101, 119, 0.10); color: var(--ink-2); }
```

### Sparkline area

- Height: ~40px, placed at the bottom of the card.
- Fill: `var(--blue)` at 8% opacity.
- Stroke: `var(--blue)` at 1.5px.
- No axis labels on the sparkline itself — the KPI value is the label.

### Usage guidance

- Lay out in a 4-column grid (`repeat(4, 1fr)`, gap 20px), collapsing to 2 columns below 760px.
- Each card: label at top (small, secondary text), value below (large, navy), trend badge below value, sparkline at bottom.
- Trend badge: up arrow = green, down arrow = red, flat = neutral gray. The arrow is a 10px stroke icon.

---

## 9. Charts

### Horizontal bar chart

```css
.bar-row {
  display: grid;
  grid-template-columns: 90px 1fr 48px;
  align-items: center;
  gap: 12px;
}
.bar-track {
  height: 28px;
  background: var(--mist);
  border-radius: var(--r-sm);  /* 8px */
  overflow: hidden;
}
.bar-fill {
  height: 100%;
  border-radius: var(--r-sm);
  transition: width 0.6s ease;
}
.bar-label {
  font-size: 13px;
  color: var(--ink-2);
  font-weight: 500;
  text-align: right;
}
.bar-val {
  font-size: 13px;
  font-weight: 600;
  color: var(--navy);
  font-variant-numeric: tabular-nums;
}
```

### Area line chart

- Container: 200px height, responsive width.
- Area fill: `var(--blue)` at ~10% opacity.
- Line stroke: `var(--azure)` at 2px.
- Grid lines: `var(--line)` at 0.5px, horizontal only.
- Data points: 4px circles, `var(--azure)` fill, on hover expand to 6px with tooltip.

### Mini donuts

```css
.mini-donut {
  display: flex;
  align-items: center;
  gap: 18px;
  background: var(--white);
  border: 1px solid var(--line);
  border-radius: var(--r-lg);
  padding: 22px 24px;
}
.mini-donut svg {
  width: 64px;
  height: 64px;
  flex-shrink: 0;
}
.mini-donut .md-val {
  font-family: var(--display);
  font-weight: 700;
  font-size: 22px;
  color: var(--navy);
  font-variant-numeric: tabular-nums;
  line-height: 1;
}
.mini-donut .md-label {
  font-size: 12.5px;
  color: var(--ink-2);
  margin-top: 4px;
}
```

### Chart card container

```css
.chart-card {
  background: var(--white);
  border: 1px solid var(--line);
  border-radius: var(--r-xl);  /* 18px */
  padding: 28px;
}
.chart-title {
  font-family: var(--display);
  font-weight: 700;
  font-size: 15px;
  color: var(--navy);
  margin-bottom: 4px;
}
.chart-sub {
  font-size: 12px;
  color: var(--ink-2);
  margin-bottom: 22px;
}
```

### Legend

```css
.legend {
  display: flex;
  gap: 18px;
  margin-top: 16px;
  flex-wrap: wrap;
}
.legend-item {
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: 12px;
  color: var(--ink-2);
}
.legend-dot {
  width: 10px;
  height: 10px;
  border-radius: 3px;
  flex-shrink: 0;
}
```

### Chart color palette

For multi-series charts, use in this order:
1. `var(--blue)` — Azure (#41A9F6)
2. `var(--azure)` — Gogolook Blue (#0058EA)
3. `var(--iris)` — Blue Iris (#5A5B9F)
4. `var(--sky)` — Iris Sky (#7EDFFE)
5. `var(--navy)` at 40% opacity — for a fifth series if needed

Never use semantic risk colors (red/amber/green) for non-risk data series.

### Usage guidance

- Lay charts out in a 2-column grid, collapsing to 1 column below 820px.
- Bar charts: label on the left, bar in the center, value on the right.
- Bar fill color: use `var(--blue)` for single-metric bars, or the chart color palette for multi-category.
- Donuts: SVG-based, stroke-dasharray technique. Center text shows the primary metric.

---

## 10. Iconography

IRIS uses **stroke-based icons** — never filled icons.

### Specification

| Property | Value |
|----------|-------|
| **viewBox** | `0 0 24 24` |
| **Stroke width** | 1.6px |
| **Stroke linecap** | round |
| **Stroke linejoin** | round |
| **Fill** | none (stroke only) |
| **Default color** | `var(--navy)` (#0F2647) |
| **Default size** | 24px (minimum 16px) |

### CSS

```css
.icon {
  width: 24px;
  height: 24px;
  stroke-width: 1.6;
  stroke-linecap: round;
  stroke-linejoin: round;
  fill: none;
  stroke: currentColor;
}
```

### Icon cell (grid display)

```css
.icon-cell {
  background: var(--white);
  border: 1px solid var(--line);
  border-radius: 14px;
  padding: 28px 16px 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 14px;
}
.icon-cell svg {
  width: 32px;
  height: 32px;
  color: var(--navy);
  stroke-width: 1.6;
}
.icon-cell span {
  font-family: var(--display);
  font-size: 10.5px;
  font-weight: 600;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--ink-2);
}
```

### Core icon set

These icons appear across the IRIS console and marketing surfaces:

- **Shield** — risk/security
- **Search** — lookup, query
- **Phone** — phone intelligence
- **Alert-triangle** — risk warning
- **Bar-chart** — analytics
- **Users** — accounts
- **Check-circle** — approved / low risk
- **X-circle** — rejected / high risk
- **Trending-up/down** — trend indicators
- **Download** — export
- **Filter** — filter controls
- **Settings** — configuration

### Usage guidance

- Icons at 24px for standard UI, 32px for icon-grid display, 16px minimum for dense tables.
- Color: `var(--navy)` by default. Use `var(--blue)` for active/selected states. Use semantic colors only inside risk-data contexts.
- Always pair icons with a text label in navigation and buttons. Icon-only is acceptable only in dense table actions or toolbars with tooltips.
- Icon grid layout: 5 columns, 3 columns at 760px, 2 columns at 480px.

---

## Responsive Breakpoints

| Breakpoint | Width | Behavior |
|-----------|-------|----------|
| **Desktop** | > 860px | Full layouts — 4-col KPIs, 2-col charts, sidebar visible |
| **Tablet** | 760px - 860px | 2-col KPIs, 1-col charts, sidebar collapses |
| **Mobile** | < 760px | Single column, stacked cards, nav links hidden |
| **Small mobile** | < 480px | 2-col icon grid, reduced padding |

---

## Accessibility Requirements

- **WCAG AA contrast** on all text elements.
- Azure (`#41A9F6`) is not used as text color on white backgrounds (fails AA). White text/icons on Azure fills.
- Gogolook Blue (`#0058EA`), Blue Iris (`#5A5B9F`), and Navy (`#0F2647`) all pass AA on white.
- Focus ring: `box-shadow: 0 0 0 3px rgba(65, 169, 246, 0.18)` on interactive elements.
- Risk levels must convey meaning through both color AND text/letter (A-E or High/Med/Low).
- Respect `prefers-reduced-motion`: disable animations and transitions.
- Touch targets: minimum 44px on mobile.
