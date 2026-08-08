# AWL - Download Artifact

## Purpose

Reusable composite action to download build artifacts.

---

## Features

- Download artifact
- Validate artifact
- Display downloaded files
- GitHub Step Summary

---

## Inputs

| Input | Default |
|-------|---------|
| artifact-name | Required |
| download-path | artifact |
| merge-multiple | false |

---

## Outputs

| Output | Description |
|---------|-------------|
| artifact-path | Download location |

---

## Example

```yaml
- name: Download Artifact
  uses: ./.github/actions/awl-download-artifact
  with:
    artifact-name: web-ui
    download-path: artifact
```