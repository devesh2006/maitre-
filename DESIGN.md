---
name: Metro Transit Command
colors:
  surface: '#fbf8ff'
  surface-dim: '#dad9e3'
  surface-bright: '#fbf8ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f4f2fd'
  surface-container: '#eeedf7'
  surface-container-high: '#e8e7f1'
  surface-container-highest: '#e3e1ec'
  on-surface: '#1a1b22'
  on-surface-variant: '#434655'
  inverse-surface: '#2f3038'
  inverse-on-surface: '#f1effa'
  outline: '#737686'
  outline-variant: '#c3c6d7'
  surface-tint: '#0053db'
  primary: '#004ac6'
  on-primary: '#ffffff'
  primary-container: '#2563eb'
  on-primary-container: '#eeefff'
  inverse-primary: '#b4c5ff'
  secondary: '#555e74'
  on-secondary: '#ffffff'
  secondary-container: '#d7dff9'
  on-secondary-container: '#5a6278'
  tertiary: '#4b5569'
  on-tertiary: '#ffffff'
  tertiary-container: '#636d82'
  on-tertiary-container: '#ebefff'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dbe1ff'
  primary-fixed-dim: '#b4c5ff'
  on-primary-fixed: '#00174b'
  on-primary-fixed-variant: '#003ea8'
  secondary-fixed: '#d9e2fc'
  secondary-fixed-dim: '#bdc6e0'
  on-secondary-fixed: '#121b2e'
  on-secondary-fixed-variant: '#3e475b'
  tertiary-fixed: '#d9e3fb'
  tertiary-fixed-dim: '#bdc7de'
  on-tertiary-fixed: '#111c2d'
  on-tertiary-fixed-variant: '#3d475a'
  background: '#fbf8ff'
  on-background: '#1a1b22'
  surface-variant: '#e3e1ec'
typography:
  headline-xl:
    fontFamily: Inter
    fontSize: 36px
    fontWeight: '600'
    lineHeight: 44px
    letterSpacing: -0.02em
  headline-xl-mobile:
    fontFamily: Inter
    fontSize: 28px
    fontWeight: '600'
    lineHeight: 36px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.015em
  headline-sm:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Inter
    fontSize: 15px
    fontWeight: '400'
    lineHeight: 22px
  body-md:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '400'
    lineHeight: 18px
  body-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
  label-md:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.01em
  label-sm:
    fontFamily: Inter
    fontSize: 11px
    fontWeight: '500'
    lineHeight: 14px
    letterSpacing: 0.02em
  mono-data:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  gutter: 0.75rem
  gutter-desktop: 1rem
  margin: 1rem
  margin-desktop: 1.5rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 0.75rem
  space-lg: 1rem
  space-xl: 1.5rem
---

## Brand & Style

This design system serves high-density mission-critical transit monitoring and safety dispatch. The aesthetic prioritizes absolute legibility, rapid data digestion, and quiet authority, drawing directly from the functional rigor of high-performance developer tools and financial infrastructure (Linear, Stripe, Vercel). 

Key characteristics:
- **Style Archetype:** Precision Enterprise Minimalism. High structural discipline, zero decorative distractions, pure utility.
- **Atmosphere:** Cool, clinical, reliable, and deeply organized. Avoids dark sci-fi control-room tropes, neon status glows, or skeuomorphic physical toggles in favor of razor-sharp tabular data and high-contrast typography.
- **Emotional Intent:** Calm operational control, confidence under stress, zero latency perception.

## Colors

The color palette is built for rapid optical parsing, reserving high-chroma tones strictly for telemetry changes, warnings, and interactive affordances.

### Foundation
- **Canvas Base:** `#F7F8FA` — Soft, off-white background engineered to reduce eye strain over 12-hour operator shifts.
- **Surfaces & Panels:** `#FFFFFF` — Pure white foreground containers to anchor dense data blocks.
- **Structural Borders:** `#E5E7EB` — Hairline delimiters providing division without visual mass.
- **Primary Typography:** `#172033` — Deep slate-navy offering sharp contrast ratios (>12:1) against white panels.
- **Secondary Typography:** `#667085` — Mid-tone neutral for metadata, unit indicators, and timestamps.
- **Interactive Blue:** `#2563EB` — Restrained accent reserved exclusively for active states, link paths, and focused controls.

### Operational Semantics
- **Nominal / Clear:** `#16A34A` (Background tint: `#F0FDF4`, Border tint: `#BBF7D0`)
- **Caution / Delay:** `#D97706` (Background tint: `#FFFBEB`, Border tint: `#FDE68A`)
- **Emergency / Critical:** `#DC2626` (Background tint: `#FEF2F2`, Border tint: `#FECACA`)

No linear or radial color gradients are permitted on data displays or status indicators.

## Typography

Typography relies on `Inter` for exceptional vertical metrics, neutral geometric letterforms, and high legibility at micro sizes.

- **Tabular Figures:** All tabular and telemetry interfaces must activate OpenType tabular numbers (`tnum`) to eliminate column jitter when time, speed, and train IDs change dynamically.
- **Monospace Pairing:** Train serial numbers, signal block IDs, and geocoordinates use `JetBrains Mono` at `12px` to prevent alphanumeric misinterpretation (e.g., distinguishing `0` vs `O`, `1` vs `I`).
- **Hierarchy:** Restrained weight delta (primarily 400 for content, 500 for metadata badges, and 600 for structural titles). Avoid bold weights exceeding 600.

## Layout & Spacing

The layout model optimizes for simultaneous multi-panel density across ultra-wide operations monitors while gracefully degrading down to incident commander tablets.

- **Grid Strategy:** 12-column desktop fluid grid using dense gutters (`1rem` / `16px`) to maximize data display efficiency. Outer canvas padding is pinned to `1.5rem` (`24px`).
- **Density Over Sprawl:** Margins and gap values default to compact steps (`space-sm` at 8px, `space-md` at 12px) allowing complex track diagrams, telemetry feeds, and alert feeds to remain visible above the fold.
- **Responsive Adaptations:**
  - **Desktop (≥ 1280px):** Multi-column tiled panel layout. Lateral panels for live alerts (fixed 360px), main area for track maps, lower drawer for telemetry logs.
  - **Tablet (768px – 1279px):** Collapsible lateral drawer; primary telemetry stacks vertically under track visualizers.
  - **Mobile (< 768px):** Strict single-column stack with persistent bottom-pinned critical incident bar.

## Elevation & Depth

Visual separation relies on structural boundaries rather than dramatic z-axis shadows.

- **Low-Contrast Hairlines:** The primary separation mechanism is a crisp `1px solid #E5E7EB` border. Stacked containers rely on alternating fills (`#FFFFFF` against `#F7F8FA`) instead of drop shadows.
- **Ambient Shadows:** Drop shadows are restricted exclusively to floating overlays, modal confirmations, and popover menus:
  - `box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05), 0 4px 6px -1px rgba(0, 0, 0, 0.02);`
- **Zero AI/Cyber Glows:** Status alerts, live trains, and caution nodes must never emit box-shadow glows or pulse effects. Hierarchy is expressed through high-contrast boundary definition and distinct badge fills.

## Shapes

The design system employs a disciplined, slightly softened industrial geometry (`roundedness: 1`).

- **Base Radius:** `4px` (`0.25rem`) applied to cards, data table containers, action buttons, and form inputs.
- **Badges & Indicators:** Pill shapes (`9999px`) are strictly reserved for operational status tags to visually differentiate them from interactive rectangular buttons and data chips.
- **Segmented Controls:** Housed inside a container with `4px` border-radius; internal segments follow a matching `2px` inner radius.

## Components

### Buttons
- **Primary:** Solid `#2563EB`, text `#FFFFFF`, 0.25rem radius, `1px solid transparent`. Hover: `#1D4ED8`. Focus: `2px solid #2563EB` with `2px` white offset.
- **Secondary / Neutral:** Background `#FFFFFF`, text `#172033`, border `1px solid #E5E7EB`. Hover: `#F9FAFB`.
- **Destructive / Emergency Stop:** Background `#DC2626`, text `#FFFFFF`. Hover: `#B91C1C`.
- **Dimensions:** Compact `28px` (height) for dense toolbars, standard `34px` for modals and global actions.

### Status Badges & Pills
- **Structure:** Pill-shaped (`rounded-full`), height `20px`, padding `0 8px`, typography `label-sm` (boldness 500).
- **Nominal:** Background `#F0FDF4`, border `1px solid #BBF7D0`, text `#16A34A`. Includes a leading `6px` solid circular dot.
- **Caution:** Background `#FFFBEB`, border `1px solid #FDE68A`, text `#D97706`.
- **Critical / Interruption:** Background `#FEF2F2`, border `1px solid #FECACA`, text `#DC2626`.

### Data Tables & Track Logs
- **Grid:** Clean row borders with `1px solid #E5E7EB`. Header row has background `#F9FAFB`, text `#667085`, uppercase `11px`, tracking `0.05em`.
- **Rows:** Alternating rows not required; hover state uses subtle `#F9FAFB`. Compact row height set to `36px` to ensure 20+ records remain visible without scrolling.

### Inputs & Filters
- **Fields:** Background `#FFFFFF`, border `1px solid #E5E7EB`, text `#172033`, placeholder `#9CA3AF`. Height `32px`, font size `13px`.
- **Focus:** Border changes to `#2563EB` with no ambient blur.

### Cards & Telemetry Panels
- **Structure:** `#FFFFFF` background, `1px solid #E5E7EB`, 4px border radius. Header separated by a solid hairline divider, padding `12px 16px`. Zero elevation shadow.

### Track Schematic Nodes
- **Lines & Tracks:** Solid `2px` vectors in `#E5E7EB` (inactive) or `#2563EB` (active corridor).
- **Block Signals:** Fixed `8x8px` squares directly placed on tracks, changing strictly between `#16A34A`, `#D97706`, and `#DC2626`.