# AWL GitHub Enterprise Reusable Workflows

> Enterprise-grade reusable GitHub Actions workflows and composite actions for standardized CI/CD across multiple technologies and deployment platforms.

---

# Overview

The **AWL GitHub Enterprise Reusable Workflows** repository provides a centralized library of reusable GitHub Actions workflows and composite actions that enable development teams to implement standardized, secure, and scalable CI/CD pipelines with minimal configuration.

The repository follows GitHub Enterprise best practices by separating:

- Reusable Workflows
- Composite Actions
- Authentication
- Deployment Standards
- Technology-specific Build Templates

This approach minimizes duplicated pipeline code, simplifies maintenance, and provides a consistent deployment experience across all projects.

---

# Key Features

- Enterprise reusable workflows
- Modular composite actions
- OIDC-based Azure authentication
- Standardized build pipelines
- Standardized deployment pipelines
- Artifact management
- Health validation
- Deployment summary
- Multi-technology support
- GitHub Enterprise ready

---

# Supported Technologies

## Build

| Technology | Supported |
|------------|-----------|
| React | ✅ |
| Node.js | ✅ |
| .NET | ✅ |
| .NET Framework IIS | ✅ |
| Java | ✅ |
| Python | ✅ |
| PHP | ✅ |
| Android (Kotlin) | ✅ |
| Flutter | ✅ |
| Firebase | ✅ |

---

## Deployment

| Platform | Supported |
|----------|-----------|
| Azure App Service | ✅ |
| Azure Functions | ✅ |
| IIS Server | ✅ |
| Linux VM | ✅ |
| Node.js PM2 | ✅ |
| Firebase Hosting | ✅ |
| Firebase Functions | ✅ |
| Azure Kubernetes Service (AKS) | ✅ |
| Power BI | ✅ |

---

# Repository Structure

```text
.
├── .github
│   ├── actions
│   └── workflows
│
├── docs
├── examples
├── scripts
│
├── README.md
├── CHANGELOG.md
└── LICENSE
```

---

# Composite Actions

The repository contains reusable composite actions for common CI/CD operations.

## Runtime Setup

- awl-setup-node
- awl-setup-dotnet
- awl-setup-dotnet-framework
- awl-setup-java
- awl-setup-python
- awl-setup-php
- awl-setup-android
- awl-setup-flutter
- awl-setup-firebase

## Azure

- awl-azure-login
- awl-health-check
- awl-deployment-summary

## Artifact Management

- awl-upload-artifact
- awl-download-artifact

## Deployment

- awl-deploy-appservice
- awl-deploy-azure-function
- awl-deploy-iis
- awl-deploy-linux-vm
- awl-deploy-node-pm2
- awl-deploy-firebase-hosting
- awl-deploy-firebase-functions
- awl-deploy-aks
- awl-deploy-powerbi

---

# Reusable Workflows

## Build Workflows

- awl-build-react.yml
- awl-build-node.yml
- awl-build-dotnet.yml
- awl-build-dotnet-framework-iis.yml
- awl-build-java.yml
- awl-build-python.yml
- awl-build-php.yml
- awl-build-android-kotlin.yml
- awl-build-flutter-android.yml
- awl-build-firebase.yml

---

## Deployment Workflows

- awl-deploy-appservice.yml
- awl-deploy-azure-function.yml
- awl-deploy-iis.yml
- awl-deploy-linux-vm.yml
- awl-deploy-node-pm2.yml
- awl-deploy-firebase-hosting.yml
- awl-deploy-firebase-functions.yml
- awl-deploy-aks.yml
- awl-deploy-powerbi.yml

---

# Authentication

Azure authentication uses **OpenID Connect (OIDC)**.

Benefits include:

- No client secrets stored in GitHub
- Short-lived authentication tokens
- Improved security posture
- Microsoft recommended authentication model
- Simplified secret management

---

# Getting Started

1. Create a GitHub repository for your application.
2. Configure Azure OIDC credentials.
3. Reference the required reusable workflow from this repository.
4. Provide the required inputs and GitHub Environment secrets.
5. Execute the workflow.

---

# Documentation

Detailed documentation is available in the **docs** directory.

- Overview
- Architecture
- Folder Structure
- Composite Actions
- Build Workflows
- Deployment Workflows
- OIDC Authentication
- Runner Requirements
- Best Practices
- Troubleshooting

---

# Versioning

This repository follows **Semantic Versioning**.

Example:

```
v1.0.0
v1.1.0
v2.0.0
```

---

# Future Roadmap

Future enhancements may include:

- Docker Build Workflow
- GitHub Release Workflow
- Notification Workflow
- Cleanup Workflow
- Rollback Workflows
- GitHub Enterprise Template Repository

---

# License

Refer to the LICENSE file for licensing information.

---

# Support

For workflow documentation, examples, and implementation guidance, refer to the documentation available in the `docs` folder.

---

**AWL GitHub Enterprise Reusable Workflows**

Version **1.0.0**