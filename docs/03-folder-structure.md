# AWL GitHub Enterprise Reusable Workflows

# 03 - Repository Folder Structure

---

# Overview

The repository is organized into logical folders that separate reusable workflows, composite actions, documentation, examples, and utility scripts.

This modular structure improves maintainability, scalability, and discoverability.

---

# Repository Layout

```text
.
│
├── .github
│   ├── actions
│   └── workflows
│
├── docs
│
├── examples
│
├── scripts
│
├── README.md
├── CHANGELOG.md
└── LICENSE
```

---

# Folder Description

| Folder | Purpose |
|---------|----------|
| .github/actions | Composite Actions |
| .github/workflows | Reusable Workflows |
| docs | Technical Documentation |
| examples | Sample Consumer Workflows |
| scripts | Utility Scripts |
| README.md | Repository Overview |
| CHANGELOG.md | Version History |
| LICENSE | Repository License |

---

# .github Folder

The `.github` folder contains the automation components.

```text
.github

├── actions
└── workflows
```

---

# Composite Actions

Location

```text
.github/actions/
```

Composite actions provide reusable building blocks for workflows.

Example

```text
.github/actions/

awl-setup-node

awl-setup-dotnet

awl-upload-artifact

awl-download-artifact

awl-azure-login

awl-health-check

awl-deployment-summary

awl-deploy-appservice

awl-deploy-aks
```

Each composite action contains

```text
action.yml

README.md
```

---

# Reusable Workflows

Location

```text
.github/workflows/
```

Reusable workflows orchestrate one or more composite actions.

Example

```text
awl-build-react.yml

awl-build-dotnet.yml

awl-build-java.yml

awl-build-python.yml

awl-build-node.yml

awl-build-php.yml

awl-build-flutter-android.yml

awl-build-firebase.yml

awl-deploy-appservice.yml

awl-deploy-aks.yml

awl-deploy-linux-vm.yml
```

---

# Documentation

Location

```text
docs/
```

Contains technical documentation for the platform.

Example

```text
01-overview.md

02-architecture.md

03-folder-structure.md

04-composite-actions.md

05-build-workflows.md

06-deploy-workflows.md

07-authentication-oidc.md

08-supported-technologies.md

09-runner-requirements.md

10-versioning.md

11-best-practices.md

12-troubleshooting.md
```

---

# Examples

Location

```text
examples/
```

Contains reference implementations demonstrating how application repositories consume reusable workflows.

Example

```text
examples/

react/

node/

dotnet/

java/

python/

php/
```

---

# Scripts

Location

```text
scripts/
```

Contains reusable utility scripts.

Example

```text
scripts/

bash/

powershell/
```

Typical use cases include:

- Validation
- File manipulation
- Deployment helpers
- Build helpers

---

# Composite Action Structure

Every composite action follows a standard layout.

```text
awl-action-name/

action.yml

README.md
```

---

# Workflow Structure

Reusable workflows follow a consistent structure.

```yaml
Workflow Header

↓

Inputs

↓

Secrets

↓

Permissions

↓

Jobs

↓

Composite Actions

↓

Outputs
```

---

# Naming Standards

Composite Actions

```text
awl-setup-node

awl-upload-artifact

awl-health-check

awl-deploy-aks
```

Reusable Workflows

```text
awl-build-react.yml

awl-build-python.yml

awl-deploy-appservice.yml

awl-deploy-linux-vm.yml
```

---

# Repository Growth

Future enhancements should follow the existing folder structure.

Example

```text
.github/actions/

awl-build-docker

awl-release

awl-cleanup

awl-notification
```

without modifying the existing architecture.

---

# Best Practices

- Keep workflows technology-specific.
- Keep composite actions small and reusable.
- Store documentation under the `docs` folder.
- Store sample implementations under the `examples` folder.
- Avoid adding application-specific logic.
- Follow naming conventions consistently.

---

# Summary

The repository structure is designed to:

- Improve discoverability
- Encourage reuse
- Reduce maintenance
- Support enterprise scalability
- Provide a consistent development experience

---

# Version

Current Version

**v1.0.0**