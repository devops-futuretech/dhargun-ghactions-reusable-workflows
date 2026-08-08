# AWL - Azure Login

## Purpose

Reusable composite action to authenticate with Azure.

---

## Features

- Azure OIDC Login
- Subscription Validation
- Azure CLI Verification
- Step Summary

---

## Inputs

| Name | Required |
|------|----------|
| client-id | Yes |
| tenant-id | Yes |
| subscription-id | Yes |

---

## Outputs

| Name |
|------|
| subscription-id |

---

## Example

```yaml
- name: Azure Login

  uses: ./.github/actions/awl-azure-login

  with:

    client-id: ${{ secrets.AZURE_CLIENT_ID }}

    tenant-id: ${{ secrets.AZURE_TENANT_ID }}

    subscription-id: ${{ secrets.AZURE_SUBSCRIPTION_ID }}
```