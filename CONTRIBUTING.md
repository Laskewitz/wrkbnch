# Contributing to wrkbnch

Thanks for your interest in contributing.

## Development

```bash
npm install
npm run dev
```

This starts a live server on port 3000 with the documentation page.

## Making Changes

1. Edit `wrkbnch.css` directly — it's the source of truth.
2. Run `npm run build` to regenerate the minified version.
3. Update `index.html` if you've added or changed components.
4. Update `skill/wrkbnch/SKILL.md` if behavior rules or component APIs changed.

## Guidelines

- Use existing design tokens. Don't introduce new color systems or spacing scales.
- Every component must work in both light and dark mode.
- Accessibility: all text/background combinations must meet WCAG AA (4.5:1 for body text).
- Keep the framework zero-JS. Interactivity comes from the consumer, not the framework.

## Pull Requests

- One feature or fix per PR.
- Include before/after screenshots if visual changes are involved.
- Update the CHANGELOG.

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
