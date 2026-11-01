# Nikita's Tower

A 3D résumé: a red-brick tower at sunrise. The intro sits on a rooftop billboard,
and each section has its own side of the building, with posters stacked down that wall.
A formation of pixel swallows dives behind the billboard, leaving contrails.

## Run it
Open `index.html` in a browser, or serve the folder with any static host:

    python3 -m http.server 8000      # then open http://localhost:8000

No build step. three.js r128 is bundled in `vendor/`, so only the Google Fonts
(DM Serif Display, IBM Plex Sans, IBM Plex Mono) load from the network.

## What's inside
| Path | What it is |
|---|---|
| `index.html` | The whole site: markup, styles, 3D scene, résumé data |
| `vendor/three.min.js` | three.js r128 (MIT, see `three-LICENSE.txt`) |
| `content/resume.md` | The résumé as plain text, section by section |
| `content/technical-assignment.md` | The design brief for the site, based on the original description |
| `content/resume.json` | Same content as structured data |
| `assets/swallow-sprite.png` | 8-frame swallow strip, 32×33 px per frame (navy silhouette) |
| `assets/swallow-sprite@4x.png` | Same strip enlarged for viewing |
| `assets/source/` | Original swallow sheet and palette reference |
| `assets/preview-*.png` | Screenshots (rendered with fallback fonts) |

## Editing content
All text lives in the `SECTIONS`, `INTRO`, `CONTACT` and `LINKS` objects near the top of the
script in `index.html`. Posters and the plain-text section below the scene are both
generated from them. Content is transcribed from `backend_engineer.html`, including contact details, employment history, achievements and education. `LINKS` defines the clickable contact, repository and certificate links in the text résumé.

Sections link by hash: `#profile`, `#backend`, `#ml`, `#experience`, `#contact`.

## Published site

Main website: https://sfill.github.io/

The header downloads `assets/nikita-kalgushkin-resume.pdf`, copied from the supplied `backend_engineer.pdf`. Links on the 3D posters use native anchors projected over the matching text and support mouse, touch and keyboard.

## Publishing

Edit this repository on `master`. The `Publish main website` workflow copies only `index.html`, `.nojekyll`, the résumé PDF, and the bundled three.js files to the `my-newyork-building` branch of `SFill/sfill.github.io`. GitHub Pages serves that branch at https://sfill.github.io/. You can also run the workflow manually from Actions.

Authentication uses the `PAGES_DEPLOY_KEY` Actions secret and a write-enabled deploy key scoped to `SFill/sfill.github.io`. No personal access token is stored in the workflow.

The previous homepage is preserved on [`archive/pre-tower-2026-11-01`](https://github.com/SFill/sfill.github.io/tree/archive/pre-tower-2026-11-01). Its original `master` and `gh-pages` branches are retained. To restore the old homepage, choose `master` and `/ (root)` under the destination repository’s Settings → Pages.
