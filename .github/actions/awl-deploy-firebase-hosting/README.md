# AWL - Deploy Firebase Hosting

## Purpose

Deploy static websites to Firebase Hosting.

---

## Features

- Validate artifact
- Firebase Hosting deployment
- Multiple hosting targets
- GitHub Step Summary

---

## Inputs

| Input | Description |
|--------|-------------|
| project-id | Firebase Project |
| artifact-path | Build Output |
| firebase-token | Firebase CI Token |
| target | Hosting Target |

---

## Used By

- awl-deploy-firebase-hosting.yml

---

## Prerequisites

- Firebase CLI
- Firebase Token
- firebase.json