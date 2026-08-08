# AWL - Deploy Node.js PM2

## Purpose

Reusable composite action to deploy Node.js applications using PM2.

---

## Features

- SSH Authentication
- Copy Deployment Package
- Extract ZIP Package
- Install Dependencies
- Build Application
- PM2 Start
- PM2 Reload
- PM2 Save
- PM2 Startup
- Deployment Validation
- GitHub Step Summary

---

## Supported Applications

- Express.js
- NestJS
- Fastify
- Koa
- Hapi
- Socket.IO
- Next.js (Standalone)
- Any Node.js PM2 Application

---

## Inputs

| Input | Default | Description |
|--------|---------|-------------|
| host | - | Linux VM Host |
| username | - | SSH Username |
| ssh-private-key | - | SSH Private Key |
| package-path | - | Deployment Package |
| target-path | - | Deployment Folder |
| package-manager | npm | npm / yarn / pnpm |
| install-command | ci | Dependency Install |
| build-command | build | Build Script |
| ecosystem-file | ecosystem.config.js | PM2 Ecosystem File |
| app-name | - | PM2 Application Name |
| clean-target | true | Clean Deployment Folder |

---

## Outputs

| Output | Description |
|--------|-------------|
| deployment-status | Deployment Status |

---

## Prerequisites

- Linux VM
- OpenSSH Server
- Node.js Installed
- PM2 Installed
- unzip Installed
- SSH Key Authentication

---

## Example

```yaml
- name: Deploy Node PM2

  uses: ./.github/actions/awl-deploy-node-pm2

  with:

    host: 10.0.0.20

    username: azureuser

    ssh-private-key: ${{ secrets.VM_SSH_KEY }}

    package-path: artifact

    target-path: /opt/apps/node-api

    app-name: node-api
```

---

## Used By

- awl-deploy-node-pm2.yml

---

## Version History

| Version | Description |
|----------|-------------|
| v1.0 | Initial Release |

---

## Maintainer

AWL DevOps Team