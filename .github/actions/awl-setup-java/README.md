# AWL - Setup Java

## Purpose

Reusable composite action to install Java JDK.

---

## Features

- Install Java
- Maven Cache
- Gradle Cache
- Version Output
- Step Summary

---

## Inputs

| Input | Default |
|--------|---------|
| java-version | 21 |
| distribution | temurin |
| cache | gradle |

---

## Outputs

| Output |
|---------|
| java-version |

---

## Example

```yaml
- name: Setup Java

  uses: ./.github/actions/awl-setup-java

  with:

    java-version: "21"

    cache: gradle
```