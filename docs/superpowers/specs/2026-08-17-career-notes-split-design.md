# Career Notes Split Design

## Goal

Make the authoritative career-and-resume Markdown easier to read and maintain
without changing factual claims, dates, credentials, confidence qualifiers, or
resume-writing guardrails.

## Authority and Scope

- The existing Markdown source is the current factual authority.
- `data/` may be updated separately and is out of scope for this change.
- No resume content or generated build output changes.

## Structure

`docs/career/` will contain the canonical, focused notes:

- `README.md` — navigation and authority statement.
- `profile.md` — professional positioning, career timeline, skills,
  credentials, education, and languages.
- `current-engagement.md` — current Avanade Azure/DevOps engagement,
  responsibilities, evidence, and claim guardrails.
- `prior-experience.md` — Smals plus the Avanade banking and energy
  assignments.
- `leadership-and-projects.md` — internship leadership, internal GitHub and
  Copilot expertise, and personal/open-source projects.
- `resume-authoring.md` — headline, summary, bullet direction, skill design,
  metrics, and tailoring guidance.

`docs/career-resume-source-of-truth.md` will become a short compatibility
index that directs readers to the canonical notes. It will not duplicate the
content.

## Migration Rules

- Move, rather than summarize, existing content under the relevant note.
- Preserve approximate figures and their qualification.
- Keep ownership and claims-to-avoid guidance with the work it qualifies;
  cross-link only where a rule applies across notes.
- Add a clear index so a reader can locate topics without searching every file.

## Validation

- Confirm every top-level source section is represented in exactly one focused
  note, excluding the compatibility index.
- Inspect the resulting index and section headings for clear navigation.
- Run `git diff --check`; no PDF build is needed because no resume inputs
  change.
