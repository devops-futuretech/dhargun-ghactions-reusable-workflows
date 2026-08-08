# AWLABL Reusable Workflow

## Workflow Name

awl-build-dotnet.yml

---

# Purpose

Build and publish a .NET application using a standardized enterprise reusable GitHub Actions workflow.

This workflow is intended to be called from application repositories using `workflow_call`.

---

# Supported Technologies

- .NET 8
- .NET 9 (Future)
- ASP.NET Core
- Console Applications
- Web API
- Worker Service

---

# Supported Repository Types

- Single Repository
- Monorepo
- Microservice Repository

---

# Workflow Flow

```text
Caller Workflow
        │
        ▼
Checkout Source
        │
        ▼
Display Build Context
        │
        ▼
Setup .NET SDK
        │
        ▼
Restore Packages
        │
        ▼
Build Solution
        │
        ▼
Publish Application
        │
        ▼
Upload Artifact
        │
        ▼
Return Outputs
```

---

# Inputs

| Input | Required | Description |
|---------|----------|-------------|
| runner-label | No | Self-hosted runner label |
| environment | Yes | GitHub Environment |
| solution-path | Yes | Solution or Project file |
| working-directory | No | Working directory |
| build-configuration | No | Release / Debug |
| artifact-name | Yes | Artifact name |
| upload-artifact | No | Upload artifact |

---

# Outputs

| Output | Description |
|---------|-------------|
| artifact-name | Published artifact name |
| artifact-path | Publish folder path |

---

# Organization Variables

Required

| Variable | Description |
|-----------|-------------|
| DOTNET_VERSION | .NET SDK Version |

---

# Repository Variables

Optional

BUILD_CONFIGURATION

---

# Secrets

None

Build workflow does not require secrets.

---

# GitHub Environment

Supported

- Development
- UAT
- Production

---

# Artifact

Default Publish Folder

```text
publish/
```

Retention

30 Days

---

# Example

See

```text
examples/dotnet/caller-build-dotnet.yml
```

---

# Version History

| Version | Changes |
|----------|----------|
| v1.0 | Initial Version |

---

# Future Enhancements

- Unit Test Support
- Code Coverage
- SonarQube
- SBOM Generation
- Code Signing
- Container Build