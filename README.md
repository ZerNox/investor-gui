# investor-gui

Static hosting for the **investor** web dashboard, served via GitHub Pages at:

> https://zernox.github.io/investor-gui/

## How this repo is maintained

This repo is **auto-published** — do not edit the built files by hand. The
dashboard source lives in the [`investor`](https://github.com/ZerNox/investor)
repo under `web/`. A scheduled job there runs:

```bash
investor-web-publish
```

which exports the latest dashboard JSON, runs the Vite production build
(base path `/investor-gui/`), mirrors the built `web/dist/` into this repo's
root, and commits + pushes. The published commit replaces the previous site.

## Layout (generated)

- `index.html` — SPA entry point
- `assets/` — hashed JS/CSS bundles
- `data/` — exported dashboard JSON
- `.nojekyll` — disables Jekyll so Vite's `_`-prefixed assets are served as-is

## Pages configuration

- **Source**: deploy from a branch — `main`, root (`/`).
- Jekyll is disabled via `.nojekyll`.
