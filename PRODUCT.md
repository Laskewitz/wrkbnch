# Product

## Register

brand

> Dual nature: the surface in this repo (the docs/showcase page, `index.html`) is a **brand** surface — it markets and demonstrates the framework, so its design *is* the product. The framework it ships, however, exists to build **product** UIs (dashboards, consoles, developer tools). Default to `brand` for the docs page; when designing example app screens or component demos that stand in for real product UI, switch the working register to `product`.

## Users

Two audiences, served by one artifact:

- **Developers** building interfaces who want a drop-in, dependency-free CSS layer. They link one stylesheet, write semantic HTML, and get a complete, accessible component set — no build step, no JavaScript, no framework lock-in. Their context: shipping internal tools, dashboards, and apps where they'd rather not hand-roll a design system.
- **AI coding agents** generating UI. wrkbnch gives them a predictable, well-documented vocabulary of classes and tokens so generated interfaces come out coherent and on-brand instead of as generic slop. The `wrkbnch` Copilot skill exists for exactly this.

The job to be done: *"Give me interfaces that feel built, not generated — without making me build a design system first."*

## Product Purpose

wrkbnch is a warm, utilitarian design system delivered as a single pure-CSS file (`wrkbnch-css` on npm). It provides design tokens and 50+ components — forms, navigation, data display, overlays, feedback, disclosure — with first-class dark mode, all reachable through semantic HTML and utility classes. No JavaScript runtime, no build step required.

It exists as a deliberate counter to AI-default interface aesthetics. Success looks like: a developer or agent links the stylesheet and ships something that looks intentionally crafted — warm, earthy, honest — on the first try, and an end user can't tell it came from a generator.

## Brand Personality

- **Three words:** warm, utilitarian, honest.
- **Voice:** plain-spoken and confident. It explains what a component is for, shows it working, and trusts the reader. No marketing froth, no hype adjectives.
- **Feel:** interfaces that feel *built, not generated* — like a well-organized workbench. Earthy and tactile rather than glossy. Practices what it preaches: the docs page is itself made entirely with wrkbnch.

## Anti-references

The whole project is a rejection of generic AI-generated SaaS aesthetics. Specifically avoid:

- Cream / sand / beige body backgrounds as the "warm" default (the saturated AI move). Warmth lives in the accents and type, not a tinted near-white canvas.
- Gradient text (`background-clip: text`).
- Identical icon-heading-text card grids repeated down the page.
- Glassmorphism as decoration.
- The hero-metric template (big number, small label, gradient accent).
- Per-section uppercase tracked eyebrows and `01 / 02 / 03` numbered section markers used as scaffolding.
- Reflex-reject display fonts and the SaaS-cream / navy-and-gold lanes.

## Design Principles

1. **Practice what you preach.** The docs page is built entirely with wrkbnch. If a component isn't good enough for our own marketing, it isn't good enough to ship.
2. **Show, don't tell.** Every component is demonstrated live with copyable markup, plus a short note on *when* to use it — not just described.
3. **Built, not generated.** Favor choices that read as deliberate and tactile over choices that read as safe defaults. Warmth and character come from type, accent, and rhythm.
4. **No-dependency honesty.** Pure CSS, semantic HTML, no build step. The constraint is the feature; never reach for JS where CSS will do.
5. **Accessible by construction.** Contrast, focus states, reduced-motion, and keyboard reach are defaults of the system, not opt-ins.

## Accessibility & Inclusion

- Target **WCAG 2.1 AA**: body text ≥4.5:1, large/bold text ≥3:1, against its actual background in both light and dark themes.
- Visible focus styling on all interactive components via a dedicated focus color; never rely on color alone to convey state.
- Honor `prefers-reduced-motion: reduce` — every animation has a crossfade or instant alternative.
- Full dark-mode parity, so contrast and legibility hold in both themes.
- Semantic HTML first (real `<button>`, `<nav>`, `<details>`, form labels) so assistive tech and keyboard navigation work without extra wiring.
