# HERMES — Harmonised Fire Observation Intelligence

**David Idemudia Odigie & [Godwin Enendu](https://github.com/Enendugodwin)**

A publication page describing how HERMES turns NASA MODIS and VIIRS thermal detections into one
defensible fire record: association-scored harmonisation, coverage-aware calendars, and a verified
storage layer (FireSeal) that proves every payload it keeps.

**Recognition:** second place, NASA International Space Apps Challenge 2026 (Nigeria); advancing to
the global category.

Live: <https://odigiedavididemudia.github.io/hermes-publication/>

The page is a single self-contained `index.html` — CSS in a `<style>` block, one small theme-toggle
script, no build step and no framework. Images are the only external assets, plus Google Fonts.

## Contents

| Path | What it is |
| --- | --- |
| `index.html` | The publication page |
| `assets/` | Three WebP figures captured from the running console (< 200 KB each) |
| `design/publication-standard.json` | The design standard this page was built against |
| `.nojekyll` | Serve the folder as-is on GitHub Pages |

## Design

Built to `design/publication-standard.json`: neobrutalism structure × minimalism restraint,
Space Grotesk / Inter / JetBrains Mono, amber accent (`#B45309` light, `#F59E0B` dark) reserved for
section numerals, links and focus, a hard offset shadow on the hero frame and figures only, and both
colour schemes implemented with a persisted manual override.

## Data

Every figure in the prose comes from the live store over **2026-10-16 → 2026-11-14**:

- 333,441 detections; 59,272 MODIS / 274,169 VIIRS
- 7,224 candidate pairs scored → 326 probable, 2,047 possible, 4,851 rejected
- 3,056 estimated events; 241 observed by both sensors
- 13 of 30 days with source coverage; 17 without availability
- 250,157 harmonised detections of 333,441 at world zoom
- FireSeal: 182 blocks, 333,834 payloads, 88.4 MB JSONL → 7.9 MB (11.2×)

Detections are thermal anomalies, not confirmed wildfires.

## Local preview

```bash
python -m http.server 8302
# http://127.0.0.1:8302/
```
