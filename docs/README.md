# Career Notes

## Purpose

These notes are the current factual and contextual source of truth for
maintaining Logan Farci's resume and related career materials.

The resume itself should remain concise, ideally one page for the
generic/master version. These notes intentionally contain more detail than
should appear in the final resume.

When generating resume content:

- Never invent metrics, responsibilities, technologies, ownership, or outcomes.
- Prefer concrete engineering outcomes over generic claims.
- Do not turn team contributions into individual ownership.
- Distinguish technologies genuinely used from technologies only studied or explored.
- Preserve the distinction between official corporate grade and functional role.
- Tailored resumes may change emphasis and wording, but facts must come from these notes.
- Approximate metrics may be used when defensible, but must not be made artificially precise.

## Navigation

- [Profile](profile.md) — positioning, timeline, skills, credentials, education, and languages.
- [Current engagement](current-engagement.md) — Avanade Azure/DevOps platform work and its claim guardrails.
- [Prior experience](prior-experience.md) — Smals plus the Avanade banking and energy assignments.
- [Leadership and projects](leadership-and-projects.md) — internships, internal expertise, and personal/open-source work.
- [Resume authoring](resume-authoring.md) — resume strategy, tailoring, metrics, and claim rules.

## Structured Data

The Markdown notes above are the current authority. The structured records in
`data/` are useful resume inputs but may need a later reconciliation; that
work is deliberately out of scope for this organization change.

## Repository Recommendation

The resume should live in a central private repository.

Suggested structure:

```text
resume/
├── README.md
│
├── context/
│   ├── career-context.md
│   ├── projects.md
│   ├── certifications.md
│   └── facts.md
│
├── src/
│   ├── resume.tex
│   ├── sections/
│   └── styles/
│
├── variants/
│   ├── master/
│   ├── cloud-devops/
│   ├── software-engineering/
│   └── github-ai/
│
├── output/
│   └── resume.pdf
│
└── .github/
    └── workflows/
