---
name: tailor-resume
description: Tailor this repository's LaTeX resume to a job using only supported evidence
---

# Tailor the Resume

Use after `analyze-job` when adapting the resume to a specific role. `lfarci/notes/career/`
is canonical; `data/` is supporting build input only. `AGENTS.md` overrides
this skill.

## Guardrails

- Keep employment history reverse chronological unless the user explicitly
  requests a non-chronological structure.
- Preserve official titles, chronology, confidence qualifiers, Avanade
  corporate-grade versus functional-role distinctions, and team versus
  individual ownership.
- Add a job-description term only when the source notes support the underlying
  experience. Better wording is allowed; new facts are not.
- Never add team sizes, department counts, budgets, users, percentages,
  monetary figures, dates, scale, performance figures, technologies,
  certifications, or ownership without verified support.
- Use documented quantitative evidence when available. Never manufacture,
  infer, extrapolate, or conservatively estimate a metric; ask for it or use
  the strongest accurate qualitative outcome.

## Tailoring sequence

1. Start with the job evidence matrix.
2. Select and reorder the headline, summary, skills, certifications, projects,
   and bullets by relevance.
3. Reorder bullets within a role before removing supported evidence for space.
4. State every addition, removal, and wording change for review.
5. Keep the generic master resume architecture unless the user asks for a
   targeted variant.

## Private-source boundary

This repository is public; `lfarci/notes` is private. Authorized agents may consult private notes for factual verification, but must never copy full private notes, confidential client details, unreviewed excerpts, private file contents, or credentials into this repository, prompts shared publicly, logs, CI artifacts, PR descriptions, or the generated PDF. Do not add CI access, tokens, automated checkout, or synchronization of private notes. Publish only explicitly selected and reviewed career facts. If the private source is unavailable, flag the claim as unverified rather than fetching or reconstructing it through unsafe means.
