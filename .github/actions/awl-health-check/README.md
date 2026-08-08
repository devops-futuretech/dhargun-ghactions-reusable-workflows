# AWL - Health Check

## Purpose

Reusable composite action to validate application health after deployment.

---

## Features

- HTTP Health Check
- Retry Logic
- Configurable Delay
- Configurable Status Code
- Step Summary

---

## Inputs

| Input | Default |
|--------|---------|
| health-url | Required |
| expected-status | 200 |
| retry-count | 10 |
| retry-delay | 15 |

---

## Outputs

| Output |
|---------|
| response-code |

---

## Example

```yaml
- name: Health Check
  uses: ./.github/actions/awl-health-check
  with:
    health-url: https://myapp.azurewebsites.net/health
```

---

## Used By

- awl-deploy-appservice.yml
- awl-deploy-aks.yml
- awl-deploy-iis.yml
- awl-deploy-linux-vm.yml
- awl-deploy-node-pm2.yml
- awl-deploy-firebase-hosting.yml
- awl-deploy-azure-function.yml