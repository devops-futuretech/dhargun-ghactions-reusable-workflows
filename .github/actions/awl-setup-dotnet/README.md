# AWL - Setup .NET

## Purpose

Reusable composite action to install .NET SDK.

---

## Features

- Install .NET SDK
- NuGet cache
- Export SDK version
- GitHub Step Summary

---

## Inputs

| Input | Default |
|--------|---------|
| dotnet-version | 8.0.x |
| cache | true |

---

## Outputs

| Output | Description |
|--------|-------------|
| dotnet-version | Installed SDK |

---

## Example

```yaml
- name: Setup .NET

  uses: ./.github/actions/awl-setup-dotnet

  with:

    dotnet-version: 8.0.x
```