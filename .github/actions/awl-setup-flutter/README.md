# AWL - Setup Flutter

## Purpose

Reusable composite action to install and configure Flutter SDK for Android builds.

---

## Features

- Install Flutter SDK
- Install Java JDK
- Configure Gradle Cache
- Configure Flutter Pub Cache
- Execute flutter pub get
- Validate Flutter Installation
- Export Flutter Version
- GitHub Step Summary

---

## Supported Platforms

- Flutter Android
- Flutter APK
- Flutter App Bundle (AAB)

---

## Inputs

| Input | Default | Description |
|--------|---------|-------------|
| flutter-version | stable | Flutter SDK Version |
| java-version | 21 | Java JDK Version |
| distribution | temurin | Java Distribution |
| cache | true | Enable Flutter Pub Cache |

---

## Outputs

| Output | Description |
|--------|-------------|
| flutter-version | Installed Flutter SDK Version |

---

## Prerequisites

- Self-hosted Runner
- Android SDK Installed
- Android SDK Environment Variables Configured
- Gradle Installed (if required)
- Flutter Compatible JDK

---

## Example

```yaml
- name: Setup Flutter
  uses: ./.github/actions/awl-setup-flutter
  with:
    flutter-version: "stable"
    java-version: "21"
```

---

## Used By

- awl-build-flutter-android.yml

---

## Version History

| Version | Date | Description |
|----------|------|-------------|
| v1.0 | Initial Release | Initial composite action |

---

## Maintainer

AWL DevOps Team