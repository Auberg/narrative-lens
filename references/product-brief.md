# Narrative Lens — design reference

## Product thesis
Create a polished, desktop-first responsive web prototype for a single-page scroll-driven narrative visualization of exactly 34 AI-generated stories across Indonesia, Japan, Norway, the United States, and Brazil.

Core question: When AI is prompted to tell stories from different national contexts, how different are the stories underneath the surface?

Core argument: Stories appear different by origin and themes, but many converge in narrative shape and resolution. Visualization reveals patterns, while interpretation requires returning to individual stories.

## Experience model
This is one continuous core flow, not a dashboard. One persistent visualization occupies about 70% of desktop width while concise scene copy occupies about 30%. Do not add filters, dashboard cards, navigation modes, tabs, or exploratory controls.

The same 34 story objects remain visually continuous through all seven scenes. Scroll-linked transitions must be deterministic and reversible. No important state may rely on a one-time entrance animation. The intended sequence is:
0. Scattered stories
1. Geographic origin
2. Thematic landscape
3. Narrative shape
4. Resolution map
5. Close comparison
6. Conclusion / return to scattered stories

## Scene requirements
### Scene 0 — Intro
Show 34 simple points in deterministic scattered positions, with subtle floating motion only. Required idea: "34 stories. 5 national contexts. Do they actually tell different stories?"

### Scene 1 — Origin
Fade in a geographically correct flat world map while the same points move simultaneously toward projected country centroids for Indonesia, Japan, Norway, the United States, and Brazil. Use small deterministic jitter. Required idea: "At first glance, they look different."

### Scene 2 — Themes
Fade the map and move points into a triangle with Tradition, Nature, and Community anchors, positioned using normalized traditionFocus, natureFocus, and communityFocus. Country identity remains secondary. Required idea: "The differences go deeper than place."

### Scene 3 — Narrative shape
Align points and unfold each into a smooth spline across Setup, Conflict, Escalation, and Resolution using each story's arc array. Keep all 34 curves visible but subdued and legible; country-average curves may be emphasized. This is the signature moment and deserves the most animation polish. Required idea: "Strip away the setting, and familiar shapes emerge."

### Scene 4 — Resolution map
Collapse curves back to points and reuse the same map. Keep points geographically grouped but encode the four resolution categories: Reconciliation, Restoration, Transformation, Victory. The visual callback must be obvious. Reader-facing statistics: 22 of 34 end in reconciliation or restoration; 33 of 34 have closed endings.

### Scene 5 — Close comparison
Fade all stories except NO_2 and US_4. Move them from the map to the center and show their curves, country, short summary, resolution, and 2–3 cultural markers side by side. Do not use a metric comparison table. Core message: similar structural trajectories can coexist with different settings, symbols, and meanings.

### Scene 6 — Conclusion
Collapse the comparison back into points, briefly return the two stories to the map, restore all stories, fade the map, and return all 34 points to their exact starting cloud positions. Include the conceptually intact "About the data" disclaimer from the PRD. Core idea: patterns guide attention but do not determine what an individual story means.

## Visual direction
Editorial visualization × digital exhibition × research prototype. Use generous whitespace, confident typography, thin map outlines, simple story points, smooth curves, restrained color, minimal labels, and quiet micro-interactions. Avoid dense legends, excessive gradients, glowing particles, high-poly 3D, dramatic cameras, spinning globes, and ornamental UI.

Clarity, reversible motion, and visual continuity outrank decoration. Use SVG/D3-style 2D or 2.5D visuals unless depth materially improves clarity.

## Interaction and accessibility
- Smooth scroll-linked progress with the exact inverse on upward scroll.
- Tooltip is optional and supplementary only: story ID, country, short summary, resolution, and 2–3 annotations.
- Main narrative must work without hover.
- Support keyboard focus, adequate contrast, and prefers-reduced-motion.
- Mobile must preserve all seven scenes; text may move above or below the visualization.
- Provide a subtle progress cue if useful, but do not turn it into navigation modes.

## Data integrity
Use the provided data file at data/narrative_lens_34.json as the source of truth. Load exactly 34 stories and preserve each story's identity across all visual states. Do not imply that this generated sample represents real national storytelling traditions or cultures.

## Deliverable expectation
Produce a polished, browser-viewable concept with a coherent design system and enough working scroll interaction to demonstrate the full seven-scene core flow. Favor a strong composition and credible data visualization over a generic product shell.