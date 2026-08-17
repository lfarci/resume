# Resume authoring

This repository contains the curated LaTeX resume. The factual source of truth is in `data/`; resume content may select and concisely rewrite those facts but must not contradict dates, credentials, or skills.

Use `node scripts/build-resume.mjs --output build/resume` to generate and validate the PDF. Generated output under `build/` must not be committed.
