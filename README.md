# Narrative Lens

Single-page editorial data story prototype for the `narrative-lens` repository.

## Project files

- `index.html` — GitHub Pages entry artifact.
- `data/narrative_lens_34.json` — authoritative 34-story dataset.
- `references/product-brief.md` — authoritative product and design reference.
- `OPEN_DESIGN_HANDOFF.md` — confirmed brief and a ready-to-paste continuation prompt.

## Open in OpenDesign

1. Open the existing **Narrative Lens — Polished Web Concept** project, or import this extracted folder as a project.
2. Keep the directory structure intact so `index.html` can load `data/narrative_lens_34.json` by its relative path.
3. Open `index.html` as the project entry artifact and use the OpenDesign preview rather than opening the HTML directly from the filesystem.
4. If you want OpenDesign to continue refining the prototype, paste the prompt in `OPEN_DESIGN_HANDOFF.md` into the project conversation.

The prototype is self-contained and has no external runtime dependencies. It is designed to be served by the OpenDesign project preview so the relative JSON request works correctly.

## GitHub Pages

Push this repository to `https://github.com/Auberg/narrative-lens` and serve it from the repository root. GitHub Pages will use `index.html` as the main page.

## Current implementation

The package contains all seven required scenes, deterministic 34-story positions, reversible scroll-linked transitions, the NO_2/US_4 comparison, responsive layouts, keyboard-focusable story points, reduced-motion support, and dataset integrity checks. The previous automated generation was interrupted during its final validation pass, so a final visual review inside OpenDesign is still recommended.
