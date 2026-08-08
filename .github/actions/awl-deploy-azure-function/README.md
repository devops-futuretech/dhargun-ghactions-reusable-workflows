# AWL - Deploy Azure Function

## Purpose

Reusable composite action to deploy Azure Function Apps.

---

## Features

- Validate Function App
- ZIP Deployment
- Run From Package Deployment
- Linux Startup Command
- Deployment Verification
- Deployment Summary

---

## Supported Hosting

- Windows Function App
- Linux Function App
- Consumption Plan
- Premium Plan
- Dedicated App Service Plan

---

## Inputs

| Input | Default | Description |
|--------|---------|-------------|
| resource-group | - | Azure Resource Group |
| function-app-name | - | Function App Name |
| package-path | - | Deployment Package |
| deployment-method | zip | zip / run-from-package |
| startup-command | Empty | Linux Startup Command |

---

## Outputs

| Output | Description |
|--------|-------------|
| deployment-status | Deployment Result |
| deployment-method | Deployment Method |

---

## Prerequisites

- Azure CLI
- OIDC Login
- Downloaded Artifact
- Self-hosted Runner

---

## Used By

- awl-deploy-azure-function.yml

---

## Version History

| Version | Description |
|----------|-------------|
| v1.0 | Initial Release |

---

## Maintainer

AWL DevOps Team