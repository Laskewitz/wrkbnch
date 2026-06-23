# Changelog

## 1.2.0

Design overhaul: escaping the AI-generated aesthetic.

### Breaking: Typography
- Display font: Bricolage Grotesque (was Fraunces)
- Body font: Karla (was Instrument Sans)
- Mono font: JetBrains Mono (was IBM Plex Mono)
- Update your Google Fonts link accordingly

### Breaking: Color
- `--chalk` (body bg): now `#ffffff` (was `#f5f2ec` cream)
- `--sand` (surface): now `#f0ede7` (was `#e8dcc8`)
- Warmth is carried by accents and typography, not background

### Changed
- `.gradient-text` renamed to `.accent-text` (solid copper, no gradient)
- `.brand-mark.lg` uses solid copper instead of gradient text
- `.quote-block` border thinned from 3px accent to 2px neutral
- Docs page: dark hero, varied section backgrounds, mobile nav hamburger
- Docs page: component usage guidance added to key sections
- Docs page: em-dash copy rewritten for natural cadence

## 1.1.0

Component expansion — 34 new components added.

### New: Enhanced Forms
- Checkbox, Radio, Switch — custom-styled toggle controls
- Segmented control — pill-shaped option selector
- Input group — prefix/suffix affixes
- Floating labels — animated field labels
- Combobox — dropdown with search
- Range slider — styled range input
- Dropzone — drag-and-drop file upload area

### New: Navigation
- Dropdown menu — positioned overlay
- Sidebar nav — vertical navigation
- Stepper — multi-step progress indicator

### New: Data Display
- Avatar (sm/md/lg) — circular user representation
- Timeline — vertical event history
- List group — bordered structured list

### New: Feedback & Overlays
- Tooltip — hover info overlay
- Popover — rich tooltip with title/body
- Banner — full-width informational bar
- Drawer — slide-in side panel
- Spinner (sm/md/lg) — loading animation
- Skeleton — content placeholder shimmer

### New: Disclosure
- Accordion — expandable/collapsible sections

### New: Buttons & Badges
- Button group — joined button row
- FAB — floating action button
- Tag — removable badge with close
- Version badge — monospace version indicator
- Cmd pill — command-line snippet badge
- Kbd — keyboard shortcut indicator

### New: Typography & Layout
- Gradient text — accent gradient on text
- Quote block — styled blockquote
- Styled list — list with custom markers
- Styled link — link with underline offset
- Section — consistent section padding
- Feature/stat/footer grids
- Divider with label — centered text rule
- Skip link — accessibility navigation

---

## 1.0.0

Initial release.

- Design tokens: color palette, typography scale, spacing, radii, shadows
- Layout utilities: container, stack, cluster, grid, split
- Typography: display, heading, body, mono, muted, meta
- Components: buttons, cards, panels, badges, alerts, forms, tables, nav, tabs, code blocks, terminal
- Dark/light mode via `data-mode` attribute
- Copilot skill for AI-assisted usage
- Documentation page
