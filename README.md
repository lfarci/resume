# Resume

This repository contains an ATS-friendly, one-page LaTeX resume. Canonical career context lives in the private [`lfarci/notes`](https://github.com/lfarci/notes) repository under `career/`. Structured records in `data/` support the build and must remain consistent with those notes.

The source hierarchy is: `lfarci/notes/career/` (canonical context) → `data/`
(structured verified facts) → `sections/` (curated wording) → `resume.tex`
(presentation/layout) → generated PDF (build artifact).

## Repository layout

- `resume.tex` defines the page, typography, colors, header, and portrait.
- `sections/` contains the resume content.
- [`lfarci/notes/career/`](https://github.com/lfarci/notes/tree/main/career) contains the canonical career context and [resume-authoring guidance](https://github.com/lfarci/notes/blob/main/career/personal-brand/resume-authoring.md). Access to this private repository is required for factual editing.
- `data/` contains structured employment, education, certification, and skills records selected from verified facts; reconcile them against `lfarci/notes/career/`.
- `.agents/skills/` contains repository-local Codex workflows for resume analysis, tailoring, writing, formatting, and ATS review.
- `fonts/` and `images/` contain the embedded visual assets.
- `.github/actions/build-resume/` contains the reusable build action and its
  Node.js build script.

## CI build

`.github/workflows/build-resume.yml` is the canonical build path. It runs on pushes and pull requests affecting resume inputs, validates the PDF, and uploads the `resume-pdf` artifact containing `resume.pdf` and `resume-preview.png`. The preview is a 150 DPI first-page PNG for layout review. Validation runs before upload, so a failed build or invalid PDF cannot produce an artifact.

## Local build

### Install prerequisites

Install the following tools and ensure their commands are available on your
`PATH`:

- [Node.js](https://nodejs.org/) 20 or later.
- [Tectonic](https://tectonic-typesetting.github.io/) for compiling the LaTeX
  source.
- [Poppler](https://poppler.freedesktop.org/) utilities: `pdfinfo`, `pdftotext`,
  and `pdftoppm`. On Linux, these are commonly provided by the `poppler-utils`
  package.

Verify the installation from the repository root:

```bash
node --version
tectonic --version
pdfinfo -v
pdftotext -v
pdftoppm -v
```

### Build and validate

From the repository root, run:

```bash
node .github/actions/build-resume/build-resume.mjs --output build/resume
```

The command creates:

- `build/resume/resume.pdf` — the one-page A4 résumé.
- `build/resume/resume-preview.png` — a 150 DPI preview of the first page for
  layout review.

It validates that the PDF has selectable text, is exactly one A4 page, and
contains the required headings, dates, certifications, and technical keywords.
Review the PNG after layout changes before sharing the PDF.

If the build reports that `tectonic`, `pdfinfo`, `pdftotext`, or `pdftoppm` is
missing, install the corresponding prerequisite above and open a new terminal
before retrying. The generated `build/` directory is reproducible output and
must not be committed.

## Website PDF update PR

`.github/workflows/update-website-resume.yml` runs after a successful
**Build Resume** push build on the default branch (`master` today). It can also
be run manually from Actions once merged, to pick up the latest existing build.
It downloads that run's validated `resume-pdf` artifact and replaces only
`src/public/resume.pdf` in `lfarci/loganfarci.com`. It opens or updates one draft
PR on `automation/update-resume`, with source commit and artifact links.
No PDF difference means no new PR. It never merges or deploys changes.

One-time setup: create a fine-grained GitHub token restricted to
`lfarci/loganfarci.com`, with **Contents: Read and write** and
**Pull requests: Read and write**. Store it as the Actions secret
`WEBSITE_RESUME_TOKEN` in **this resume repository**. The normal `GITHUB_TOKEN`
only reads this repository and its build artifacts; it cannot write to the website.
No private-notes access or workflow-write permission is needed. Missing or expired
credentials cause an explicit failure; rotate the token when needed.

Only default-branch push builds qualify; PR/fork builds never supply the PDF.
The latest push build must have succeeded: an older PDF is not used if a newer
build is queued, running, or failed. Older completion events are ignored. Runs
are serialized to avoid concurrent branch updates. A missing/expired artifact
fails without changing the website; rerun **Build Resume** on the default branch,
then rerun this workflow if necessary. Artifacts currently expire after 30 days.

Review the PDF and preview from the linked source build before approving the
website PR. Generated commits contain `[skip ci]` because website PRs otherwise
automatically deploy previews. This also skips website CI; run the approved checks
before merging. Keep `[skip ci]` out of the final squash commit so the normal
website production deployment runs. Verify the hosted `/resume.pdf` afterward.

## Privacy boundary

This repository is **public**, while `lfarci/notes` is **private**. The notes are for authorized, local factual review only. Never commit, vendor, download into tracked files, upload as CI artifacts, or publish private notes or their unreviewed excerpts. The public resume must contain only deliberately selected and reviewed career facts. CI must build exclusively from this repository's checked-in public inputs; it must not receive a token or checkout permission for the private notes repository.
