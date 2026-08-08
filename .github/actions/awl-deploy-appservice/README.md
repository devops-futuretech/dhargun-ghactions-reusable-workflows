# AWL - Deploy Azure App Service

## Purpose

Reusable composite action to deploy application packages to Azure App Service.

---

## Features

- Validate Azure App Service
- ZIP Deployment
- WAR Deployment
- JAR Deployment
- Run From Package Deployment
- Optional Startup Command
- Deployment Slot Support
- Slot Swap Support
- Deployment Summary

---

## Supported Applications

- .NET
- .NET Framework
- Node.js
- React
- Angular
- Vue
- Java WAR
- Java JAR
- Python
- PHP

---

## Inputs

| Input | Default | Description |
|--------|---------|-------------|
| resource-group | - | Azure Resource Group |
| app-name | - | Azure App Service Name |
| package-path | - | Package Path |
| deployment-method | zip | zip / war / jar / run-from-package |
| use-slot | false | Deploy to Slot |
| slot-name | staging | Deployment Slot |
| swap-slot | false | Swap Slot |
| target-slot | production | Swap Target |
| startup-command | Empty | Linux Startup Command |

---

## Outputs

| Output | Description |
|--------|-------------|
| deployment-status | Deployment Result |
| deployment-method | Deployment Type |

---

## Prerequisites

- Azure CLI Installed
- Azure Login Completed
- OIDC Authentication
- Artifact Downloaded
- Self-hosted Runner

---

## Example

```yaml
- name: Deploy Azure App Service
  uses: ./.github/actions/awl-deploy-appservice
  with:
    resource-group: rg-dev
    app-name: webapp-dev
    package-path: artifact
    deployment-method: zip
```

---

## Used By

- awl-deploy-appservice.yml

---

## Version History

| Version | Description |
|----------|-------------|
| v1.0 | Initial Release |

---

## Maintainer

AWL DevOps Team