# IRIS Presentation / Slide Deck Rules

Rules for generating IRIS-branded slide decks as single-file HTML presentations.
Every deck must follow these visual rules, slide type specs, and QA checks.

---

## 1. Slide Color Palette

| Role | Name | Hex | Usage |
|------|------|-----|-------|
| Primary fill | Azure | `#41A9F6` | Accent bars, highlights, active indicators, button fills |
| Secondary | Gogolook Blue | `#0058EA` | Secondary accents, chart fills, icon tints |
| Accent | Blue Iris | `#5A5B9F` | Supporting surfaces, muted accents, badge fills |
| Dark bg | Iris Navy | `#0F2647` | Cover, section break, data dashboard backgrounds |
| Light bg | Iris Mist | `#F3F8FE` | Content slide backgrounds |
| Text on dark | White | `#FFFFFF` | All text on navy backgrounds |
| Text on light | Iris Navy | `#0F2647` | Headings, titles on light backgrounds |
| Body text | Secondary ink | `#5A6577` | Body copy on light backgrounds |
| Borders | Line | `#E6ECF5` | Card borders, dividers on light slides |

**Semantic risk colors** (data slides only):
- High risk: `#E5484D`
- Medium risk: `#F5A623`
- Low risk: `#2FB87A`

Never use risk colors decoratively. They appear only on data slides to represent
risk levels.

---

## 2. Fonts

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headlines | Plus Jakarta Sans | 300 | Tracking -0.02em. Use 300 (light) for all slide titles including cover. |
| Body | Inter | 400 / 500 | Line-height 1.5. Use 500 for emphasis within body. |
| Data / numbers | Inter | 500 / 700 | `font-variant-numeric: tabular-nums` on all figures. |
| CJK / regional | Noto Sans TC/JP/KR/TH | 400 / 500 / 700 | Use when deck contains non-Latin content. |

Load via Google Fonts:
```html
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
```

---

## 3. Slide Types

Every IRIS deck draws from these 8 slide types. Not every deck uses all types.

### Type 1 — Cover

- **Background:** Iris Navy (`#0F2647`) with subtle brand gradient overlay
  (`#0058EA -> #41A9F6 -> #7EDFFE`, low opacity, radial from bottom-right)
- **Content:** IRIS logotype (white SVG) centered horizontally, upper third.
  Below: deck title (Plus Jakarta Sans 300, white, 48-56px), subtitle line
  (Inter 400, `rgba(255,255,255,0.7)`, 18-20px), date and presenter name
  (Inter 400, `rgba(255,255,255,0.5)`, 14px)
- **Tagline:** "See risk clearly." in Plus Jakarta Sans 300, white, letterspaced
  (+0.08em), positioned below the logotype, above the title
- **Decorative:** Single concentric circle accent (thin stroke, `rgba(65,169,246,0.12)`)
  in bottom-right corner. Max 3 concentric rings.

### Type 2 — Agenda

- **Background:** Iris Navy (`#0F2647`)
- **Title:** "Agenda" — Plus Jakarta Sans 300, white, 36px, top-left area
- **Items:** Numbered list (01, 02, 03...) using Inter 500, white, 20px.
  Number in Azure (`#41A9F6`), section name in white. Vertical stack with
  24px gap between items.
- **Active indicator:** Optional Azure left-border bar (3px) on the current
  section when used as a recurring navigation slide.

### Type 3 — Section Break

- **Background:** Iris Navy (`#0F2647`)
- **Content:** Section number (Inter 500, Azure `#41A9F6`, 16px, letterspaced)
  above section title (Plus Jakarta Sans 300, white, 44-52px). Centered
  vertically and horizontally.
- **Decorative:** Subtle Azure accent — a single thin horizontal rule (1px,
  `rgba(65,169,246,0.25)`, 120px wide) below the title.

### Type 4 — Content (Light)

- **Background:** Iris Mist (`#F3F8FE`)
- **Title:** Plus Jakarta Sans 300, Iris Navy, 28-32px, top-left with 64px
  top padding
- **Body area:** Inter 400/500, `#5A6577`, 16-18px, max-width 720px for
  readability. Bullet points use Azure circle markers.
- **Footer:** IRIS wordmark (navy, small) bottom-left + confidentiality line
  bottom-center.
- **Cards:** White background, 1px `#E6ECF5` border, 16px radius, 24-32px
  padding. Use for grouping related content.

### Type 5 — Data Dashboard

- **Background:** Iris Navy (`#0F2647`)
- **Title:** Plus Jakarta Sans 300, white, 28px, top-left
- **KPI cards:** 2-4 cards in a row. Each card: `rgba(255,255,255,0.06)`
  background, 16px radius, 24px padding. Value in Plus Jakarta Sans 300,
  white, 36px, tabular-nums. Label in Inter 400, `rgba(255,255,255,0.6)`,
  13px. Optional trend arrow (green up / red down) beside the value.
- **Chart area:** Below KPI cards. Charts use brand palette (Azure, Gogolook
  Blue, Blue Iris) for non-risk data; risk colors for risk data.
- **Footer:** Same as content slides but white text on navy.

### Type 6 — Risk Distribution

- **Background:** Iris Navy (`#0F2647`)
- **Title:** Plus Jakarta Sans 300, white, 28px
- **Risk bars:** Horizontal bars for risk levels A-E. Each bar labeled with
  the level letter, count, and percentage. Bar fill colors:

  | Level | Color | Hex |
  |-------|-------|-----|
  | A (lowest risk) | Low green | `#2FB87A` |
  | B | Azure | `#41A9F6` |
  | C | Gogolook Blue | `#0058EA` |
  | D | Medium amber | `#F5A623` |
  | E (highest risk) | High red | `#E5484D` |

- **Donut variant:** Risk donut chart centered, with alert icon in center
  and risk level legend beside it. Segments use the same A-E color mapping.
- **Labels:** Always pair color with text labels. Never rely on color alone.

### Type 7 — Two-Column

- **Background:** Iris Mist (`#F3F8FE`) or white
- **Layout:** 50/50 or 60/40 split. Left column: text content (title + body
  or bullet list). Right column: visual (chart, screenshot, illustration,
  or data card).
- **Title:** Plus Jakarta Sans 300, Iris Navy, 28px
- **Body:** Inter 400, `#5A6577`, 16px
- **Divider:** Optional thin vertical line (`#E6ECF5`, 1px) between columns,
  or use whitespace (32-48px gap) alone.

### Type 8 — Summary / CTA

- **Background:** White with Azure accent bar (8px) along the top edge
- **Content:** Key takeaways as 3-4 bullet points (Inter 500, Iris Navy, 18px).
  Below: CTA block — action text (Plus Jakarta Sans 300, Gogolook Blue, 24px)
  and contact info (Inter 400, `#5A6577`, 14px).
- **IRIS logotype:** Navy, bottom-left, small.
- **Gogolook co-brand:** If applicable, "Powered by Gogolook" or Gogolook logo
  bottom-right.

---

## 4. Footer (Every Content Slide)

Present on every slide except Cover and Section Break.

- **Bottom-left:** IRIS wordmark (navy on light slides, white on dark slides),
  max 48px wide
- **Bottom-center:** "Confidential & Copyright of Gogolook Co., Ltd." — Inter
  400, 10px, `#5A6577` on light / `rgba(255,255,255,0.4)` on dark
- **Bottom-right:** Slide number — Inter 400, 11px, same color rules as center

Footer sits in a 40px-tall strip with 32px horizontal padding.

---

## 5. Decorative Elements

- **Concentric circle accent:** Thin stroke (1px), low-opacity Azure
  (`rgba(65,169,246,0.10)`), placed at one corner only. Max 3 rings. Used on
  Cover and optionally on Section Break slides.
- **Risk donut chart:** For data slides showing risk distribution. Single
  alert icon in center, 4-5 colored segments with even gaps.
- **Gradient logotype:** The Gogolook Blue -> Azure -> Sky gradient fill on the
  IRIS wordmark is permitted on Cover slides only.
- **Rule:** Never use more than one decorative element per slide. The design
  should feel open and clear — ornamentation competes with data.

---

## 6. Slide Navigation (HTML Output)

Decks are single-file HTML with keyboard and click navigation.

```
Arrow Right / Down / Space / Click  ->  Next slide
Arrow Left / Up                     ->  Previous slide
Home                                ->  First slide
End                                 ->  Last slide
F / Escape                          ->  Toggle fullscreen (optional)
```

Use CSS `scroll-snap-type: x mandatory` with horizontal scroll, or JS-based
slide index with transform transitions. Must work as `file://` without a server.

Slides should be 16:9 aspect ratio (1920x1080 reference), scaled to fit the
viewport with `object-fit: contain` behavior.

---

## 7. Workflow

1. **Brief** — Gather: topic, audience, key messages, desired slide count,
   whether data slides are needed.
2. **Outline** — Create a slide-by-slide outline with type, title, and key
   points for each slide. Present to user for approval.
3. **Generate** — Build the full HTML deck following the slide type specs above.
4. **Self-check** — Run the QA checklist below.
5. **Iterate** — Fix failures, re-check. Up to 10 passes.
6. **Handoff** — Present the file path and a summary of the deck.

---

## 8. QA Checklist for Presentations

### Visual compliance
- [ ] Cover slide uses navy background with IRIS logotype and tagline
- [ ] Section break slides use navy background with Azure accent
- [ ] Content slides use mist or white background
- [ ] Data slides use navy background
- [ ] Only IRIS palette colors used — no off-palette colors
- [ ] Azure fills use white text/icons
- [ ] Risk colors appear only on data slides, never decoratively

### Typography
- [ ] Headlines: Plus Jakarta Sans 300
- [ ] Body: Inter 400/500
- [ ] All numbers use tabular-nums
- [ ] No typefaces outside the IRIS stack (Plus Jakarta Sans / Inter / Noto Sans)

### Layout
- [ ] Footer on every content slide (wordmark + confidentiality + slide number)
- [ ] Max one decorative element per slide
- [ ] No content overflow on any slide at 16:9
- [ ] Generous whitespace — slides never feel crowded
- [ ] Text line lengths capped at ~720px for readability

### Functionality
- [ ] Keyboard navigation works (arrows, space, home, end)
- [ ] Click/tap advances slides
- [ ] Works as file:// without server
- [ ] Responsive — works on projector (1920x1080) and laptop screens (1440x900)

### Brand
- [ ] IRIS logotype rendered correctly (not stretched, recolored, or shadowed)
- [ ] Gradient logotype only on Cover slide
- [ ] "Confidential & Copyright of Gogolook Co., Ltd." present
- [ ] Tone is evidence-led, precise — no hype language
