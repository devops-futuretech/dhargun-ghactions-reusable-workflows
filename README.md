# AWLABL GitHub Actions Reusable Workflows
## Overview
This repository contains the enterprise reusable GitHub Actions workflows used across the AWLABL GitHub Enterprise Organization.
The objective is to standardize CI/CD implementation by centralizing build, deployment, infrastructure, validation and security workflows.
Application repositories should never duplicate workflow logic. Instead, they should reference reusable workflows from this repository.
---
# Repository Purpose
This repository provides reusable workflows for:
- Application Build
- Application Deployment
- Infrastructure Deployment
- Security Validation
- Quality Gates
- Runner Validation
- Branch Validation
- Artifact Management
---
# Supported Platforms
- Azure
- AWS (Future)
- Google Cloud (Future)
---
# Supported Technologies
- .NET
- Java
- Node.js
- Python
- Docker
- Kubernetes
- Terraform
---
# Repository Structure
```text
.github/
    workflows/
    actions/
docs/
examples/
schemas/
scripts/

README.md
CHANGELOG.md
CODEOWNERS
LICENSE
.gitignore
```
---
# Workflow Categories
## Build
- awl-build-dotnet.yml
- awl-build-node.yml
- awl-build-java.yml
- awl-build-python.yml
---
## Deployment
- awl-deploy-appservice.yml
- awl-deploy-function.yml
- awl-deploy-aks.yml
---
## Infrastructure
- awl-terraform-plan.yml
- awl-terraform-apply.yml
---
## Validation
- awl-validate-branch.yml
---
## Utility
- awl-utility-runner-health.yml
---
# Workflow Versioning
Application repositories must reference released workflow versions.
Example
```yaml
uses: AWLABL/awl-ghactions-reusable-workflows/.github/workflows/awl-build-dotnet.yml@v1
```
Never reference:
```yaml
@main
```
---
# Configuration Strategy
Reusable workflows never contain:
- Resource Names
- Subscription IDs
- Resource Groups
- Web App Names
- Secrets

All configuration is provided through GitHub Variables, Secrets and Environments.
---
# Environment Strategy
Deployments automatically consume configuration from GitHub Environments.
Development
↓
UAT
↓
Production
No workflow changes are required between environments.
---
# Documentation
Additional implementation guides are available under:
```text
docs/
```
---
# Current Status
Repository Foundation Completed
Reusable Workflow Development In Progress
