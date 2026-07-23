# CLAUDE.md

Guidance for Claude Code (and other AI assistants) working in this repository.

## What this project is

**Showcash** is a single-page, animated showcase of products built by
Rajan Bhattarai ([@cdrrazan](https://github.com/cdrrazan)). It is a static
site — no framework, no build step, no dependencies.

## Repository layout

```
index.html    The entire site: markup, CSS, and JS in one self-contained file
README.md     Project overview with product table
assets/       Images used by the README (banner, screenshots)
CLAUDE.md     This file
```

## Architecture of index.html

- **Product data** lives in the `products` array inside the `<script>` tag.
  Each entry has: `name`, `cat` (category shown on the card and used by the
  filter bar), `tagline`, `desc`, `url`, `github`, `stack` (array), and
  `status` (`live` | `dev` | `soon`).
- The filter bar is generated from the distinct `cat` values; the colophon
  cell stays visible in every filter and spans the remainder of the last
  grid row (`sizeColophon()`).
- Cards are rendered into `#grid` by mapping over `products` — to add or edit
  a product, change the data array, not the markup.
- Cover images fall back to a gradient + monogram via an inline `onerror`
  handler, so cards never show broken images.
- Animations: aurora background (pure CSS), staggered scroll-in reveal via
  `IntersectionObserver`, hover lift/glow. All animation respects
  `prefers-reduced-motion`.
- Theme variables are defined in `:root` at the top of the stylesheet.

## Conventions

- Keep the site a **single self-contained HTML file** — inline all CSS/JS.
  Do not introduce build tools, package.json, or external JS libraries.
  The one permitted external resource is the Google Fonts stylesheet
  (Google Sans, used for all text including headings); the stack must
  keep a system-ui fallback so the page renders correctly offline.
- Colors are Material 3-style tokens in `:root` (dark default) with light
  overrides under `:root[data-theme="light"]` and
  `prefers-color-scheme: light` — surface/on-surface/primary/container
  pairs seeded from navy blue. Never hard-code a color in a component
  rule — add a token. Buttons use the `.btn` classes (filled, tonal,
  outlined, text) with an `::after` state layer.
- External images (GitHub avatars, OpenGraph previews) must always have a
  graceful fallback.
- Never invent product facts. Unverified products are labeled
  "In Development" or "Coming Soon" with no dead links.
- Product statuses: `live` requires a working public URL; `dev` means the
  repo exists but no public site; `soon` means nothing public yet.

## Verifying changes

There is no test suite. Verify visually:

```sh
python3 -m http.server   # then open http://localhost:8000
```

Or headless (Chromium + Playwright), checking for `pageerror` events and
that `document.querySelectorAll('.card').length` matches the product count.

## Git

- Default branch: `main`.
- Write clear, descriptive commit messages; one logical change per commit.
