# AWL GitHub Enterprise Reusable Workflows

# 05 - Build Workflows Reference

---

# Overview

Build workflows provide standardized Continuous Integration (CI) pipelines for supported application technologies.

Each workflow performs technology-specific build operations while following a common enterprise architecture.

---

# Common Build Flow

All build workflows follow the same execution pattern.

```text
Checkout Repository
        │
        ▼
Setup Runtime
        │
        ▼
Restore Dependencies
        │
        ▼
Build Application
        │
        ▼
Publish Output
        │
        ▼
Upload Artifact
```

---

# Common Characteristics

| Feature | Supported |
|----------|-----------|
| Reusable Workflow | ✅ |
| Composite Actions | ✅ |
| Artifact Upload | ✅ |
| Runtime Setup | ✅ |
| Parameterized Inputs | ✅ |
| GitHub Environment Support | ✅ |

---

# Supported Build Workflows

| Workflow | Technology | Runtime | Build Tool | Output |
|----------|------------|----------|------------|---------|
| awl-build-react.yml | React | Node.js | npm | Static Website |
| awl-build-node.yml | Node.js | Node.js | npm | Application Package |
| awl-build-dotnet.yml | .NET | .NET SDK | dotnet CLI | Publish Folder |
| awl-build-dotnet-framework-iis.yml | .NET Framework | MSBuild | MSBuild | IIS Package |
| awl-build-java.yml | Java | JDK | Maven / Gradle | JAR / WAR |
| awl-build-python.yml | Python | Python | pip | Application Package |
| awl-build-php.yml | PHP | PHP | Composer | Application Package |
| awl-build-android-kotlin.yml | Android | Android SDK | Gradle | APK / AAB |
| awl-build-flutter-android.yml | Flutter | Flutter SDK | Flutter | APK / AAB |
| awl-build-firebase.yml | Firebase | Node.js | Firebase CLI | Hosting Package |

---

# Standard Workflow Structure

Each reusable workflow contains:

```text
Workflow Header

↓

workflow_call

↓

Inputs

↓

Secrets

↓

Permissions

↓

Build Job

↓

Composite Actions

↓

Artifact Upload
```

---

# Standard Inputs

Most build workflows expose the following inputs.

| Input | Purpose |
|--------|----------|
| environment | GitHub Environment |
| artifact-name | Build Artifact Name |
| retention-days | Artifact Retention |
| build-configuration | Release / Debug |
| runtime-version | Runtime Version |

Technology-specific workflows may expose additional inputs.

---

# Standard Outputs

| Output | Description |
|---------|-------------|
| artifact-name | Uploaded Artifact |
| build-status | Build Result |

---

# Runtime Setup

Runtime installation is delegated to Composite Actions.

| Runtime | Composite Action |
|----------|------------------|
| Node.js | awl-setup-node |
| .NET | awl-setup-dotnet |
| .NET Framework | awl-setup-dotnet-framework |
| Java | awl-setup-java |
| Python | awl-setup-python |
| PHP | awl-setup-php |
| Android | awl-setup-android |
| Flutter | awl-setup-flutter |
| Firebase | awl-setup-firebase |

---

# Artifact Management

Every build workflow publishes artifacts using:

```text
awl-upload-artifact
```

The generated artifact becomes the deployment input for reusable deployment workflows.

---

# Example Consumer Workflow

```yaml
jobs:

  build:

    uses: organization/awl-github-enterprise-reusable-workflows/.github/workflows/awl-build-react.yml@v1

    with:

      environment: DEV

      artifact-name: react-build

      node-version: 22
```

---

# Technology Summary

## React

Purpose

Build React applications using npm.

Output

Compiled static web application.

---

## Node.js

Purpose

Build server-side Node.js applications.

Output

Deployment package.

---

## .NET

Purpose

Compile and publish .NET applications.

Output

Publish folder.

---

## .NET Framework IIS

Purpose

Compile legacy .NET Framework applications for IIS deployment.

Output

Web Deploy package or published IIS content.

---

## Java

Purpose

Compile Java applications using Maven or Gradle.

Output

JAR or WAR.

---

## Python

Purpose

Install dependencies and package Python applications.

Output

Deployment package.

---

## PHP

Purpose

Restore Composer dependencies and package the application.

Output

Deployment package.

---

## Android

Purpose

Compile Android applications.

Output

APK or Android App Bundle.

---

## Flutter

Purpose

Compile Flutter Android applications.

Output

APK or Android App Bundle.

---

## Firebase

Purpose

Prepare Firebase Hosting deployment package.

Output

Firebase Hosting artifact.

---

# Best Practices

- Use Release configuration for production builds.
- Upload artifacts instead of rebuilding during deployment.
- Keep runtime versions consistent.
- Use semantic artifact names.
- Keep reusable workflows technology-specific.

---

# Version

Current Version

**v1.0.0**