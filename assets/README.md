# assets — provenance

Visuals for the repository README only. None of this is copied into a project that adopts Prefrontal Context: the five markdown files are the whole artifact.

| File | What it is |
| --- | --- |
| `logo-mark.svg` | The Prefrontal Context mark |
| `five-files.svg` | Figure A — the five files, one job each, and who maintains them |
| `session-loop.svg` | Figure B — one session and the next, as a four-step loop |
| `social-preview.png` | The GitHub social preview card (1200×630) |

## `logo-mark.svg`

The owner-supplied artwork, unmodified. It is recoloured to the Clean Proof palette — the brain in proof ink `#f0ece0`, the circuit traces and nodes in live-channel amber `#c47b2b` — by `scripts/build-mark.mjs` in `itsabk/prefrontal-dev`, which also emits that project's favicon and apple touch icon from the same geometry. Nothing in the file is redrawn here.

`sha256 71a617388026929df698357cbf6bd303eea1974dd417146be77adf216c300700`

## The two figures

Hand-authored SVG, written in the tokens the site uses: ground `#0a0908` painted inside each figure so it reads the same on GitHub's light and dark themes, ink `#f0ece0`, soft `#d4cec0`, dim `#bab2a1`, amber `#c47b2b only as the ownership dot, hairlines at 13% and 22%, 6.4px container radius, no shadows and no gradients.

They hold to constraints that make them survive a README:

- Presentation attributes only — no `<style>`, no script, no external reference, no embedded font — so GitHub's sanitizer and its image proxy serve them unchanged.
- System font stacks (`ui-monospace` / `system-ui` and their fallbacks), because a font cannot be loaded inside an image. Text is left-anchored and the tiles carry slack, so a wider fallback face does not collide.
- A 620-unit canvas with a 20-unit type floor, which is about 11–12px at the 343px column a phone gives a README image.

`five-files.svg sha256 6d20559245c96f21f5307cc9d75efc022762eca40ae6dabac38869eb85814d92`
`session-loop.svg sha256 35c2d35f3443feb300acbfcd801d209ee80f3cce6fbd0f4ab7a73b51384175d6`

Every text fill clears WCAG AA on the surface it sits on. Measured: `#f0ece0` 16.8:1, `#d4cec0` 12.7:1 and `#bab2a1` 9.5:1 on the ground, and no worse than 9.2:1 on a row wash.

To look at a figure without a browser, render it through headless Chrome:

```sh
chrome --headless --screenshot=out.png --window-size=880,1200 "file://$PWD/assets/five-files.svg"
```

## `social-preview.png`

The product's own social card, not a new composition: it is a screenshot of `prefrontal-dev`'s `/og-card` export at 1200×630 (`public/og.png` at commit `247449d`), copied here so a shared link to this repository shows the same card the site publishes. To change it, change `src/pages/og-card.astro` in that project, re-shoot `public/og.png` there, and copy the file here.

`sha256 95f3fd18d8b54326a34e1db9dcc077d3aaaa677bf755c6495dd553529c18d91e`

GitHub has no API for the repository social preview: upload this file by hand at **Settings → Social preview**.
