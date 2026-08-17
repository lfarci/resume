---
applyTo: "docs/**/*,resume.tex,sections/**/*,data/**/*,fonts/**/*,images/**/*,scripts/*.mjs,.github/workflows/build-resume.yml"
---

# Resume instructions

- Treat `docs/` as the canonical factual and contextual career source of truth. `data/` supports the build and must remain consistent with it; flag a disagreement for reconciliation rather than silently resolving it in favor of `data/`.
- `sections/` contain curated CV wording derived from verified facts, and `resume.tex` contains presentation/layout. Neither may introduce contradictory dates, credentials, technologies, ownership, or outcomes.
- Build with the documented non-interactive Node.js/Tectonic command; never commit generated PDFs or build output.
- Keep the LaTeX output ATS-readable: real text, standard section headings, conventional dates, and no text embedded in images.
