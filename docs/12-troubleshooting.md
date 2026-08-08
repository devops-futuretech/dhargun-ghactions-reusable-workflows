# AWL GitHub Enterprise Reusable Workflows

# 12 - Troubleshooting

---

# Azure Login Failure

## Symptoms

Authentication fails.

Possible Causes

- Incorrect Client ID
- Incorrect Tenant ID
- Incorrect Subscription ID
- Missing Federated Credential

---

# Artifact Not Found

Possible Causes

- Upload step failed.
- Incorrect artifact name.
- Retention period expired.

---

# Health Check Failure

Possible Causes

- Application not started.
- Incorrect health endpoint.
- Firewall restrictions.

---

# Deployment Failure

Possible Causes

- Missing permissions.
- Invalid deployment package.
- Incorrect deployment configuration.

---

# Runner Offline

Possible Causes

- Runner service stopped.
- Network connectivity issue.
- Registration token expired.

---

# OIDC Failure

Possible Causes

- Missing `id-token: write`
- Incorrect Federated Credential
- Missing Azure RBAC assignment

---

# AKS Deployment Failure

Possible Causes

- Namespace missing.
- Invalid manifest.
- Helm chart error.
- Image pull failure.

---

# IIS Deployment Failure

Possible Causes

- Service stopped.
- Permission denied.
- Invalid package.

---

# Linux VM Deployment Failure

Possible Causes

- SSH key invalid.
- PM2 service unavailable.
- Deployment path incorrect.

---

# Power BI Deployment Failure

Possible Causes

- Workspace access missing.
- Authentication failure.
- Invalid report package.

---

# Support Checklist

Before raising an issue, verify:

- Workflow logs
- Runner status
- Azure permissions
- Environment variables
- GitHub secrets
- Artifact availability

---

# Version

Current Version

**v1.0.0**