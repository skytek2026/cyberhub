# CyberHub — project notes

## Design system (binding)
- This project uses the **Skytek Design System**, bound at:
  `_ds/skytek-design-system-fda4f434-27a8-4d78-8fa7-92ccd315175d/`
- Always load the **bound, latest** version in every page/DC `<helmet>`:
  - `<link rel="stylesheet" href="_ds/skytek-design-system-fda4f434-27a8-4d78-8fa7-92ccd315175d/styles.css">`
  - `<script src="_ds/skytek-design-system-fda4f434-27a8-4d78-8fa7-92ccd315175d/_ds_bundle.js"></script>`
  - (from `modals/` and other subfolders, prefix with `../`)
- The DS namespace for `<x-import component-from-global-scope="…">` is `SkytekDesignSystem_fda4f4`.
- The latest DS **overrides all existing UI implementations**. Existing code is legacy and may be incorrect — defer to the DS.
- Do **not** use any earlier/legacy DS copy (the old `ds/skytek/` folder has been removed). Use only the bound version above.

## Scrollbars
- The DS themes the page scrollbar globally (`html`) — a 6px brand-blue thumb on a light-grey track (DS Motion → Scrollbars, v2.2.0).
- For **inner** scroll containers (anything with `overflow:auto/scroll` — drawers, lists, wide tables), add `data-scroll` (or class `ds-scroll`) so they get the same themed bar.
