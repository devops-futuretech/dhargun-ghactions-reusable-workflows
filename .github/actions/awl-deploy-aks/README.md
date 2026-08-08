# AWL - Deploy AKS

## Purpose

Reusable composite action to deploy applications to Azure Kubernetes Service.

---

## Features

- Get AKS Credentials
- Namespace Validation
- Namespace Creation
- Kubernetes Manifest Deployment
- Helm Deployment
- Image Override
- Rollout Validation
- Deployment Verification
- GitHub Step Summary

---

## Supported Deployment Types

- Kubernetes YAML Manifest
- Helm Chart

---

## Inputs

| Input | Default | Description |
|--------|---------|-------------|
| resource-group | - | Azure Resource Group |
| aks-name | - | AKS Cluster |
| namespace | default | Kubernetes Namespace |
| deployment-type | manifest | manifest / helm |
| manifest-path | k8s | Manifest Folder |
| helm-chart-path | chart | Helm Chart |
| release-name | app | Helm Release |
| values-file | values.yaml | Helm Values |
| image-name | Empty | Override Image |
| image-tag | Empty | Override Image Tag |
| wait-timeout | 300s | Rollout Timeout |

---

## Outputs

| Output | Description |
|--------|-------------|
| deployment-status | Deployment Result |

---

## Prerequisites

- Azure CLI
- kubectl
- Helm
- Azure Login Completed
- AKS Cluster Exists

---

## Example

```yaml
- name: Deploy AKS

  uses: ./.github/actions/awl-deploy-aks

  with:

    resource-group: rg-dev

    aks-name: aks-dev

    namespace: dev

    deployment-type: helm
```

---

## Used By

- awl-deploy-aks.yml

---

## Version History

| Version | Description |
|----------|-------------|
| v1.0 | Initial Release |

---

## Maintainer

AWL DevOps Team