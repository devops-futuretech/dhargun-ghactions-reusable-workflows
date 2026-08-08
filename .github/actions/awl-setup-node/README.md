# AWL - Setup Node

## Purpose

Reusable composite action for installing Node.js runtime.

---

## Features

- Node.js installation
- npm support
- yarn support
- pnpm support
- Dependency cache
- Runtime version output

---

## Inputs

| Name | Default | Description |
|------|---------|-------------|
| node-version | 22 | Node.js version |
| package-manager | npm | npm / yarn / pnpm |
| enable-cache | true | Enable dependency cache |

---

## Outputs

| Name | Description |
|------|-------------|
| node-version | Installed Node.js version |

---

## Example

```yaml
- name: Setup Node
  uses: ./.github/actions/awl-setup-node
  with:
    node-version: "22"
    package-manager: npm
```