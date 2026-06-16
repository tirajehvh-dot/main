# OM Page Templates

Reusable, brand-matched Offering Memorandum page templates (Marcus & Millichap · LAAA Team style).
Built as single-file HTML that renders to PDF at the exact OM page size (**US Letter, landscape — 11ʺ × 8.5ʺ**).

## `market-overview.html` — Market Overview (Area & Demand Drivers)

A redesigned **Section 09 · Location / Market Overview** page, modeled on the 601 Pearl "demand
driver" approach: a narrative hook + **Demand Drivers** + an **Area Highlights / Points of Interest**
list with approximate distances (hospitals, transit, job centers, freeway access, culture).

### Reuse for a new deal
Edit **only** the `OM = { ... }` config block in the `<script>` at the bottom of the file —
no markup or CSS changes are needed. You control:

- `eyebrow`, `title`, `locus` — header
- `lead` — the serif hook sentence (`<b>…</b>` renders in orange)
- `narrative` — paragraphs about the submarket
- `drivers` — the four demand-driver cards
- `poi` — the points-of-interest rows: `{ tag, name, sub, dist, unit }`
- `stats` — the six-up demographic strip (`hl: true` colors a stat green)
- `footnote`, `footBrand`, `footCenter`, `footPage`

### Brand tokens (CSS `:root`)
`--navy #0D2245` · `--orange #E07B3A` · `--green #1D6B44` · fonts **Playfair Display** + **Inter**
(all sampled from the existing OM).

### Export to PDF
Open in Chrome → **Print** → *Save as PDF* → **Landscape**, paper **Letter**, margins **None**,
**Background graphics ON**. (A pre-rendered `market-overview.pdf` is included.)

### Notes
- All distances are **approximate** drive distances for orientation and are labeled buyer-verified.
- Demographics are ACS/Census estimates for ZIP 90023 (matching the source OM).
