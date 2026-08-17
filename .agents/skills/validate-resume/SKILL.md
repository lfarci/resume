---
name: validate-resume
description: Validate factual accuracy and the parser and visual quality of this repository's one-page LaTeX resume
---

# Validate the Resume

This repository uses LaTeX, embedded fonts, a small portrait, and an
established one-page visual hierarchy. Do not replace it with generic Word
resume rules.

## 1. Factual audit

Before building, audit every resume claim against the canonical `docs/`
source. `data/` supports the build but does not override `docs/`.

Explicitly verify:

- employment titles and dates
- Avanade corporate grade versus functional role
- technologies and certifications
- metrics and their approximation qualifiers
- team contribution versus individual ownership
- outcomes
- skill and exposure claims

Flag every claim that is unsupported, stronger than the canonical notes, more
precise than the canonical notes, or inconsistent with `docs/`. Ask for
evidence or remove the claim; do not silently reconcile a disagreement in
favour of `data/`.

A successful LaTeX/PDF build establishes neither factual correctness nor
claim accuracy. Complete this audit before parser, layout, and ATS-oriented
validation.

## 2. Build, parser, and visual validation

After the factual audit passes, check the following acceptance criteria:

- The generic master resume is one A4 page.
- Typography, hierarchy, whitespace, and the established design remain clear
  and readable.
- Important information exists as real text, not only in an image.
- PDF text extraction succeeds and has sensible section and chronology order.
- There is no clipping, overflow, or visual regression.
- After any layout change, a human reviews `resume-preview.png`.

## Validation

Run:

```bash
node scripts/build-resume.mjs --output build/resume
```

The build validates the A4 page, selectable text, required content, and
creates `build/resume/resume-preview.png`. Review that preview after layout
changes. Do not commit anything under `build/`.

ATS-oriented review is qualitative: confirm real text, recognizable section
headings, sensible reading order, and natural supported terminology. Do not
present an ATS or keyword-match percentage as an objective result.
