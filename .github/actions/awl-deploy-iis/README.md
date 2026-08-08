# AWL - Deploy IIS

## Purpose

Reusable composite action to deploy applications to Microsoft IIS.

---

## Features

- Validate IIS Website
- Validate Application Pool
- Stop Website
- Stop Application Pool
- Backup Existing Website
- Clean Target Folder
- Copy Deployment Files
- Start Application Pool
- Start Website
- Validate Deployment
- GitHub Step Summary

---

## Supported Applications

- ASP.NET Framework
- ASP.NET Core IIS
- React IIS
- Angular IIS
- Vue IIS
- Static Website
- PHP IIS

---

## Inputs

| Input | Default | Description |
|--------|---------|-------------|
| site-name | - | IIS Website Name |
| app-pool | - | IIS Application Pool |
| package-path | - | Deployment Package |
| physical-path | - | IIS Physical Path |
| backup-enabled | true | Backup Existing Website |
| backup-path | D:\IISBackups | Backup Folder |
| clean-target | true | Clean IIS Folder Before Deployment |

---

## Outputs

| Output | Description |
|--------|-------------|
| deployment-status | Deployment Status |

---

## Prerequisites

- Windows Self-hosted Runner
- IIS Installed
- WebAdministration PowerShell Module
- Website Created
- Application Pool Created
- Downloaded Artifact

---

## Example

```yaml
- name: Deploy IIS

  uses: ./.github/actions/awl-deploy-iis

  with:

    site-name: MyWebsite

    app-pool: MyWebsitePool

    package-path: artifact

    physical-path: D:\Websites\MyWebsite
```

---

## Used By

- awl-deploy-iis.yml

---

## Version History

| Version | Description |
|----------|-------------|
| v1.0 | Initial Release |

---

## Maintainer

AWL DevOps Team