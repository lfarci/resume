# Resume

This repository contains an ATS-friendly, one-page LaTeX resume. Canonical
facts live in `data/`, while `resume.tex` and `sections/` contain the
curated presentation.

## Repository layout

- `resume.tex` defines the page, typography, colors, header, and portrait.
- `sections/` contains the resume content.
- `data/` contains structured employment, education, certification, and skills records; it may require later reconciliation with the canonical Markdown notes.
- `docs/` contains the current career and resume source of truth, organized as focused, navigable notes.
- `fonts/` and `images/` contain the embedded visual assets.
- `scripts/` builds and validates the generated PDF.

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
node scripts/build-resume.mjs --output build/resume
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

A consumer workflow can download the named artifact with `actions/download-artifact`:

```yaml
- uses: actions/download-artifact@v6
  with:
      name: resume-pdf
      path: public
```

The personal website can consume this artifact without duplicating the resume
source or build toolchain.
