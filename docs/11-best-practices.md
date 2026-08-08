# AWL GitHub Enterprise Reusable Workflows

# 11 - Best Practices

---

# General

- Keep workflows reusable.
- Avoid application-specific logic.
- Use composite actions wherever possible.
- Keep workflows modular.
- Validate inputs.

---

# Authentication

- Use OIDC for Azure authentication.
- Avoid long-lived secrets.
- Follow least privilege RBAC.

---

# Build

- Build once.
- Publish artifacts.
- Do not rebuild during deployment.

---

# Deployment

- Download artifacts.
- Validate deployment.
- Execute health checks.
- Publish deployment summaries.

---

# Repository

- Follow naming conventions.
- Document every reusable workflow.
- Version releases.
- Keep examples updated.

---

# Security

- Use GitHub Enterprise native security.
- Enable Dependabot.
- Enable Secret Scanning.
- Enable Push Protection.
- Enable CodeQL.

---

# Documentation

- Update documentation with every release.
- Maintain CHANGELOG.
- Use semantic versioning.

---

# Version

Current Version

**v1.0.0**