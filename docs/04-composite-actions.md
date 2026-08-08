# AWL GitHub Enterprise Reusable Workflows

# 04 - Composite Actions Reference

---

# Overview

Composite Actions are reusable automation modules that encapsulate a specific task and can be invoked by one or more reusable workflows.

The primary objectives are:

- Eliminate duplicated workflow logic
- Standardize common operations
- Simplify workflow maintenance
- Improve modularity

---

# Composite Actions Inventory

| Composite Action | Category | Purpose | Used By |
|------------------|----------|---------|---------|
| awl-setup-node | Runtime | Install and configure Node.js | React, Node, Firebase |
| awl-setup-dotnet | Runtime | Install .NET SDK | .NET |
| awl-setup-dotnet-framework | Runtime | Configure .NET Framework Build Environment | .NET Framework IIS |
| awl-setup-java | Runtime | Install Java JDK | Java |
| awl-setup-python | Runtime | Install Python | Python |
| awl-setup-php | Runtime | Install PHP | PHP |
| awl-setup-android | Runtime | Configure Android SDK | Android |
| awl-setup-flutter | Runtime | Configure Flutter SDK | Flutter |
| awl-setup-firebase | Runtime | Install Firebase CLI | Firebase |
| awl-upload-artifact | Artifact | Upload build artifacts | All Build Workflows |
| awl-download-artifact | Artifact | Download build artifacts | All Deploy Workflows |
| awl-azure-login | Authentication | Authenticate using Azure OIDC | Azure Deployments |
| awl-health-check | Validation | Validate deployed application | Deploy Workflows |
| awl-deployment-summary | Reporting | Publish deployment summary | Deploy Workflows |
| awl-deploy-appservice | Deployment | Deploy Azure App Service | App Service Workflow |
| awl-deploy-azure-function | Deployment | Deploy Azure Functions | Azure Function Workflow |
| awl-deploy-iis | Deployment | Deploy to IIS Server | IIS Workflow |
| awl-deploy-linux-vm | Deployment | Deploy to Linux Virtual Machine | Linux VM Workflow |
| awl-deploy-node-pm2 | Deployment | Deploy Node.js using PM2 | Node PM2 Workflow |
| awl-deploy-firebase-hosting | Deployment | Deploy Firebase Hosting | Firebase Hosting Workflow |
| awl-deploy-firebase-functions | Deployment | Deploy Firebase Functions | Firebase Functions Workflow |
| awl-deploy-aks | Deployment | Deploy Kubernetes Workloads | AKS Workflow |
| awl-deploy-powerbi | Deployment | Deploy Power BI Reports | Power BI Workflow |

---

# Runtime Actions

## Purpose

Runtime setup actions install and configure the required build tools before the build process begins.

Supported runtimes include:

- Node.js
- .NET
- Java
- Python
- PHP
- Android
- Flutter
- Firebase CLI

---

# Artifact Actions

## Upload Artifact

Purpose

- Publish build outputs
- Share artifacts between workflows
- Store deployment packages

Typical Consumers

- All Build Workflows

---

## Download Artifact

Purpose

- Retrieve build artifacts
- Prepare deployment package

Typical Consumers

- All Deployment Workflows

---

# Authentication Actions

## Azure Login

Authentication Method

OpenID Connect (OIDC)

Benefits

- Secretless authentication
- Short-lived tokens
- Microsoft recommended authentication

Consumers

- App Service
- Azure Function
- AKS

---

# Validation Actions

## Health Check

Purpose

Validate application availability after deployment.

Typical Validation

- HTTP Status Code
- Health Endpoint
- Retry Logic
- Timeout Handling

---

# Reporting Actions

## Deployment Summary

Purpose

Generate a standardized GitHub Deployment Summary.

Information includes:

- Application
- Environment
- Version
- Artifact
- Deployment Type
- Runner
- Status
- Duration

---

# Deployment Actions

Deployment actions encapsulate platform-specific deployment logic.

Supported targets:

- Azure App Service
- Azure Functions
- IIS
- Linux VM
- Node.js PM2
- Firebase Hosting
- Firebase Functions
- Azure Kubernetes Service
- Power BI

---

# Composite Action Standards

Every composite action follows the same structure.

```text
action-name/

├── action.yml
└── README.md
```

---

# Design Principles

Each composite action should:

- Perform one responsibility
- Be reusable
- Be platform independent where possible
- Support configurable inputs
- Avoid application-specific logic
- Return meaningful outputs
- Produce consistent logging

---

# Best Practices

- Keep actions modular.
- Validate inputs.
- Avoid hardcoded values.
- Use OIDC for Azure authentication.
- Reuse existing actions whenever possible.
- Keep documentation up to date.

---

# Version

Current Version

**v1.0.0**