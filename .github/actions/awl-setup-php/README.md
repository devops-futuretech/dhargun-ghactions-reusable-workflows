# AWL - Setup PHP

## Purpose

Reusable composite action to install PHP runtime with Composer.

---

## Features

- Install PHP
- Install Composer
- Configure PHP Extensions
- Export PHP Version
- GitHub Step Summary

---

## Inputs

| Input | Default |
|--------|---------|
| php-version | 8.3 |
| extensions | Common Extensions |
| coverage | none |
| tools | composer |

---

## Outputs

| Output | Description |
|--------|-------------|
| php-version | Installed PHP Version |

---

## Example

```yaml
- name: Setup PHP
  uses: ./.github/actions/awl-setup-php
  with:
    php-version: "8.3"
```
