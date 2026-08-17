# Leadership and Projects

## Internship Leadership at Avanade

Logan regularly mentors interns, generally during the February–June period.

This responsibility is stronger than casual mentoring.

He has helped run real internal projects, combining:

- technical mentorship
- project coordination
- Scrum responsibilities
- product/scope responsibilities

---

## 2025 Internship Cohort

Approximately:

> **3 interns**

Profiles:

- 2 software developers
- 1 infrastructure/DevOps intern

Internal project:

> **Avanade Support Hub**

The application was a customer-support platform built around Azure Communication Services.

Main functionality included:

- embeddable React widget
- anonymous customer support requests
- support-agent dashboard
- agents accepting conversations
- issue tagging
- skills-based or issue-based routing toward suitable support agents

Technology included:

- .NET backend
- React frontend
- Azure Communication Services
- Terraform
- GitHub workflows

The infrastructure intern focused on Azure deployment using Terraform and GitHub workflows.

### Logan's Responsibilities

- Scrum Master
- technical mentor
- meeting/facilitation responsibilities
- code reviews
- technical guidance
- company/process guidance
- internship defense support

### Outcome

> **2 of the 3 interns were hired.**

Confirmed hires:

- 1 developer
- 1 infrastructure/DevOps profile

This is confirmed and safe to state.

---

## 2026 Internship Cohort

Approximately:

> **4 interns**

Profiles:

- 2 developers
- 1 infrastructure profile
- 1 AI-focused profile

The project extended the Support Hub with AI functionality.

Logan had an even broader role combining:

- Scrum Master
- Product Owner-type responsibilities
- technical mentor

Responsibilities included:

- helping define scope/features
- daily meetings
- planning
- reviews
- retrospectives
- technical guidance
- coordination
- presentations
- internship defense support

He did **not** personally implement all AI functionality.

---

## AI Functionality in the 2026 Internship Project

Technologies included:

- Azure AI Foundry
- deployed language models
- Azure AI Search
- Azure Communication Services
- App Service
- Key Vault
- Storage

Use cases included:

### Support Message Quality Review

An LLM analyzed support-agent messages and could produce structured feedback/tags related to things such as:

- profanity
- rude language
- unhelpful responses

The result could be surfaced in the support dashboard.

### Knowledge Assistance

Knowledge-base content was indexed/searchable.

AI/search functionality could surface relevant information for support agents.

Logan coached the interns and understood the architecture sufficiently to guide them, but was not the principal AI developer.

---

## Internship Totals

Across the two cohorts:

> **7 interns mentored**

Confirmed:

> **2 hires**

Potential/pending:

> Approximately 2 additional hires were expected, but not confirmed.

Safe:

> Mentored seven interns across two engineering cohorts, with two confirmed hires.

Unsafe:

> Mentored seven interns, four of whom were hired.

Do not count expected hires as confirmed.

---

## Internal GitHub / Copilot Expertise

Within his Avanade development practice, Logan and his supervisor are among the more GitHub/DevOps-oriented engineers.

As the organization moved from Azure DevOps toward GitHub, Logan became an active GitHub user and has followed:

- GitHub Actions
- GitHub Copilot
- custom agents
- custom instructions
- GitHub Copilot CLI
- newer agentic development capabilities

---

## GitHub Copilot Training

Logan has been selected to help deliver an internal:

> **GitHub Copilot training in September 2026**

This is upcoming, not completed.

Correct phrasing if included:

> Selected to design and deliver internal GitHub Copilot training.

Do not write:

> Delivered GitHub Copilot training.

until it has actually happened.

The audience is primarily internal development-practice colleagues.

The training is expected to be practical and hands-on.

---

## Personal and Open-Source Projects

Personal projects should not dominate the master one-page resume because Logan already has substantial professional experience.

For tailored GitHub/AI-oriented versions, one or two projects may be useful.

---

## pull-request-quality-checks

Repository:

> `lfarci/pull-request-quality-checks`

This is one of the strongest portfolio projects for Logan's GitHub/agentic engineering positioning.

The project uses:

- GitHub Agentic Workflows / `gh-aw`
- GitHub Copilot
- GitHub Actions / automation

Purpose:

> Automated pull-request quality validation.

When a PR is opened or updated, an agent evaluates the PR against a defined quality contract.

The system can:

- inspect PR metadata/content
- validate predefined quality rules
- post/update a managed PR comment
- block merging when validation fails

Checks include concepts such as:

- conventional PR title
- required PR sections
- motivation/context
- consistency between diff and description
- validation/test evidence
- screenshots where appropriate
- linked issue where appropriate
- assignee
- focused/sufficiently scoped PR

The repository contains concepts such as:

- action
- agent
- skill/contract
- workflow source
- compiled workflow lock

This project is a particularly strong example of:

> Using AI/agents as part of software-engineering quality gates rather than simply generating code.

Before putting strong ownership wording on the resume, confirm how much of the quality contract and workflow architecture was designed entirely by Logan versus derived from an existing example/framework.

---

## Flouz

Repository:

> `lfarci/flouz`

AI-powered personal-finance CLI.

Capabilities include:

- bank CSV import
- local SQLite storage
- AI-assisted transaction categorization
- budget tracking
- spending analysis
- projections/dashboard functionality

AI functionality uses GitHub-hosted model capabilities / GitHub Models.

Privacy design:

- financial data remains local
- only information required for AI categorization is sent to the model provider

Engineering work includes:

- CLI development
- testing
- documentation
- GitHub Actions
- VitePress documentation
- releases
- agent skills

Recent work included substantial budget-management functionality and a large test suite.

Important:

This is a **personal/open-source project**, not a production financial product used by customers.

Do not frame it as a commercial fintech application.

---

## loganfarci.com

Personal website:

> `loganfarci.com`

Repository:

> `lfarci/loganfarci.com`

Technology includes:

- React
- Vite
- TypeScript
- Tailwind
- Azure Static Web Apps
- Terraform
- GitHub Actions
- Playwright
- accessibility testing
- developer tooling

The repository is increasingly used as a laboratory for agentic software-development workflows.

Recent experimentation includes concepts such as:

- specialized agents
- orchestrator agents
- developer/reviewer/finalization workflows
- per-issue sessions/subsessions
- backlog-maintenance agents
- explorer/shaper/prioritizer/writer/reviewer roles
- human approval gates
- GitHub MCP/tool integration
- automated validation
- accessibility automation

Because the website is already linked directly from the resume, it may not require a separate Projects entry.

It is useful as supporting evidence for Logan's interest in:

> Agent orchestration and AI-native software-development workflows.

---

## Our Grocery List

Repository:

> `lfarci/our-grocery-list`

Built approximately at the end of 2025.

Shared grocery-list PWA.

Technology includes:

- React 19
- TypeScript
- Tailwind
- Vite / PWA
- .NET 8 Azure Functions
- Cosmos DB
- Azure SignalR
- Docker Compose
- Playwright E2E
- Azure Static Web Apps
- automated deployments
- PR preview environments

The application was genuinely deployed to Azure and used by Logan and his partner for several months.

### Unique Project Story

The main value is not the grocery-list domain.

Logan built it as an experiment in **agentic development**.

While frequently on the move and using an iPad, he experimented with:

- GitHub coding-agent sessions
- voice input/dictation
- managing development work from an iPad
- letting agents perform a large proportion of implementation

The application was nevertheless real, deployed, maintained for a period and used regularly.

Do **not** call this `low-code`.

That term would incorrectly imply tools such as PowerApps or no-code platforms.

Better description:

> AI-assisted / agentic development experiment.

Potential story:

> Built and shipped an Azure application using GitHub coding agents as the primary implementation workflow, experimenting with voice-driven development from an iPad.

This may be excellent interview/article/talk material.

It may be too niche for the generic one-page resume unless space permits.

---

## Other GitHub Repositories

### my-agentic-workflows

Interesting experimentation around:

- agents
- skills
- agentic workflows
- MCP
- GitHub workflows

Currently not documented enough to be recruiter-friendly.

Do not use as a primary resume project yet.

### github-copilot-playground

Primarily experimentation/training.

Not a resume project.

### copilot

Learning repository around GitHub Copilot/.NET.

Not a resume project.

### azure

Learning/study repository around Azure certification.

Not a resume project.

### bicep-github-actions

Useful technical sample around:

- GitHub Actions
- Bicep
- what-if/deploy
- Checkov
- OIDC
- environment approvals

However, it appears closer to a learning/sample project.

Do not highlight unless original contribution/ownership is clarified.

---

## Project Selection Strategy

For the generic one-page resume:

> **Do not force a large Projects section.**

Professional experience is strong enough to carry the resume.

If space permits, use at most one or two compact projects.

For GitHub / agentic / AI-enabled development positions, likely strongest:

1. `pull-request-quality-checks`
2. `flouz`

For cloud/full-stack variants:

- `our-grocery-list` can demonstrate a complete Azure application
- its agentic development story is what makes it distinctive

`loganfarci.com` is already linked in the header and can act as portfolio evidence.

---
