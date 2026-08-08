# AWL GitHub Enterprise Reusable Workflows

# 06 - Deployment Workflows Reference

---

# Overview

Deployment workflows provide standardized Continuous Deployment (CD) pipelines for supported deployment targets.

Each deployment workflow follows a consistent architecture while implementing platform-specific deployment logic through reusable composite actions.

---

# Common Deployment Flow

All deployment workflows follow the same execution pattern.

```text
Download Artifact
        │
        ▼
Authenticate
        │
        ▼
Deploy
        │
        ▼
Validate
        │
        ▼
Health Check
        │
        ▼
Deployment Summary
```

---

# Common Characteristics

| Feature | Supported |
|----------|-----------|
| Reusable Workflow | ✅ |
| Composite Actions | ✅ |
| Artifact Download | ✅ |
| OIDC Authentication | ✅ (Azure) |
| Health Check | ✅ |
| Deployment Summary | ✅ |
| GitHub Environment | ✅ |

---

# Supported Deployment Workflows

| Workflow | Target Platform | Authentication | Health Check |
|-----------|----------------|----------------|--------------|
| awl-deploy-appservice.yml | Azure App Service | Azure OIDC | Yes |
| awl-deploy-azure-function.yml | Azure Function | Azure OIDC | Yes |
| awl-deploy-iis.yml | Windows IIS Server | WinRM / SMB | Optional |
| awl-deploy-linux-vm.yml | Linux VM | SSH | Optional |
| awl-deploy-node-pm2.yml | Linux VM (PM2) | SSH | Optional |
| awl-deploy-firebase-hosting.yml | Firebase Hosting | Firebase CLI | Yes |
| awl-deploy-firebase-functions.yml | Firebase Functions | Firebase CLI | Yes |
| awl-deploy-aks.yml | Azure Kubernetes Service | Azure OIDC | Yes |
| awl-deploy-powerbi.yml | Power BI Service | Microsoft Entra ID | Optional |

---

# Standard Workflow Structure

Every deployment workflow follows the same structure.

```text
Workflow Header

↓

workflow_call

↓

Inputs

↓

Secrets

↓

Permissions

↓

Download Artifact

↓

Authentication

↓

Deployment

↓

Health Validation

↓

Deployment Summary
```

---

# Standard Inputs

| Input | Purpose |
|--------|----------|
| environment | GitHub Environment |
| artifact-name | Deployment Artifact |
| enable-health-check | Enable Health Validation |
| health-url | Application Health Endpoint |

Platform-specific deployment workflows expose additional deployment inputs.

---

# Standard Outputs

| Output | Description |
|---------|-------------|
| deployment-status | Deployment Result |

---

# Authentication

## Azure

Authentication is performed using OpenID Connect (OIDC).

Composite Action

```text
awl-azure-login
```

Supported by

- Azure App Service
- Azure Function
- Azure Kubernetes Service

---

## Linux Virtual Machine

Authentication

SSH Private Key

---

## IIS

Authentication

Windows credentials or deployment account depending on implementation.

---

## Firebase

Authentication

Firebase CLI using service account or CI token.

---

## Power BI

Authentication

Microsoft Entra ID Service Principal.

---

# Artifact Management

Every deployment workflow downloads the application package using:

```text
awl-download-artifact
```

The deployment workflow never rebuilds the application.

---

# Health Validation

Where supported, deployments may execute an application health check after deployment.

Composite Action

```text
awl-health-check
```

Typical validation includes:

- HTTP Status Code
- Retry Logic
- Timeout
- Availability Check

---

# Deployment Summary

All deployment workflows publish a standardized deployment summary.

Composite Action

```text
awl-deployment-summary
```

Summary includes:

- Application
- Environment
- Deployment Target
- Version
- Artifact
- Status
- Duration

---

# Platform Overview

## Azure App Service

Purpose

Deploy web applications to Azure App Service.

Authentication

OIDC

Deployment Package

ZIP Package

---

## Azure Function

Purpose

Deploy Azure Functions.

Authentication

OIDC

Deployment Package

ZIP Package

---

## IIS

Purpose

Deploy applications to Microsoft IIS.

Authentication

Windows Credentials

Deployment Package

Published IIS Package

---

## Linux Virtual Machine

Purpose

Deploy applications over SSH.

Authentication

SSH Private Key

Deployment Package

ZIP Package

---

## Node.js PM2

Purpose

Deploy Node.js applications managed by PM2.

Authentication

SSH Private Key

Deployment

PM2 Reload / Restart

---

## Firebase Hosting

Purpose

Deploy static web applications.

Authentication

Firebase CLI

Deployment

Hosting Files

---

## Firebase Functions

Purpose

Deploy Firebase Cloud Functions.

Authentication

Firebase CLI

Deployment

Cloud Functions

---

## Azure Kubernetes Service

Purpose

Deploy Kubernetes workloads.

Authentication

Azure OIDC

Deployment Methods

- Kubernetes Manifest
- Helm Chart

---

## Power BI

Purpose

Deploy Power BI reports and semantic models.

Authentication

Microsoft Entra ID

Deployment Types

- PBIP
- PBIX

---

# Example Consumer Workflow

```yaml
jobs:

  deploy:

    uses: organization/awl-github-enterprise-reusable-workflows/.github/workflows/awl-deploy-appservice.yml@v1

    with:

      environment: PROD

      artifact-name: webapp

      app-name: customerportal
```

---

# Best Practices

- Build once and deploy the same artifact.
- Use GitHub Environments for deployment approvals.
- Prefer OIDC over client secrets.
- Always enable health checks where available.
- Keep deployment workflows platform-specific.
- Publish deployment summaries for every deployment.

---

# Future Enhancements

Potential future workflows include:

- Docker Deployment
- GitHub Release
- Rollback Workflows
- Deployment Notifications
- Blue-Green Deployment
- Canary Deployment

---

# Version

Current Version

**v1.0.0**