# AWL - Setup Python

## Purpose

Reusable composite action to install Python runtime.

---

## Features

- Install Python
- Upgrade pip
- pip Cache
- Export Python Version
- GitHub Step Summary

---

## Inputs

| Input | Default |
|--------|---------|
| python-version | 3.12 |
| cache | pip |

---

## Outputs

| Output | Description |
|--------|-------------|
| python-version | Installed Python Version |

---

## Example

```yaml
- name: Setup Python

  uses: ./.github/actions/awl-setup-python

  with:

    python-version: "3.12"
```