# AWL - Setup Firebase

## Purpose

Reusable composite action to install Firebase CLI.

---

## Features

- Reuse AWL Setup Node
- Install Firebase CLI
- Verify Firebase CLI
- Export Version
- GitHub Step Summary

---

## Inputs

| Input | Default |
|--------|---------|
| node-version | 22 |
| package-manager | npm |

---

## Outputs

| Output |
|---------|
| firebase-version |

---

## Example

```yaml
- name: Setup Firebase

  uses: ./.github/actions/awl-setup-firebase

  with:

    node-version: "22"
```

---

## Used By

- awl-build-firebase.yml
- awl-deploy-firebase-hosting.yml
- awl-deploy-firebase-functions.yml