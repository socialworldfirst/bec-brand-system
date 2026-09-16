# CHANGELOG — Ant brand system

Every change to tokens, rules, assets or BRAND.md, newest first. Feedback from the brand team is logged in `_feedback/feedback_log.json` and referenced here by id.

## 2026-09-15 · v2026-09-15.1 · system created
- Source: Brand Center download `antbrand.zip` (35 files, WorldFirst + Ant International fonts) → `00_intake/antbrand_2026-09-15/`.
- Built: manifest (92 entries), tokens.json (palette + gradients from the pattern guideline; type scale, grid, spacing, radius, buttons imported from BEC Figma DLS via `~/Documents/Claude/WFxWD_DLS/figma_tokens.json`), rules.json (37 rules), BRAND.md, index.html, 56 icons exported, map/globe exported, fonts.css.
- PROVISIONAL (awaiting guideline or BEC confirmation): LOG-03 minimum logo size 24 px; LOG-06 clear space = height of W; gradient 70/30 interpreted as a CSS colour-hint midpoint.
- Known conflicts left as observed values: hover pink #BC0050 (live build) vs #EB004B (BEC Figma, canonical) vs #E0004A (wforge context).

## 2026-09-16 — guard.py TYP-01 false negative fixed
`font-family` regex `([^;}\"']+)` excluded quote characters, so any quoted family (`font-family:'Alibaba PuHuiTi'`) never entered the `fams` set. Two consequences: quoted foreign fonts were never flagged by TYP-01 (a block rule silently passing), and CJK builds that correctly declared a quoted Alibaba PuHuiTi were wrongly advised "PuHuiTi not declared". Changed to `([^;}]+)`; the per-family `.strip("'\"")` already in place handles the quotes. Regression-tested: a quoted `"Comic Sans MS"` now blocks. Backup at `tools/guard.py.bak`. Found while verifying the /bec corrected mockups for the 16 Sep review.

## 2026-09-16 — index.html asset anchors
Every asset tile now carries `id="<asset-id>"` (27 tiles) plus `:target` highlight styling, so /bec findings can deep-link to the exact asset (e.g. `index.html#wf-partnership-template-en`). Backup at `index.html.bak`.
