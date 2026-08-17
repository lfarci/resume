# Current Avanade Engagement

## Current Avanade Engagement — Azure / DevOps Platform

### Context

Started approximately **December 2023**.

Public-sector client.

Do not disclose the client name.

The organization operates a hybrid architecture.

For regulatory/legal reasons, the primary end-user production architecture remains largely hosted in private datacenters.

A significant collection of development, testing, pre-production and selected production workloads are hosted in Azure.

The platform team provisions and maintains those Azure environments.

---

## Current Functional Role

Logan works as a **DevOps / platform engineer**.

The broader team has approximately ten people and is roughly divided into two areas:

1. Project/support activities helping development teams that require environments.
2. Platform engineering activities building and maintaining the automated deployment platform.

Logan primarily belongs to the platform-oriented group.

The platform is currently mainly used internally by operators/platform engineers.

Do **not** describe it as a fully-fledged developer self-service platform or internal developer portal.

---

## Azure Deployment Architecture

The solution automates Azure infrastructure using:

- Terraform
- GitHub Actions

There are manually pre-existing Azure hub environments.

The Terraform deployment architecture is separated into multiple layers, including:

- foundational networking and security
- optional Azure Red Hat OpenShift deployment
- administration resources
- resources with independent lifecycles around the cluster or standalone environments, including:
  - Azure VMs
  - Storage Accounts
  - databases
  - supporting Azure resources

Important:

The Kubernetes platform used here is:

> **Azure Red Hat OpenShift (ARO)**

Do **not** replace this with AKS.

The architecture is configuration-driven so deployments can vary according to client/project requirements.

---

## Current Platform Scale

Approximate but defensible scale:

- ~20 active Azure environments
- 30+ Terraform resource modules
- multiple reusable solution-level deployment topologies
- 50+ GitHub Actions workflows

Approximate GitHub Actions breakdown:

- ~10 reusable actions
- ~20 reusable workflows
- ~30 orchestration / manually or automatically triggered workflows

Terraform also includes approximately:

- 30 resource-oriented modules
- ~5 reusable solution-level compositions/topologies
- several utility/convention modules

These numbers are approximate and should not be made artificially precise.

Safe wording:

> Contributed to a reusable Terraform platform comprising 30+ resource modules and multiple solution-level topologies, orchestrated through 50+ GitHub Actions workflows.

Use **contributed to**, not wording implying sole creation or ownership.

---

## Bicep to Terraform Migration

When Logan joined the engagement, portions of the platform had been implemented in **Bicep**.

The team decided shortly afterwards to migrate toward Terraform.

Logan:

- participated in the migration from Bicep to Terraform
- had prior basic Bicep experience from personal Azure projects
- significantly contributed to Terraform module implementation and design
- collaborated with more senior technical leads and architects
- contributed to the ARO deployment/configuration implementation
- built and maintained reusable Azure resource modules
- contributed to modules related to areas such as:
  - Azure VMs
  - Azure Communication Services / email-related resources
  - RBAC / role-related resources
  - other Azure resources
- continues to maintain and troubleshoot modules

He also works on module lifecycle and release management within the monorepo:

- versioning
- tags/releases
- Git references between dependent modules
- documentation

He implemented automated documentation generation based on Terraform variables and outputs and contributed internal documentation.

Do **not** present Logan as the sole architect of the Terraform platform.

---

## GitHub Actions Engineering

GitHub Actions is one of Logan's strongest areas.

He has built or contributed to:

- reusable workflows
- composite/reusable actions
- at least one JavaScript GitHub Action
- Terraform plan workflows
- Terraform apply workflows
- security checks
- Azure operations
- configuration-generation workflows
- deployment orchestration

A major part of his contribution is configuration-driven orchestration.

The system can:

1. Generate initial deployment configuration.
2. Generate/import Azure role configuration.
3. Use configuration to determine:
   - whether ARO is required
   - which deployment layers are required
   - which supporting resources should be deployed
4. Orchestrate the relevant Terraform workflows.

This configuration-driven automation is one of the strongest technical accomplishments from the engagement.

---

## Provisioning Impact

Before the automated platform, provisioning an ARO environment involved substantial manual work, including Azure Portal operations and manually coordinating infrastructure dependencies.

Depending on missing inputs and dependencies, deployment could take several days.

Estimated previous duration:

- roughly 2–3 days under reasonable conditions
- potentially approaching 5 days / one working week when dependencies or missing information caused delays

This was **not formally instrumented**.

Do not convert these numbers into an invented percentage improvement.

Manual deployment also had significant operational complexity:

- networking had to be configured correctly
- peering/security dependencies had to be remembered
- missing inputs created back-and-forth
- updates and cleanup were difficult
- delete/recreate operations required significant manual work

With the automated Terraform/GitHub Actions platform, once required prerequisites and networking/security inputs are available:

#### ARO environment

Approximately:

> **~1 hour end-to-end**

Azure provisioning itself can be slightly shorter.

#### VM-oriented environment

Approximately:

> **~20 minutes**

#### ARO cleanup / teardown

Approximately:

> **~1 hour**

depending on Azure.

The more important impact is not only speed.

The platform makes deployments:

- repeatable
- standardized
- configuration-driven
- easier to maintain
- less dependent on operator memory
- easier to update
- easier to destroy/recreate
- less error-prone

Operational knowledge is encoded into Terraform and GitHub Actions instead of existing mainly as manual procedures.

Strong potential resume statement:

> Helped replace a multi-day manual ARO provisioning process with a configuration-driven Terraform and GitHub Actions platform capable of deploying an operational environment in approximately one hour once prerequisites are available.

Do not claim a specific percentage reduction.

---

## Security and Reliability Contributions

### Self-Hosted GitHub Actions Runners

Self-hosted runners operate on Azure VMs because deployments require access to private Azure networking/resources.

### Managed Identity

Azure VMs use **user-assigned managed identities** for Azure deployment operations.

This reduces dependence on traditional long-lived credentials.

### Azure RBAC

Permissions are assigned where required.

Terraform modules also assign appropriate roles to deployed resources.

### Key Vault

Azure Key Vault is used within the platform.

### GitHub Security and Deployment Protection

The platform uses:

- GitHub secrets
- environment secrets
- GitHub environment protection rules

### Pull Request Validation

Logan contributed to PR-triggered infrastructure validation.

### IaC Security Scanning

**Trivy** is currently used for IaC/security checks.

Validation occurs before Terraform apply.

### Terraform Plans

Terraform plan mechanisms exist, but plan enforcement is **not currently mature/stable enough to describe as a fully enforced deployment gate**.

Do not claim that every deployment is currently protected by mandatory Terraform plan approval.

### Azure Policy

The client uses Azure Policies for broader governance and security.

These policies are managed outside Logan's team.

Do **not** credit Logan with implementing them.

---

## Software Engineering Discipline Applied to IaC

One of Logan's differentiators on the current engagement is that he entered an infrastructure-oriented team with a strong software-development background.

When he joined, repository/process conventions were relatively inconsistent.

The team progressively introduced stronger engineering practices such as:

- pull request templates
- clearer Terraform conventions
- repository organization
- code quality expectations
- automated testing
- security checks
- versioning and releases
- reusable modules
- documentation
- GitHub Copilot instructions

Logan contributed substantially to bringing software-development discipline into Infrastructure as Code.

Important career narrative:

> Logan did not move from development into DevOps by abandoning software engineering. He applies software-engineering practices to cloud and infrastructure platforms.

---

## GitHub Copilot on the Current Engagement

The client uses GitHub Enterprise and GitHub Copilot.

The Terraform monorepo contains categories such as:

- resources
- utilities
- solution-level compositions

The team uses:

- repository-level custom instructions
- scoped/module-specific custom instructions
- custom agents

Agent roles include areas such as:

- development
- QA
- debugging
- documentation
- solution/project overview generation

Project feedback and recurring knowledge can be incorporated into instructions so conventions become reusable context for future work.

### Ownership Nuance

This is important.

Logan should **not** be described as having single-handedly designed or introduced the complete Copilot agent architecture.

The broader custom-agent architecture was significantly bootstrapped by a Microsoft colleague / technical lead.

Logan's contribution includes:

- being an early driver of custom-instruction usage within the team
- actively contributing to their evolution
- maintaining/updating instructions while working on modules
- creating/contributing specialized agents
- contributing a documentation-oriented agent
- contributing an overview-generation agent
- contributing to debugger-oriented functionality
- using the system intensively for real Terraform delivery

Safe framing:

> Advanced GitHub Copilot adoption through repository and scoped custom instructions, contributed specialized agents, and embedded project conventions into AI-assisted Terraform development.

Avoid:

> Introduced GitHub Copilot custom agents to the team.

---

## Concrete Copilot Productivity Example

Using the Copilot/custom-instruction setup, Logan was able to create a new Terraform module in approximately one afternoon.

The work included:

- implementation
- project conventions
- testing
- documentation
- supporting implementation/plan materials

This represented a substantial perceived productivity improvement.

However:

> There is no formally measured percentage improvement.

Do not invent metrics such as:

- 40% faster
- 2× productivity
- 60% reduction in development time

unless real measurements become available later.

---

## Client-Facing / Consulting Responsibilities

Logan is in frequent direct contact with the client.

Activities include:

- daily meetings
- weekly status reporting
- technical discussions
- requirement/prioritization discussions
- interaction with networking/security teams when necessary
- documentation
- troubleshooting support
- backlog/planning activities

Approximately every four months, Logan travels onsite to the client in **France** for around two days of planning.

During these sessions the team discusses:

- upcoming work
- priorities
- backlog items
- next-period planning

Because Logan works full-time on the platform and understands much of the implementation, operators frequently contact him when deployments or automation fail.

Typical issues include:

- missing GitHub environment configuration
- incorrect branch/workflow usage
- workflows referencing outdated shared module versions
- configuration mistakes

He can investigate and resolve many of these issues quickly because of his detailed understanding of the platform.

He also proactively improves documentation when repeated operator mistakes reveal missing knowledge or unclear procedures.

This supports Consultant-level positioning:

> Technical ownership + client interaction + operational responsibility

rather than simply executing assigned tickets.

---

## Promotion to Consultant

Promotion occurred in:

> **December 2025**

It recognized growing autonomy and ownership rather than a sudden technical role switch.

Important contributing factors included:

### Current Client Engagement

- strong technical contribution
- design participation
- proactive problem solving
- client-facing responsibilities
- increasing autonomy

### Internship Leadership

- leading internal internship projects
- coordinating across teams
- Scrum responsibilities
- mentoring

### Professional Development

- Azure Developer Associate certification
- continued development despite client workload and internship responsibilities

The resume does not need to explicitly say:

> Promoted because of...

The level of responsibilities and outcomes should make the progression credible.

---
