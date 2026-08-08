# AWL - Deploy Linux VM

## Purpose

Reusable composite action to deploy applications to Linux Virtual Machines over SSH.

---

## Features

- SSH Authentication
- Backup Existing Deployment
- Clean Target Folder
- Copy Deployment Package
- Extract ZIP Package
- Restart Linux Service
- Execute Post Deployment Command
- Validate Service
- GitHub Step Summary

---

## Supported Applications

- .NET
- Java
- Node.js
- Python
- PHP
- Static Website
- Docker (Non-Kubernetes)

---

## Inputs

| Input | Default | Description |
|--------|---------|-------------|
| host | - | Linux VM Host |
| username | - | SSH Username |
| ssh-private-key | - | SSH Private Key |
| package-path | - | Deployment Package |
| target-path | - | Target Deployment Folder |
| backup-enabled | true | Backup Existing Deployment |
| backup-path | /opt/backup | Backup Folder |
| clean-target | true | Clean Deployment Folder |
| extract-package | true | Extract ZIP Package |
| service-name | Empty | Linux Service Name |
| post-deploy-command | Empty | Custom Command |

---

## Outputs

| Output | Description |
|--------|-------------|
| deployment-status | Deployment Status |

---

## Prerequisites

- Linux VM
- OpenSSH Server
- SSH Key Authentication
- unzip Installed
- systemd Service (Optional)

---

## Example

```yaml
- name: Deploy Linux VM
  uses: ./.github/actions/awl-deploy-linux-vm
  with:
    host: 10.0.0.10
    username: azureuser
    ssh-private-key: ${{ secrets.VM_SSH_KEY }}
    package-path: artifact
    target-path: /opt/apps/myapp
    service-name: myapp
```

---

## Used By

- awl-deploy-linux-vm.yml

---

## Version History

| Version | Description |
|----------|-------------|
| v1.0 | Initial Release |

---

## Maintainer

AWL DevOps Team