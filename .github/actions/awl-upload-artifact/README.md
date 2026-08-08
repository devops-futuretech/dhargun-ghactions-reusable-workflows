# AWL - Upload Artifact

## Purpose

Reusable composite action to upload build artifacts.

---

## Features

- Artifact validation
- Upload artifact
- Compression support
- Retention support
- Overwrite existing artifact
- Build summary

---

## Inputs

| Input | Default |
|-------|---------|
| artifact-name | Required |
| artifact-path | Required |
| retention-days | 30 |
| compression-level | 6 |
| overwrite | true |

---

## Outputs

| Output |
|---------|
| artifact-name |

---

## Example

```yaml
- name: Upload Build

  uses: ./.github/actions/awl-upload-artifact

  with:

    artifact-name: web-ui

    artifact-path: dist
```