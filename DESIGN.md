# Design

Visual system for **wrkbnch** — a warm, utilitarian, pure-CSS design system. This document captures the real tokens and components as shipped in `wrkbnch.css` (v1.2.0). It is the source of truth for keeping variants on-brand. See `PRODUCT.md` for the strategic register, users, and principles.

## Theme

Warm and earthy, not cool and corporate. The canvas is a true off-white (chroma 0), so warmth is carried by the **accents and typography**, never by a cream/sand body tint. The mood is a well-organized workbench: tactile, honest, built. Full light/dark parity — dark mode is a first-class theme, not an afterthought, toggled via `data-mode="dark"` on the root.

## Color

One dominant accent per surface. Copper leads; slate and moss are supporting roles. Every accent ships a `-tint` (background), `-text` (accessible on light), and `-dark` (dark-mode) variant.

### Brand & accent palette

| Token | Hex | Role |
|---|---|---|
| `--copper` | `#c45d2c` | Primary accent |
| `--copper-tint` | `#fdf0ea` | Copper background wash |
| `--copper-text` | `#9e4420` | Copper text on light surfaces |
| `--copper-dark` | `#e8784a` | Copper in dark mode |
| `--slate` | `#4a6670` | Secondary accent (links, focus) |
| `--slate-tint` | `#edf3f5` | Slate background wash |
| `--slate-text` | `#3a5259` | Slate text on light surfaces |
| `--slate-dark` | `#7ba8b5` | Slate in dark mode |
| `--moss` | `#5a7a52` | Success / positive |
| `--moss-tint` | `#eef5ec` | Moss background wash |
| `--moss-text` | `#456b3d` | Moss text on light surfaces |
| `--moss-dark` | `#7fad74` | Moss in dark mode |
| `--danger` | `#b83a3a` | Destructive / error |
| `--warning` | `#a86b1d` | Caution |

Danger and warning carry the same `-tint` / `-text` / `-dark` family.

### Neutrals & surfaces

| Token | Hex | Role |
|---|---|---|
| `--chalk` | `#ffffff` | Body background (light) — true off-white, chroma 0 |
| `--sand` | `#f0ede7` | Raised/secondary surface (light) |
| `--sand-dim` | `#e5e1da` | Recessed surface |
| `--ink` | `#1a1a18` | Primary text (light) / background (dark) |
| `--charcoal` | `#2d2d2a` | Surface (dark) |
| `--graphite` | `#3d3d3a` | Raised surface (dark) |

### Semantic roles (theme-aware)

These resolve per theme — design against the role, not the raw hue.

| Role | Light | Dark |
|---|---|---|
| `--color-bg` | `--chalk` `#ffffff` | `--ink` `#1a1a18` |
| `--color-surface` | `--sand` `#f0ede7` | `--charcoal` `#2d2d2a` |
| `--color-surface-raised` | `#ffffff` | `--graphite` `#3d3d3a` |
| `--color-text` | `--ink` `#1a1a18` | `#f0ede8` |
| `--color-text-muted` | `#5c5c58` | `#a8a8a3` |
| `--color-text-faint` | `#8a8a85` | `#6e6e69` |
| `--color-border` | `#d1cbbf` | `#4a4a46` |
| `--color-border-subtle` | `#e5e0d8` | `#3a3a36` |
| `--color-accent` | `--copper` | `--copper-dark` |
| `--color-link` | `--slate-text` | `--slate-dark` |
| `--color-focus` | `--slate` | `--slate-dark` |

### Contrast

WCAG 2.1 AA. Body text targets ≥4.5:1, large/bold ≥3:1, in both themes. Muted text (`--color-text-muted`) is intentionally kept dark enough (#5c5c58 → ~6.7:1 on white) to stay readable — never light gray "for elegance". When a component renders on its own surface inside a contrasting band, re-assert the component's native text colors rather than letting the band's override bleed through.

## Typography

Three families on a contrast axis (humanist sans + grotesque display + mono), never two lookalikes.

| Token | Stack | Role |
|---|---|---|
| `--font-sans` | `'Karla', -apple-system, …, sans-serif` | UI text: body, headings, labels |
| `--font-display` | `'Bricolage Grotesque', Georgia, serif` | Display accents, hero text |
| `--font-mono` | `'JetBrains Mono', 'SF Mono', monospace` | Code, metadata, structural labels, timestamps |

### Type scale

| Token | Size |
|---|---|
| `--text-xs` | 0.75rem |
| `--text-sm` | 0.8125rem |
| `--text-base` | 0.9375rem |
| `--text-md` | 1.0625rem |
| `--text-lg` | 1.25rem |
| `--text-xl` | 1.5rem |
| `--text-2xl` | 2rem |
| `--text-3xl` | 2.75rem |
| `--text-4xl` | 3.5rem |

Hero title uses `clamp(2.25rem, 6vw, 4.5rem)` — display ceiling stays ≤ 4.5rem.

### Weights & leading

Weights: `--weight-regular` 400, `--weight-medium` 500, `--weight-semibold` 600, `--weight-bold` 700, `--weight-heavy` 800.
Leading: `--leading-tight` 1.2, `--leading-normal` 1.5, `--leading-relaxed` 1.7.
Mono labels are uppercase, tracked, in `--font-mono` for status/metadata — a deliberate brand device, not a per-section eyebrow.

## Spacing

4px-based scale: `--space-1` 0.25rem through `--space-24` 6rem (1, 2, 3, 4, 5, 6, 8, 10, 12, 16, 20, 24). Vary spacing for rhythm; don't apply one uniform gap everywhere.

## Layout

Containers: `--container-sm` 640 · `--container-md` 768 · `--container-lg` 1024 · `--container-xl` 1200 · `--container-2xl` 1400px.
Primitives: `.stack` (1D vertical gap), `.cluster` (inline wrap with gap), `.grid` (2D). Flex for 1D, Grid for 2D; responsive grids use `repeat(auto-fit, minmax(…, 1fr))`.

## Shape & elevation

Radii: `--radius-sm` 3px · `--radius-md` 6px · `--radius-lg` 10px · `--radius-xl` 16px · `--radius-full` 9999px.
Borders: `--border-thin` (1px `--color-border`), `--border-subtle` (1px `--color-border-subtle`).
Shadows: `--shadow-sm` → `--shadow-xl`, low-alpha and tight in light mode, deeper in dark mode. Elevation is restrained — borders do more work than shadows.

## Motion

Durations: `--duration-fast` 100ms · `--duration-normal` 200ms · `--duration-slow` 350ms.
Easing: `--ease-default` `cubic-bezier(0.4, 0, 0.2, 1)`, `--ease-out` `cubic-bezier(0, 0, 0.2, 1)`. Ease out, no bounce/elastic. Every animation honors `prefers-reduced-motion: reduce`.

## Components

50+ components, all reachable through semantic HTML + utility classes, no JS:

- **Actions:** buttons (primary / default / ghost / danger / sizes), button groups, version badges, command pills, `kbd`.
- **Forms:** inputs, selects, textareas, form hints, validation states, checkbox/radio, switch, segmented control, input group, OTP input, range slider, dropzone.
- **Navigation:** horizontal nav, tabs, breadcrumbs, pagination, sidebar nav, nav rail, stepper, command palette.
- **Data display:** cards, panels, tables, progress bars, description lists, key-value lists, log viewer, stats row, bar chart, timeline, list groups, calendar card, avatars, figures.
- **Feedback:** alerts, toasts, dialogs, banners, tooltips, hover cards, context menus, spinners, skeletons, badges, status indicators, empty states.
- **Disclosure:** accordion, details groups.
- **Surfaces:** hero (`.hero`, `.hero-lg`, `.hero-full`, `.hero-surface`, `.hero-accent`), quote block, styled list, divider-with-label.
- **Patterns:** pricing grid, testimonial card, and other compound layouts.

### Bans (carried from the brand register)

No gradient text, no side-stripe accent borders, no decorative glassmorphism, no cream/sand body backgrounds, no per-section uppercase eyebrows or `01 / 02 / 03` numbered scaffolding, no identical icon-heading-text card grids.

## Dark mode

Toggle `data-mode="dark"` on the root. Surfaces shift to the ink/charcoal/graphite ramp, text to `#f0ede8`, accents to their `-dark` variants, shadows deepen. Components that sit on their own light surface inside a dark band must keep their native colors so contrast holds.
