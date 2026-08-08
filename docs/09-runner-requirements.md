# AWL GitHub Enterprise Reusable Workflows

# 09 - Runner Requirements

---

# Overview

Reusable workflows can execute on either GitHub-hosted runners or self-hosted runners.

The recommended deployment model for enterprise environments is to use self-hosted runners for deployment workloads and GitHub-hosted runners for build workloads where organizational policies permit.

---

# Supported Runner Types

| Runner | Build | Deploy | Recommended |
|---------|-------|---------|-------------|
| GitHub Hosted | ✅ | Limited | Development |
| Self Hosted Linux | ✅ | ✅ | Yes |
| Self Hosted Windows | ✅ | ✅ | Yes |

---

# Runner Labels

The following labels are recommended.

## Build Runner

```text
self-hosted

build

linux
```

---

## Deployment Runner

```text
self-hosted

deploy

linux
```

---

## Windows Deployment Runner

```text
self-hosted

deploy

windows
```

---

# Required Software

## Linux Runner

- Git
- Azure CLI
- kubectl
- Helm
- Node.js
- Java
- Python
- PHP
- Docker (if applicable)
- Firebase CLI (if applicable)

---

## Windows Runner

- Git
- PowerShell 7
- Visual Studio Build Tools
- MSBuild
- .NET SDK
- Azure CLI
- IIS Management Tools (if required)

---

# Network Requirements

Deployment runners should have network connectivity to:

- Azure
- GitHub
- Deployment targets
- Package repositories

---

# Security Recommendations

- Use dedicated service accounts.
- Keep runners patched.
- Restrict administrative access.
- Separate build and deployment runners.
- Register runners using runner groups.
- Avoid using personal accounts.

---

# Scaling Recommendations

For larger environments:

- Separate build and deployment runner pools.
- Create dedicated runner groups.
- Monitor runner utilization.
- Remove offline runners.

---

# Version

Current Version

**v1.0.0**