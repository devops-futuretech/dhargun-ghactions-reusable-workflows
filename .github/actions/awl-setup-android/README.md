# AWL - Setup Android

## Purpose

Reusable composite action to configure Java runtime for Android Gradle builds.

---

## Features

- Java Installation
- Gradle Cache
- Gradle Permission
- Version Export
- GitHub Summary

---

## Example

```yaml
- name: Setup Android

  uses: ./.github/actions/awl-setup-android

  with:

    java-version: "21"
```