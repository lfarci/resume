---
name: validate-resume
description: Validate the repository's one-page LaTeX resume for parser and visual quality
---

# Validate the Resume

This repository uses LaTeX, embedded fonts, a small portrait, and an
established one-page visual hierarchy. Do not replace it with generic Word
resume rules.

## Acceptance criteria

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
