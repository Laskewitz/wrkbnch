---
name: wrkbnch
description: "Apply the wrkbnch design language to frontend work. Warm, utilitarian CSS for AI-generated interfaces that feel built, not generated."
---

# wrkbnch Skill

You are designing with **wrkbnch CSS**. Your job is to make interfaces feel specific, warm, utilitarian, and built — like tools from a well-organized workshop.

**Warm CSS for precise products.** The framework provides structure and warmth. The product, data, and workflow speak.

If this skill conflicts with generic web-design instincts, this skill wins.

---

## P0 Behavioral Rules

These rules block output. Do not emit UI until they pass.

1. **No generic SaaS structure.** Never default to Hero → Features → Testimonials → Pricing → CTA.
2. **No decorative emptiness.** Every card, badge, stat, and section must carry product meaning.
3. **No fake specificity.** Do not invent numbers, logos, quotes, avatars, customers, or metrics. Use honest placeholders.
4. **No centered marketing fog.** Prefer left-aligned, information-dense layouts. Center only for narrow confirmations, empty states, or single-purpose prompts.
5. **No rainbow styling.** One dominant accent per surface. Copper for action/brand, slate for information, moss for success/progress.
6. **No emoji. Ever.** Use SVG icons from Lucide, Phosphor, or Tabler sized to `--icon-sm`/`--icon-md`/`--icon-lg` tokens. If no icon clarifies, use none.
7. **No stock icon grids.** Icons are optional, small, and clarifying. They are not content.
8. **No bloated copy.** Labels must name the actual object, action, input, output, or consequence.
9. **No arbitrary CSS values.** Use wrkbnch tokens/classes. Custom CSS may compose tokens, not replace them.
10. **No template recipes.** Use layout decisions from the content. Do not copy a canned page shape.
11. **No unreviewed output.** Run the self-review scan before finalizing.

---

## Authority Hierarchy

1. **User's requested content and product context** — source of truth for meaning.
2. **wrkbnch behavioral rules in this file** — source of truth for taste.
3. **`wrkbnch.css`** — source of truth for class names, tokens, and component APIs.
4. **`index.html`** — source of truth for live examples and edge cases.
5. Your general design knowledge — only when it does not conflict with the above.

---

## Required Setup

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,300;12..96,400;12..96,700;12..96,800&family=JetBrains+Mono:wght@400;500;600&family=Karla:wght@400;500;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://laskewitz.github.io/wrkbnch/wrkbnch.min.css">
```

Use `<html data-mode="light">`, `<html data-mode="dark">`, or omit `data-mode` for system preference.

Docs: https://laskewitz.github.io/wrkbnch

---

## wrkbnch Personality

wrkbnch feels like:

- A well-lit studio with concrete floors and warm wood surfaces.
- Dense information made navigable through strict hierarchy.
- Utilitarian without being cold — warm neutrals instead of blue-grays.
- Monospace as structural texture, not as decoration or gimmick.
- Confident negative space — not afraid to leave empty.
- Built from real app surfaces, not mockups or Dribbble shots.

wrkbnch does **not** feel like:

- Gradient blob SaaS.
- Emoji-and-card dashboards.
- "Unlock your potential" landing pages.
- Purple-blue glassmorphism.
- Cold developer tools with only blue-gray palettes.
- Fake enterprise trust walls.

---

## Color Usage

The palette is warm and earthy. Use color with intention.

| Token | Role | When to use |
|-------|------|-------------|
| `--copper` | Primary accent | Actions, brand moments, active states |
| `--slate` | Secondary accent | Links, informational highlights, focus states |
| `--moss` | Success/positive | Confirmations, health indicators, progress |
| `--danger` | Destructive | Errors, delete actions, critical states |
| `--warning` | Caution | Rate limits, expiring states, degraded status |

Rules:
- One dominant accent per surface (usually copper).
- Use `-tint` variants for backgrounds, `-text` variants for accessible body text.
- Never apply accent colors as decoration. Color signals state or action.

---

## Quick Decision Tree

### 1. Product page or landing page?

**Technical/workflow-based:**
- Lead with a real workflow slice: command, config, dashboard row, event stream.
- Structure: problem context → working surface → specific capabilities → action.

**Conceptual/early-stage:**
- Lead with a crisp positioning statement and one concrete example.
- Structure: claim → example → mechanics → next step.

### 2. App or dashboard?

**Data-primary:**
- Start with the most important table, log, queue, or status surface.
- Summary cards are subordinate to the work surface.
- Structure: context bar → filters/actions → primary data surface → secondary detail.

**Action-primary:**
- Make the next action unmistakable. Show inputs and consequences.
- Structure: current state → available action → preview/result → confirmation.

**Monitoring:**
- Calm density: status, trends, exceptions, timestamps.
- Structure: system state → exceptions → recent activity → drill-down.

### 3. Docs or developer reference?

- Lead with the smallest working example.
- Structure: outcome → install/setup → example → options → troubleshooting.

### 4. Component?

- Design around its state model (default, empty, loading, error, success).
- Structure internally by state, not by visual flourish.

### 5. Sparse content?

- Do not inflate into a full page. Create a focused single-screen composition.

---

## Component Selection Guide

Choose the right component for the data:

| Data shape | Use | Not |
|---|---|---|
| List of records with columns | `.table` | Cards |
| Key-value metadata | `.kv-list` | Table |
| Status with category | `.badge` with `.badge-dot` | Colored text alone |
| Sequential events | `.timeline` or `.log-viewer` | Table |
| Single metric with context | `.card` with `.heading-xl` | Badge |
| User action needed | `.btn-primary` in context | Floating FAB |
| Long-running result | `.spinner` + status text | Spinner alone |
| Nothing to show | `.empty-state` with action | Hidden section |
| Confirmation needed | `.dialog` | Inline form |
| System feedback | `.toast` or `.banner` | Alert in content flow |
| Multiple actions available | `.command-palette` | Dropdown menu |
| Boolean settings | `.switch` | Checkbox |
| Multi-option selection | `.segmented-control` | Radio group |
| Progressive disclosure | `.accordion` | Tabs for 2 items |
| Person/entity identity | `.avatar` + name text | Icon alone |
| Step-by-step process | `.stepper` | Numbered list |
| Vertical navigation | `.sidebar-nav` | Horizontal tabs |
| Removable categories | `.tag` | Badge |
| Loading placeholder | `.skeleton` | Spinner for layout |
| File upload | `.dropzone` | Bare input[file] |
| Keyboard shortcuts | `kbd` element | Code block |

---

## Layout Postures

Pick one dominant posture per page/section.

### Workflow-led
- Anchor with a realistic work surface (terminal, editor, task list, event timeline).
- Show inputs, transformation, and output.

### Data-led
- Prioritize tables, queues, filters, and summaries.
- Let density be beautiful. Use whitespace to group, not to dilute.

### Evidence-led
- Put proof before persuasion.
- Show logs, policies, checks, uptime, audit trails.

### Editorial-led
- Strong hierarchy, short sections, and sharp prose.
- Prefer pull quotes and code examples over feature grids.

---

## AI Design Tells: P0 Blockers

Scan every emitted surface for these. If found, revise before output.

| Tell | Symptom | Replacement |
|---|---|---|
| Generic hero stack | Huge centered headline, vague subhead, two CTAs | Left-aligned claim plus concrete product surface |
| Three feature cards | "Fast / Secure / Easy" grid | Show workflow steps, states, or actual capabilities |
| Fake metrics | "10x faster", "99.9%" without source | Use "Metric pending" or remove |
| Gradient blob background | Purple/blue glow with no meaning | Subtle token color, border, or no decoration |
| Icon confetti | Same-size icon above every card | Use text hierarchy; icons only where they disambiguate |
| Buzzword copy | "Transform your workflow" | Name the input, action, output, and consequence |
| Repetitive cards | Identical cards with swapped nouns | Vary form: table, timeline, code, checklist, stat |
| Floating testimonial | Quote/avatar invented | Use provided quotes only; otherwise show evidence or omit |
| Oversized CTA band | Final gradient box repeating headline | End with practical next step, command, or compact CTA |
| Decorative dashboard | Charts with meaningless labels | Domain-specific rows, logs, statuses |
| Centered everything | All sections aligned center | Left alignment and asymmetric content rhythm |

---

## Copy Rules

wrkbnch copy is specific, compressed, and operational.

Write like this:
- "Replay failed jobs from the last deploy."
- "Compare config drift before merging."
- "3 instances healthy. Next deploy queued."
- "Paste a webhook payload; get a typed handler."

Do not write like this:
- "Streamline your workflow."
- "Powerful insights at your fingertips."
- "Everything you need to succeed."
- "Beautifully designed for modern teams."

Test: **Could this headline appear on 500 unrelated startup sites?** If yes, rewrite.

---

## Class Usage Anchors

Core layout:
- `container` for page width. `container-sm` through `container-2xl` for variants.
- `stack` for vertical rhythm. `stack-sm` through `stack-2xl` for gap sizes.
- `cluster` for horizontal grouping.
- `grid`, `grid-2`, `grid-3`, `grid-4`, `grid-auto` for grids.
- `split`, `split-sidebar`, `split-content` for two-column layouts.

Core typography:
- `display-xl`, `display-lg`, `display-md` for Bricolage Grotesque display text.
- `heading-xl` through `heading-sm` for Karla headings.
- `body-lg`, `body-md`, `body-sm` for body text.
- `mono`, `mono-sm`, `mono-label` for JetBrains Mono.
- `text-muted`, `text-faint`, `text-accent`, `text-success` for color.

Core components:
- Buttons: `.btn`, `.btn-primary`, `.btn-ghost`, `.btn-danger`, `.btn-sm`, `.btn-lg`
- Cards: `.card`, `.card-sm`, `.card-flush`
- Panels: `.panel`, `.panel-header`, `.panel-inset`
- Badges: `.badge`, `.badge-accent`, `.badge-success`, `.badge-warning`, `.badge-danger`, `.badge-info`, `.badge-dot`
- Alerts: `.alert`, `.alert-accent`, `.alert-success`, `.alert-warning`, `.alert-danger`, `.alert-info`
- Forms: `.form-group`, `.form-label`, `.form-input`, `.form-textarea`, `.form-select`, `.form-hint`, `.form-error`
- Tables: `.table-wrap`, `.table`, `.table-compact`, `.table-striped`, `.table-mono`
- Navigation: `.nav`, `.nav-item`, `.nav-vertical`, `.breadcrumb`, `.tabs`, `.tab`, `.pagination`
- Code: `code`, `pre`, `.terminal`, `.terminal-header`, `.terminal-prompt`, `.terminal-output`
- Data: `.kv-list`, `.kv-key`, `.kv-value`, `.log-viewer`, `.log-entry`
- Status: `.status-dot`, `.progress`, `.progress-bar`
- Feedback: `.toast`, `.empty-state`, `.dialog`
- Command: `.command-palette`, `.command-palette-input`, `.command-palette-list`, `.command-palette-item`

Utilities: spacing (`p-*`, `px-*`, `py-*`, `mt-*`, `mb-*`), flex, border, background, text alignment, overflow, width, animation.

---

## Honest Placeholder Rule

When real content is missing, be explicit:
- "Customer quote pending"
- "Metric not yet measured"
- "Connect data source to populate this table"
- "Example event payload"

Do not use:
- Fake people, logos, avatars, companies.
- Fake growth metrics.
- Lorem ipsum in product surfaces.
- Placeholder copy that sounds finished.

---

## Self-Review Scan

Before final output:

1. **Structure**: Did I choose a posture from the decision tree? Is the primary surface specific to the user's content?
2. **Content**: Are all claims specific? Are placeholders honest?
3. **Visual**: Is alignment left or purposefully asymmetric? One dominant accent? No gradient blobs?
4. **Framework**: Are fonts and CSS loaded correctly? Did I use wrkbnch classes before custom CSS?

If any answer fails, fix the output silently. Do not explain the failure.

---

## Final Standard

A successful wrkbnch result should feel:

- Specific to this product.
- Warm but not soft.
- Dense but not cramped.
- Technical without being hostile.
- Polished without obvious AI tells.

If the page could be renamed to another product by changing only the logo, it is not done.
