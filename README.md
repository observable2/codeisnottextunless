# The Code is Not the Text: Generator 101

a generator that writes 101 statements of the form “the code is not the text unless it is the text”. Made for Nick Monfort et al., [*Our Generation*](https://badquar.to/publications/our_generation.html) (2024). Refresh the page to regenerate.

Refactored (2026-11-08) from the Observable Framework project `codeisnottextunless` into an
[Observable Notebook Kit](https://observablehq.com/notebook-kit/) project.
Co-implemented with Claude Sonnet 5.5.

## Commands

```sh
npm install
npm run preview   # http://localhost:5173
npm run build     # builds into dist/
```

## Where things went

- Framework → Notebook Kit: index.md → `nbks/index.html` (a markdown heading, a pinned JS cell showing the generator code, a markdown note and an `html` output cell).
- Framework `observablehq.config.js`, `.observablehq/` cache and `rimraf` are no longer needed.
- Markup that JavaScript touches is created in a JS cell with `html` (cells run in dependency order, not page order, so the DOM must exist before code looks for it).

## Differences from the original

- Fonts: none changed (theme fonts from the Kit).
- Page chrome (sidebar, header, footer, pager) is gone; Notebook Kit has none.
