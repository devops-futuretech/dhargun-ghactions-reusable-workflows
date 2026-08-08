# AWL - Setup .NET Framework

## Purpose

Reusable composite action to validate Visual Studio Build Tools, MSBuild and NuGet on self-hosted Windows runners.

---

## Features

- Validate Visual Studio Build Tools
- Locate MSBuild using vswhere
- Validate NuGet
- Export MSBuild path
- GitHub Step Summary

---

## Prerequisites

- Windows Self-hosted Runner
- Visual Studio 2022 Build Tools or Visual Studio 2022
- MSBuild
- NuGet CLI
- vswhere.exe

---

## Inputs

| Input | Default | Description |
|--------|---------|-------------|
| msbuild-version | 17 | Preferred MSBuild version |
| nuget-version | latest | Preferred NuGet version |

---

## Outputs

| Output | Description |
|--------|-------------|
| msbuild-path | Full path of MSBuild.exe |

---

## Example

```yaml
- name: Setup .NET Framework

  uses: ./.github/actions/awl-setup-dotnet-framework
```

---

## Used By

- awl-build-dotnet-framework-iis.yml

---

## Version History

| Version | Description |
|----------|-------------|
| v1.0 | Initial Release |

---

## Maintainer

AWL DevOps Team