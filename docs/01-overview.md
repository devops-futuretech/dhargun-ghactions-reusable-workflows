# AWL GitHub Enterprise Reusable Workflows

## Overview

---

## Purpose

The AWL GitHub Enterprise Reusable Workflows repository provides a centralized collection of reusable GitHub Actions workflows and composite actions to standardize Continuous Integration (CI) and Continuous Deployment (CD) across enterprise software projects.

The objective is to eliminate duplicated pipeline logic, simplify maintenance, enforce organizational standards, and accelerate application onboarding.

---

## Objectives

The platform has been designed with the following objectives:

- Standardize CI/CD implementation across all repositories
- Reduce duplicated GitHub Actions code
- Simplify workflow maintenance
- Improve deployment consistency
- Support multiple programming languages
- Support multiple deployment platforms
- Adopt GitHub Enterprise best practices
- Improve security using OpenID Connect (OIDC)
- Provide reusable and modular workflow components

---

## Design Principles

The repository follows these principles:

- Reusability
- Modularity
- Maintainability
- Security by Design
- Technology Agnostic
- Enterprise Scalability
- Minimal Consumer Configuration

---

## Repository Components

The solution consists of two primary building blocks.

### Composite Actions

Composite actions encapsulate common tasks into reusable modules.

Examples include:

- Runtime setup
- Azure authentication
- Artifact management
- Health validation
- Deployment execution
- Deployment summary

---

### Reusable Workflows

Reusable workflows orchestrate multiple composite actions into complete CI/CD pipelines.

Examples include:

- React Build
- Node.js Build
- .NET Build
- Java Build
- Python Build
- Azure App Service Deployment
- AKS Deployment
- Linux VM Deployment

---

## Supported Technologies

### Build Technologies

- React
- Node.js
- .NET
- .NET Framework
- Java
- Python
- PHP
- Android (Kotlin)
- Flutter
- Firebase

---

### Deployment Targets

- Azure App Service
- Azure Functions
- IIS
- Linux Virtual Machine
- Node.js PM2
- Firebase Hosting
- Firebase Functions
- Azure Kubernetes Service (AKS)
- Power BI

---

## Authentication Model

Azure authentication is implemented using OpenID Connect (OIDC).

Benefits include:

- Secretless authentication
- Short-lived access tokens
- Reduced credential management
- Improved security posture
- Microsoft recommended approach

---

## Repository Scope

This repository provides reusable automation only.

It does not contain:

- Application source code
- Consumer application workflows
- Repository governance templates
- Branch protection rules
- CODEOWNERS
- Issue templates
- Pull request templates

These components are maintained separately within application repositories or organizational template repositories.

---

## Intended Audience

This repository is intended for:

- DevOps Engineers
- Platform Engineers
- Cloud Engineers
- Azure Administrators
- GitHub Enterprise Administrators
- Application Development Teams

---

## Benefits

Organizations adopting this repository can expect:

- Faster project onboarding
- Reduced maintenance effort
- Consistent CI/CD implementation
- Improved deployment reliability
- Centralized workflow management
- Enterprise-grade standardization

---

## Version

Current Version

**v1.0.0**