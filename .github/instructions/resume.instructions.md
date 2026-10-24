---
applyTo: "resume.tex,sections/**/*,data/**/*,fonts/**/*,images/**/*,scripts/*.mjs,.github/workflows/build-resume.yml"
---

# Resume instructions

- Treat `lfarci/notes/career/` as the canonical factual and contextual career source of truth. `data/` supports the build and must remain consistent with it; flag a disagreement for reconciliation rather than silently resolving it in favor of `data/`.
- `sections/` contain curated CV wording derived from verified facts, and `resume.tex` contains presentation/layout. Neither may introduce contradictory dates, credentials, technologies, ownership, or outcomes.
- Build with the documented non-interactive Node.js/Tectonic command; never commit generated PDFs or build output.
- Keep the LaTeX output ATS-readable: real text, standard section headings, conventional dates, and no text embedded in images.

## Private-source boundary

This repository is public; `lfarci/notes` is private. Authorized agents may consult private notes for factual verification, but must never copy full private notes, confidential client details, unreviewed excerpts, private file contents, or credentials into this repository, prompts shared publicly, logs, CI artifacts, PR descriptions, or the generated PDF. Do not add CI access, tokens, automated checkout, or synchronization of private notes. Publish only explicitly selected and reviewed career facts. If the private source is unavailable, flag the claim as unverified rather than fetching or reconstructing it through unsafe means.
