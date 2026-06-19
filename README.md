# wrkbnch CSS

A warm, utilitarian design system built entirely in CSS. No JavaScript, no build step.

[![npm version](https://img.shields.io/npm/v/wrkbnch-css)](https://www.npmjs.com/package/wrkbnch-css)
[![License: MIT](https://img.shields.io/badge/License-MIT-c45d2c.svg)](./LICENSE)

→ [Documentation](https://laskewitz.github.io/wrkbnch/)

---

## Colors

The palette is warm and earthy — neutrals with purposeful accents:

| Token | Hex | Role |
|-------|-----|------|
| `--copper` | `#c45d2c` | Primary accent |
| `--slate` | `#4a6670` | Secondary accent |
| `--moss` | `#5a7a52` | Success / positive |

Each accent has a soft tint variant (`--copper-tint`, `--slate-tint`, `--moss-tint`) for backgrounds, and accessible text variants (`--copper-text`, `--slate-text`, `--moss-text`) for use on light surfaces.

Surface colors: `--sand`, `--chalk`, `--ink`, `--charcoal` provide the warm neutral canvas.

---

## Typography

Three typefaces at specific roles:

- **Instrument Sans** — UI text (body, headings, labels)
- **IBM Plex Mono** — Code blocks, metadata, structural labels
- **Fraunces** — Display accents, hero text

---

## Install

```bash
npm install wrkbnch-css
```

Or link directly:

```html
<link rel="stylesheet" href="https://laskewitz.github.io/wrkbnch/wrkbnch.min.css">
```

### Font Setup

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,700;1,9..144,400&family=IBM+Plex+Mono:wght@400;500;600&family=Instrument+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
```

### Dark Mode

```html
<html data-mode="light">  <!-- Force light -->
<html data-mode="dark">   <!-- Force dark -->
<html>                     <!-- System preference -->
```

---

## Components

wrkbnch includes components optimized for AI-generated app interfaces:

- **Layout**: container, stack, cluster, grid, split
- **Typography**: display, heading, body, mono, muted
- **Buttons**: primary, default, ghost, danger (sm/lg variants)
- **Cards & Panels**: raised cards, inset panels, flush cards
- **Badges**: accent, success, warning, danger, info (with dot indicator)
- **Alerts**: contextual feedback in accent, success, warning, danger, info
- **Forms**: inputs, textareas, selects, labels, hints, errors
- **Tables**: responsive, compact, striped, mono variants
- **Navigation**: horizontal/vertical nav, tabs, breadcrumbs, pagination
- **Code & Terminal**: inline code, code blocks, terminal emulator
- **Data**: key-value lists, log viewer
- **Status**: status dots, progress bars
- **Feedback**: toasts, empty states, dialogs
- **Command Palette**: searchable action list

See the [documentation](https://laskewitz.github.io/wrkbnch/) for live examples.

---

## Copilot Skill

wrkbnch ships with a Copilot skill file at `skill/wrkbnch/SKILL.md` that teaches AI agents how to use the design system correctly — including behavioral rules, component selection guidance, and anti-patterns to avoid.

---

## License

[MIT](./LICENSE)
