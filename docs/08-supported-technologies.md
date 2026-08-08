# AWL GitHub Enterprise Reusable Workflows

# 08 - Supported Technologies

---

# Overview

The reusable workflow platform supports multiple application technologies and deployment targets through standardized reusable workflows and composite actions.

---

# Build Technologies

| Technology | Build Workflow | Runtime | Build Tool | Output |
|------------|---------------|----------|------------|---------|
| React | awl-build-react.yml | Node.js | npm | Static Website |
| Node.js | awl-build-node.yml | Node.js | npm | Application Package |
| .NET | awl-build-dotnet.yml | .NET SDK | dotnet CLI | Publish Folder |
| .NET Framework | awl-build-dotnet-framework-iis.yml | MSBuild | MSBuild | IIS Package |
| Java | awl-build-java.yml | JDK | Maven / Gradle | JAR / WAR |
| Python | awl-build-python.yml | Python | pip | Application Package |
| PHP | awl-build-php.yml | PHP | Composer | Application Package |
| Android | awl-build-android-kotlin.yml | Android SDK | Gradle | APK / AAB |
| Flutter | awl-build-flutter-android.yml | Flutter SDK | Flutter | APK / AAB |
| Firebase | awl-build-firebase.yml | Firebase CLI | Firebase CLI | Hosting Package |

---

# Deployment Targets

| Platform | Workflow | Authentication |
|----------|----------|----------------|
| Azure App Service | awl-deploy-appservice.yml | OIDC |
| Azure Function | awl-deploy-azure-function.yml | OIDC |
| IIS | awl-deploy-iis.yml | Windows Credentials |
| Linux VM | awl-deploy-linux-vm.yml | SSH |
| Node PM2 | awl-deploy-node-pm2.yml | SSH |
| Firebase Hosting | awl-deploy-firebase-hosting.yml | Firebase CLI |
| Firebase Functions | awl-deploy-firebase-functions.yml | Firebase CLI |
| AKS | awl-deploy-aks.yml | OIDC |
| Power BI | awl-deploy-powerbi.yml | Microsoft Entra ID |

---

# Authentication Summary

| Platform | Authentication |
|----------|----------------|
| Azure Services | OpenID Connect (OIDC) |
| Linux VM | SSH |
| IIS | Windows Credentials |
| Firebase | Firebase CLI |
| Power BI | Microsoft Entra ID |

---

# Future Support

Potential future additions include:

- Docker
- Azure Container Apps
- Azure Container Registry
- GitHub Releases
- Notification Workflows
- Rollback Workflows

---

Current Version

**v1.0.0**