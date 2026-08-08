# AWL GitHub Enterprise Reusable Workflows

# 10 - Versioning

---

# Overview

This repository follows Semantic Versioning (SemVer).

Format:

```
MAJOR.MINOR.PATCH
```

Example

```
v1.0.0
v1.1.0
v1.2.3
v2.0.0
```

---

# Version Guidelines

| Version | When to Use |
|----------|-------------|
| MAJOR | Breaking changes |
| MINOR | New features (backward compatible) |
| PATCH | Bug fixes |

---

# Tagging

Every production release should be tagged.

Example

```
v1.0.0
```

---

# Branch Strategy

```text
main
develop
release/*
feature/*
hotfix/*
```

---

# Release Process

```text
Development

↓

Testing

↓

Release Branch

↓

Git Tag

↓

GitHub Release

↓

Production
```

---

# Version

Current Version

**v1.0.0**