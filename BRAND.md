# BRAND.md — Ant International brand system, local (read this first)

**Home:** `~/Downloads/ant-brand-system/` · **Built:** 15 Sep 2026 from the Brand Center download `antbrand.zip` · **Owner:** Steven · **Direction:** aligned to Ant International's BEC brand team (their Brand Center + Figma DLS).

This file is the constitution. Every graphical build for WorldFirst (or any Ant International brand) loads it before starting and runs `/bec` before declaring done. Assets are referenced by manifest path, never redrawn.

## 0. Where things are

| Need | Path |
|---|---|
| Every asset, with sha1 | `manifest.json` (generated; edit `assets_map.json` then `python3 tools/build_assets.py`) |
| Canonical tokens (colour, gradients, type, grid, radius) | `brands/worldfirst/tokens.json` → `tokens.css` |
| Checkable rules (37, ids COL/TYP/LOG/ARC/PRT/ICO/GFX/PHO/CPY/AFA) | `brands/worldfirst/rules.json` |
| Browsable Brand Center | `index.html` (regenerate: `python3 tools/build_index.py`) |
| Fonts + @font-face | `shared/fonts/fonts.css` (Poppins 18 styles, Alibaba PuHuiTi 5) |
| Guideline PDFs, page PNGs, extracted text | `guidelines/pdf/`, `guidelines/pages/<slug>/`, `guidelines/<slug>.md` |
| Original drops, untouched | `00_intake/<drop>/` |
| Drop zone for new files or brand-team feedback | `_inbox/` → `python3 tools/ingest.py` |
| Guard reports | `_guard/` (`python3 tools/guard.py <file|folder>`) |
| Change history and feedback log | `CHANGELOG.md`, `_feedback/feedback_log.json` |
| Web design language (BEC Figma DLS index, staging captures) | `~/Documents/Claude/WFxWD_DLS/` (built by /wf_dls; tokens here import its type scale) |
| Sponsorship compliance (AFA / Messi / Alipay+) | `/afa_kit`, `~/Documents/Claude/AFA_Brand_Kit/` (wins where it conflicts) |
| Copy rules | `/wf_copy_base` |

Brands: `worldfirst` (complete for this drop) · `ant-international` (fonts only; mark lives inside co-brand lockups) · `alipay-plus`, `antom`, `bettr` (stubs).

## 1. Brand core (WorldFirst)

- **A&I vision:** to be the most innovative and trusted digital partner to bring inclusive growth to all.
- **A&I mission:** to make it easy to do business anywhere, bringing small and beautiful changes to the world.
- **WF brand promise:** Connecting the world through one global account.
- **WF master tagline (exact):** `One Account. Global Reach.`
- **Personality:** Real (genuine, clear, human; makes the complex feel simple) · Dependable (consistent, reliable, always there) · Energising (ambitious, optimistic, forward-moving).
- **Parent line (exact):** `a brand of Ant International` (only via the lockup file when shown as a mark).
- Source: `brands/worldfirst/01_brand-core/wf_brand-house_2026.png`.

## 2. Logo

Files in `brands/worldfirst/02_logo/` (SVG master + PNG preview each):

| id | file | use |
|---|---|---|
| wf-logo-en-hrz-pos | `wf_logo_en_hrz_pos.svg` | default, light grounds |
| wf-logo-en-hrz-rev | `wf_logo_en_hrz_rev.svg` | white, dark or red grounds |
| wf-logo-en-vrt-pos / -rev | `wf_logo_en_vrt_*.svg` | stacked, square spaces |
| wf-logo-cn-hrz-pos / -rev | `wf_logo_cn_hrz_*.svg` | 万里汇 + World First, CN markets |

Rules: never typeset "WorldFirst" as a logo (LOG-05) · never recolour, stretch or add effects; the belt gradient #7D0042→#FF0051→#FF882A stays (LOG-04) · positive on light, reverse on dark (LOG-02) · minimum 24 px tall on screen and clear space = height of the W (both PROVISIONAL until the logo guideline is dropped).

## 3. Colour

Core palette (pattern guideline p3): **WF Red #FF0051** · WF Dark Purple #13002D · WF Purple #32006E · WF Grey #484F56 · WF Black #1F2323 · WF Light Grey #ECEDEE · WF White #FFFFFF.
Restricted: Enterprise #BC0050 (For Enterprise only) · Ant blue #1677FF (inside Ant International co-brand lockups only).
Extended web palette (BEC Figma): Coral 100–600, Pink 050/100, Violet 500–700, Lilac 100, Orange #FF882A, Yellow #FFE41E, Neutrals 050–950; button hover #EB004B, pressed #E50049.

Gradients (top-left to bottom-right): Red #FF0051→#13002D (70/30) · Light Grey #FFFFFF→#ECEDEE (30/70) · Purple #32006E→#13002D (70/30) · Grey #484F56→#1F2323 (70/30). Belt ribbon: #FF0051→#FF882A.

**WF Red must be present in every composition** (background, graphic or text accent). No second accent colour. No cream.

## 4. Typography

- **EN:** Poppins. Headlines Extrabold 800, negative tracking on H1 (−1 px) and H2 (−3 px). Body Regular/Medium 18 px desktop (Body M) or 16 px (Body S). Buttons Medium 16 px.
- **CN:** Alibaba PuHuiTi. Headings **Bold 700, never Extrabold/Heavy** (BEC rule).
- Scale, grid (1440/1232/1184), spacing and radius: `tokens.json` (imported from BEC's Figma DLS). Fonts: `shared/fonts/fonts.css`.
- No serif companion, no system fonts as a design choice.

## 5. Brand architecture

`brands/worldfirst/05_brand-architecture/`: "a brand of Ant International" lockup (pos/rev) · Ant International | WorldFirst parent-and-pillar lockup (pos/rev) · WorldFirst × Alipay co-brand EN and CN (pos/rev) · WorldFirst For Enterprise horizontal (rev SVG; pos in `ai/wf_enterprise_hrz.ai` page 1) and vertical (pos/rev). Always the file, never assembled from parts (ARC-01). Enterprise mark only on enterprise content and never beside the standard wordmark (ARC-02).

## 6. Partnership lockup

Templates in `brands/worldfirst/06_partnership-lockup/` (ai masters + png pages). Construction (PRT-01): partner logo **left**, WorldFirst brandmark **right**, "+" between, both at a matched maximum height, optional description line beneath (sport). Multi-partner: partners in a row on the left with grey divider bars, WorldFirst right. Enterprise partnerships use the For Enterprise mark. CN versions use the CN logo.

## 7. Iconography

14 icons × 4 variants in `brands/worldfirst/07_iconography/svg/<variant>/wf_icon_<name>_<variant>.svg` (+ png 256 px). Names: collect-payments, send-payments, convert-payments-fx, manage-payments (World Account capabilities) · all-in-one, secure, fast-payments, fast-set-up (value proposition) · e-commerce, trade-import-export, freelancers, software-app-developers, banks, vcc (representations). Variants: primary (WF Red, light grounds) · reverse-white (dark grounds) · duotone (WF Red + WF Purple, light grounds) · red-circular (white on a WF Red disc, 48 px). Spec: 32 px grid, 2 px padding, 2 px stroke, round cap and join. One variant per surface. No third-party icon sets (ICO-01).

## 8. Photography

Six principles (`guidelines/wf_photography_guidelines.md`): real people and genuine interactions · warm natural light, no high contrast or oversaturation · business in action (packing, inventory, deliveries; scale and detail) · local vibrancy (markets, landmarks, crafts) · business diversity (trading shops, e-commerce merchants, enterprises) · moments of connection · hero the WorldFirst Red as a visual cue in key visuals. No approved photo library in this drop.

## 9. Brand graphics and backgrounds

`brands/worldfirst/09_brand-graphics/`: dot world map and globe on the red gradient (ai masters, png 3840 and 1600). Background families (pattern guideline): gradient only · full map pattern · map with belt · map overlay on belt · globe. Pairings p10–11: on red/purple grounds white main text and white supporting pill; on light grey ground dark text and WF Red pill; on grey ground white text and WF Red pill. The belt sweeps in from a lower corner, WF Red into Orange, one per surface, never behind body text. Belt vector is a gap (only inside the PDF).

## 10. Copy (short form; full rules in /wf_copy_base)

Tagline exact. No em-dashes. No exclamation marks in body. Avoid: game-changing, utilise, in today's world, seamless, revolutionise, world-class, cutting-edge, best-in-class. British English. Confident, clear, human.

## 11. Compliance hand-offs

Argentina / AFA / Messi / Alipay+ sponsorship content: `/afa_kit` rules apply on top of this file. Web pages that must match production worldfirst.com: `/wf_site`. The 2026 revamp: `/wf_dls`.

## 12. Gaps (stubs until dropped)

Logo guideline (clear space, min size, misuse) · colour guideline (tints, accessibility, CMYK/Pantone) · typography guideline as published · brand core beyond the house · Ant International master logo · belt vector · 3D coin/product visuals · photo library · brand application, demand gen, website templates · Alipay+, Antom, Bettr kits · BEC's Brand Agent rule set.

## 13. Keeping it current

New files or brand-team feedback → `_inbox/` → `/brand_kit ingest` (or `python3 tools/ingest.py`) → confirm the proposed `assets_map.json` entries → `python3 tools/build_assets.py` → update tokens/rules/BRAND.md → `python3 tools/tokens_css.py && python3 tools/build_index.py` → log in `CHANGELOG.md` and `_feedback/feedback_log.json`.
