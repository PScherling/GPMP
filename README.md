# Group Policy Management Portal

![Release](https://img.shields.io/badge/release-Pre%20Release-orange)
![Platform](https://img.shields.io/badge/platform-Windows%20Server-lightgrey)
![Backend](https://img.shields.io/badge/backend-ASP.NET%20Core-blueviolet)
![Database](https://img.shields.io/badge/database-PostgreSQL-336791)
![Auth](https://img.shields.io/badge/auth-Windows%20Negotiate-green)
![Mode](https://img.shields.io/badge/mode-controlled--write-orange)

<img width="200px" alt="image" src="Docs/Assets/logo-simple.png" /><br>
> A modern, lightweight reimagining of the Group Policy Management Console (GPMC)  
> built for clarity, speed, and real-world administrative workflows.

---

## 🚀 Overview

**GPMP (Group Policy Management Portal)** is a web-based tool designed to simplify and modernize how administrators interact with Active Directory Group Policies.

<img alt="image" src="Docs/Assets/Dashboard.png" /><br>


Instead of relying on the legacy MMC-based GPMC, GPMP provides:

- Web UI (no RSAT UI dependency)
- Fast navigation of OUs and GPOs
- Full-text search across GPO objects
- Clear visibility into inheritance and relationships
- Integrated AD-based authentication & authorization
- Safe-by-default enterprise write architecture
- Controlled live GPO management
- Instant UI synchronization after changes


### Release Information

**GPMP** works with the following release declerations:

- Versioning (e.g. 15.4.2)
- Channels
- Labels

#### Channels

Channels provide a first identification of the current state. There exists 3 channels so far:

1. ![Channel](https://img.shields.io/badge/DEV-green) - Development Builds
2. ![Channel](https://img.shields.io/badge/NIGHTLY-orange) - First test builds
3. ![Channel](https://img.shields.io/badge/STABLE-blue) - A final release

#### Labels

Labels provide further release information and are optional. There exists 2 labels so far:
1. Release Candidate aka. 'RC-2'
2. General Availability aka. 'GA'

#### Example
A release could look like this:

[AppName]-[Channel]-[Label]-v[Versioning]

GpoPortal-[dev]-[RC-2]-v[0.0.1]


---


## ❔ Why GPMP?

Classic GPMC is powerful — but operationally outdated.

GPMP modernizes Group Policy management through:

- web-based administration
- live operational workflows
- interactive inheritance visibility
- enterprise-safe write operations
- modern UI/UX concepts
- centralized cache-driven architecture

without replacing the underlying Microsoft Group Policy infrastructure.

### GPMP vs Classic GPMC

| Capability | Classic GPMC | GPMP |
|---|---|---|
| MMC-based UI | ✅ | ❌ |
| Modern Web UI | ❌ | ✅ |
| Browser-based Administration | ❌ | ✅ |
| Interactive Inheritance Visualization | ⚠️ Limited | ✅ |
| Full-text GPO Search | ❌ | ✅ |
| Real-time UI Updates | ❌ | ✅ |
| Live Write Operations | ⚠️ Legacy MMC Workflow | ✅ |
| Modal-driven Operations | ❌ | ✅ |
| Enterprise-safe Write Awareness | ❌ | ✅ |
| Cached Metadata Architecture | ❌ | ✅ |
| Release-aware Platform Design | ❌ | ✅ |
| Modern UX Concepts | ❌ | ✅ |
| Instant Link State Visibility | ❌ | ✅ |
| Interactive Badge Actions | ❌ | ✅ |
| Separation of Object / Link / Inheritance State | ⚠️ Partial | ✅ |
| Web-based Operational Workflows | ❌ | ✅ |

### Interpretation

| Symbol | Meaning |
|---|---|
| ✅ | Supported |
| ❌ | Not supported |
| ⚠️ | Partially supported |


---

## 📚 Documentation

| Document | Description |
|---|---|
| [PHASE-COMPARISON.md](Docs/PHASE-Comparison.md) | RC1 vs RC2 feature comparison |
| [INSTALLATION.md](Docs/INSTALLATION.md) | Full installation, deployment and removal/cleanup guide |
| [CONFIGURATION.md](Docs/Application-Configuration.md) | Application configuration reference |
| [ARCHITECTURE.md](Docs/ARCHITECTURE.md) | Internal architecture and system design |
| [AUTHORIZATION.md](Docs/Authorization.md) | RID-based authorization model |
| [ROADMAP.md](Docs/ROADMAP.md) | Planned features and future direction |
| [Logging.md](Docs/LOGGING.md) | Application logging information |


---


## 👤 Author

**Author:** Patrick Scherling  
**Contact:** @Patrick Scherling  

---

## 🧠 Final Note

This is now Phase 2 - the transition from visibility platform to interactive enterprise management platform.

The project now demonstrates:

- controlled live Active Directory write operations
- enterprise-safe write protection architecture
- reusable modal-driven operational workflows
- live cache synchronization
- interactive inheritance management
- modernized GPO administration concepts

The architectural foundation is now capable of safely handling controlled enterprise-grade Group Policy management operations directly from the web UI.

---

> ⚡ *“Automate. Standardize. Simplify.”*  
> Part of Patrick Scherling’s IT automation suite for modern Windows Server infrastructure management.
