# Group Policy Management Portal

![Phase](https://img.shields.io/badge/NIGHTLY-orange)
![Platform](https://img.shields.io/badge/Windows%20Server-lightgrey)
![Backend](https://img.shields.io/badge/ASP.NET%20Core-blueviolet)
![Database](https://img.shields.io/badge/PostgreSQL-336791)
![Auth](https://img.shields.io/badge/NTLM-green)
![Auth](https://img.shields.io/badge/Kerberos-green)
![AuditEngine](https://img.shields.io/badge/Audit%20Engine-blue)

<img width="200px" alt="image" src="Docs/Assets/logo-simple.png" /><br>

> A modern, lightweight reimagining of the Group Policy Management Console (GPMC)  
> built for clarity, speed, and real-world administrative workflows.

---

<br>

## 🚀 Overview

**GPMP (Group Policy Management Portal)** is a modern web-based management platform for Microsoft Group Policy environments.

It modernizes classic Group Policy administration by replacing legacy MMC-based workflows with a fast, interactive and browser-based experience, while still fully relying on Microsoft's native Group Policy infrastructure.

<img alt="image" src="Docs/Assets/Dashboard.png" /><br>


GPMP provides:

- Modern browser-based administration
- Interactive OU and inheritance visualization
- Full-text Group Policy search
- Real-time UI synchronization
- Controlled live write operations
- RID-based authorization
- Safe-by-default operational workflows
- PowerShell-driven integration with Active Directory
- Centralized cache-driven architecture

---

<br>

## 🛠️ Project Status

GPMP is currently in active development and approaching the next major NIGHTLY milestone release.

The platform has evolved beyond a traditional Group Policy viewer and now provides:

- Browser-based Group Policy administration
- Controlled Active Directory write operations
- Enterprise-oriented authorization concepts
- Interactive inheritance visualization
- Domain audit export generation
- Compliance baseline evaluation
- Normalization-driven audit analysis
- Rule-pack based compliance architecture

The current NIGHTLY builds are fully functional and actively used for real-world testing and validation.

---

<br>

# ✨ Current Features

## Group Policy Management

- Browse Active Directory OU structures
- View linked and inherited GPOs
- Full-text GPO search
- Render native GPO reports
- Interactive inheritance visualization
- Link visibility tree views
- Live synchronization

## Administrative Operations

- Create GPOs
- Delete GPOs
- Rename GPOs
- Enable / Disable GPOs
- Link GPOs to OUs
- Remove GPO links
- Enable / Disable links
- Enforce / Remove enforcement
- Immediate cache synchronization

## Authorization & Safety

- Windows Authentication
- Kerberos / NTLM support
- RID-based authorization
- Read-only mode
- Write-mode separation
- Confirmation protected operations
- Safe-by-default deployment model

## Audit & Compliance

- Full domain audit export packages
- HTML audit reports
- CSV export generation
- Parser framework
- Normalization engine
- Rule-pack architecture
- Compliance baseline evaluation
- Findings engine
- Baseline exception support

## Platform Features

- ASP.NET Core (.NET 10)
- PostgreSQL
- Windows Service support
- Self-contained deployment
- HTTPS support
- Initial synchronization
- Sync history tracking
- PowerShell integration

---

<br>

# ❔ Why GPMP?

Microsoft's Group Policy infrastructure remains one of the most powerful configuration management systems available for Windows environments.

However, the traditional GPMC experience has changed very little over the last decade.

GPMP modernizes Group Policy administration by introducing:

- Browser-based management
- Interactive visualization
- Safe operational workflows
- Enterprise authorization concepts
- Audit and compliance capabilities
- Modern deployment architecture

while continuing to rely entirely on Microsoft's native Group Policy infrastructure.

---

<br>

# ⚖️ GPMP vs Classic GPMC

| Capability | Classic GPMC | GPMP |
|---|---|---|
| MMC-based UI                 | ✅ | ❌ |
| Modern Web UI                | ❌ | ✅ |
| Browser-based Administration | ❌ | ✅ |
| Interactive Inheritance Visualization | ⚠️ Limited | ✅ |
| Full-text GPO Search         | ❌ | ✅ |
| Real-time UI Updates         | ❌ | ✅ |
| Live Write Operations        | ⚠️ Legacy Workflow | ✅ |
| Modal-driven Operations      | ❌ | ✅ |
| Cached Metadata Architecture | ❌ | ✅ |
| Instant Link State Visibility | ❌ | ✅ |
| Interactive Badge Actions    | ❌    | ✅ |
| Separation of Object / Link / Inheritance State | ⚠️ Partial | ✅ |
| Modern UX Concepts           | ❌    | ✅ |
| Browser-based Administration | ❌    | ✅    |
| Windows Authentication       | ⚠️   | ✅    |
| Full-text Search             | ❌    | ✅    |
| Inheritance Visualization    | ⚠️   | ✅    |
| Live Synchronization         | ❌    | ✅    |
| Domain Audit Export          | ❌    | ✅    |
| Compliance Baselines         | ❌    | ✅    |
| Rule Pack Architecture       | ❌    | ✅    |
| Normalization Engine         | ❌    | ✅    |
| Findings Engine              | ❌    | ✅    |
| Windows Service Deployment   | ❌    | ✅    |
| PostgreSQL Metadata Cache    | ❌    | ✅    |


---

<br>

### 📦 Release Information

| Channel | Purpose |
|---|---|
| NIGHTLY | Public preview builds with newest features |
| STABLE | Recommended production-ready releases |

Current public release:

```text
v0.0.8-nightly-RC1
```

<br>

#### Channels

Channels provide a first identification of the current state. There exists 3 channels so far:

1. ![Channel](https://img.shields.io/badge/DEV-green) - Development Builds
2. ![Channel](https://img.shields.io/badge/NIGHTLY-orange) - First test builds
3. ![Channel](https://img.shields.io/badge/STABLE-blue) - A final release

<br>

### ⚠️ Disclaimer

GPMP performs live Active Directory Group Policy operations.

Although multiple safety mechanisms and confirmation workflows are implemented ('Read-Only-Mode' per default is set!), this software is still considered pre-release software at least it is not declared with the ![Channel](https://img.shields.io/badge/STABLE-blue) badge.

Always test in a non-production environment before deploying into critical infrastructure.

---

<br>

## 🏗️ Architecture Highlights

GPMP is built around a cache-driven architecture.

Core components:

- ASP.NET Core (.NET 10)
- PostgreSQL Metadata Cache
- PowerShell Execution Layer
- Active Directory Integration
- Group Policy Management API
- Synchronization Engine
- Audit & Compliance Engine

The platform intentionally separates:

- Object State
- Link State
- Inheritance State
- Authorization State
- Operational State

to provide safer and more predictable administration workflows.

---

<br>

## 🌐 Browser Support Matrix

<table>
  <tbody>
    <tr>
      <th>Browser</th>
      <td><img width="30" height="30" alt="image" src="Docs/Assets/edge.png" /></td>
      <td><img width="30" height="30" alt="image" src="Docs/Assets/chrome.png" /></td>
      <td><img width="30" height="30" alt="image" src="Docs/Assets/firefox.png" /></td>
      <td><img width="30" height="30" alt="image" src="Docs/Assets/opera.png" /></td>
      <td><img width="30" height="30" alt="image" src="Docs/Assets/safari.png" /></td>
    </tr>
    <tr>
      <th>Compatibility</th>
      <td>✅ (Preferred)</td>
      <td>✅</td>
      <td>❌</td>
      <td>✅</td>
      <td>⚠️ (Not Tested)</td>
    </tr>
  </tbody>
</table>

---

<br>

## 🔍 Audit & Compliance Engine

GPMP includes an integrated audit and compliance platform capable of evaluating Group Policy configurations against reusable compliance baselines.

Features include:

- Parser-based setting extraction
- Normalized configuration mapping
- JSON rule packs
- Baseline evaluation
- Findings generation
- Compliance exceptions
- HTML export packages
- CSV export packages

The audit engine is designed to support organizational standards, security baselines and future compliance frameworks.

---

<br>

## 📚 Documentation

| Document | Description |
|---|---|
| [RELEASE-COMPARISON.md](Docs/Release-Comparison.md) | DEV RC1 vs. NIGHTLY RC1 feature comparison |
| [INSTALLATION.md](Docs/INSTALLATION.md) | Full installation, deployment and removal/cleanup guide |
| [CONFIGURATION.md](Docs/Application-Configuration.md) | Application configuration reference |
| [ARCHITECTURE.md](Docs/ARCHITECTURE.md) | Internal architecture and system design |
| [AUTHORIZATION.md](Docs/Authorization.md) | RID-based authorization model |
| [ROADMAP.md](Docs/ROADMAP.md) | Planned features and future direction |
| [Logging.md](Docs/LOGGING.md) | Application logging information |

---

<br>

## 🧠 Final Note

GPMP aims to modernize Group Policy management through:
- browser-based administration
- interactive operational workflows
- safer change visibility
- modern UI/UX concepts
- automation-friendly architecture

without replacing Microsoft’s underlying Group Policy infrastructure.


---

<br>

## 👤 Author

**Author:** Patrick Scherling  
**Contact:** @Patrick Scherling  

---

> ⚡ *“Automate. Standardize. Simplify.”*  
> Part of Patrick Scherling’s IT automation suite for modern Windows Server infrastructure management.
