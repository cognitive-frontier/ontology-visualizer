# Personality System Ontology Visualizer

**Live site:** https://cognitive-frontier.github.io/ontology-visualizer/

An interactive 3D map of how seven personality frameworks divide up the same territory: Socionics (Model A / Model G, Reinin, DCNH), Attitudinal Psyche / Psychosophy / ARM-24, the Enneagram, the Fisher Temperament Inventory, Attachment theory, Cybernetic Big Five Theory, and a Neurotyping placeholder.

## What you are looking at

- **Seven strata** stack from the neurochemical substrate (S1 Affective / Basal) up to narrative identity (S7 Integrative / Narrative). Each stratum is a glass plate.
- **Each framework is a translucent spindle.** Its width at a stratum is how much of that stratum the framework claims; where spindles cross, their claims overlap.
- **Click a spindle** to open that framework's native geometry in place:
  - Socionics: the 16-type tesseract, edges coloured by intertype relation, quadras as cosets
  - Attitudinal Psyche: the order-4 permutohedron (24 configurations), sextas as colour classes
  - Enneagram: the enneagon with hexad and triangle lines, instinct shells as rings
  - Fisher: the tetrahedron of the four neurochemical systems
  - Attachment: the anxiety × avoidance plane
  - Neurotyping: a projected pentachoron (placeholder for the Neurotype Matrix)
- **Click a node** to inspect a type: Model A stack, AP positions and ARM assignment, passions and subtypes, Big Five and ACPS vectors, and every cross-framework mapping that touches it.
- **Manifold** embeds every type with a published or proxy Big Five vector on the Agency, Plasticity and Communion axes (CB5T frame); the slider rotates Stability into the third axis.
- **Lenses:** Fibers (cross-framework mappings), Attractor lens (the four attractor signatures), Generative bands (L1–L4 of the generative model), plus a Constructs index of shared constructs across frameworks.

Controls: drag to orbit, scroll or pinch to zoom, `Esc` goes up a level, `/` focuses search. Light and dark themes.

## Evidence and status

Every cross-framework mapping carries an evidence class — `empirical`, `author`, `community`, `structural`, `user-hypothesis`, or `claude-hypothesis` — and a confidence value. Several links are explicitly hypotheses awaiting review rather than demonstrated findings; the data block records them as such. Ontology data version `2.2-cb5t`.

## How it is built

A single self-contained `index.html`: three.js r128 (loaded from cdnjs) with custom GLSL for the glass strata and glow, hand-rolled orbit controls, and the entire ontology inlined as JSON in the `<script id="ontology" type="application/json">` block. No build step and no dependencies to install. View state (theme, lenses, manifold slider) is kept in `localStorage` only.

To update the site, replace `index.html` on `main`; GitHub Pages redeploys automatically. To read or reuse the data, parse the JSON block directly.

## Related

- [Socionics Ontology](https://cognitive-frontier.github.io/socionics-ontology/)
- [Socion Tesseract](https://cognitive-frontier.github.io/socion-tesseract/)
- [Sociotype Attractors](https://cognitive-frontier.github.io/attractor-basins/)
- [Integrated Element Lattice](https://cognitive-frontier.github.io/integrated-elements/)
- [Intertype Relations](https://cognitive-frontier.github.io/intertype-relations/)
