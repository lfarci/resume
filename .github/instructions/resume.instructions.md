---
applyTo: "resume.tex,sections/**/*,data/**/*,fonts/**/*,images/**/*,scripts/*.mjs,.github/workflows/build-resume.yml"
---

# Resume instructions

- Treat `data/` as the factual source of truth for employment dates, education, certifications, and skills.
- `resume.tex` and `sections/` contain the curated CV: they may select, prioritize, and concisely rewrite facts, but must not introduce contradictory dates or credentials.
- Build with the documented non-interactive Node.js/Tectonic command; never commit generated PDFs or build output.
- Keep the LaTeX output ATS-readable: real text, standard section headings, conventional dates, and no text embedded in images.
