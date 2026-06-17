# GPMP Release Comparison

This document provides an overview of the feature evolution and architectural improvements between the public GPMP release generations.

---

## 📈 Release Comparison

| Capability                   | RC 1 | RC 2 | RC 3 |
| ---------------------------- | ------- | ------- | ------- |
| Browser-based Administration | ✅       | ✅       | ✅       |
| OU Tree Visualization        | ✅       | ✅       | ✅       |
| GPO Discovery                | ✅       | ✅       | ✅       |
| GPO Report Rendering         | ✅       | ✅       | ✅       |
| Inheritance Visualization    | ✅       | ✅       | ✅       |
| Search Capabilities          | ✅       | ✅       | ✅       |
| Windows Authentication       | ✅       | ✅       | ✅       |
| RID-based Authorization      | ✅       | ✅       | ✅       |
| PostgreSQL Backend           | ✅       | ✅       | ✅       |
| Synchronization Engine       | ✅       | ✅       | ✅       |
| Windows Service Support      | ✅       | ✅       | ✅       |
| Release-aware Deployment     | ✅       | ✅       | ✅       |
| Live Write Operations        | ❌       | ✅       | ✅       |
| GPO Creation                 | ❌       | ✅       | ✅       |
| GPO Deletion                 | ❌       | ✅       | ✅       |
| GPO Status Management        | ❌       | ✅       | ✅       |
| GPO Link Management          | ❌       | ✅       | ✅       |
| Enforcement Management       | ❌       | ✅       | ✅       |
| Write-aware UI               | ❌       | ✅       | ✅       |
| Enterprise-safe Write Model  | ❌       | ✅       | ✅       |
| Real-time UI Synchronization | ❌       | ✅       | ✅       |
| Unknown GPO Owner Repair Feature | ❌       | ❌       | ✅       |
| Compliance Auditing          | ❌       | ❌       | 🚧      |
| Audit Rule Framework         | ❌       | ❌       | 🚧      |
| Audit Findings Framework     | ❌       | ❌       | 🚧      |
| Normalization Framework      | ❌       | ❌       | 🚧      |
| Security Baseline Validation | ❌       | ❌       | 🚧      |
| Compliance Reporting         | ❌       | ❌       | 🚧      |
| Operational Intelligence     | ❌       | ❌       | 🚧      |


---

# 🧩 Phase 1 — Visibility

Phase 1 established the foundation of the platform.

The focus was providing visibility into Active Directory and Group Policy environments through a modern web interface.

## Delivered Capabilities

### Group Policy Visibility

* Organizational Unit tree
* Group Policy discovery
* GPO details
* HTML report rendering
* Inheritance visualization
* Search functionality

### Security & Access Control

* Windows Authentication
* RID-based Authorization
* Read / Write separation
* Global write protection

### Platform Foundation

* ASP.NET Core
* PostgreSQL
* Entity Framework Core
* PowerShell integration
* Synchronization engine
* Windows Service support

---

# 🧩 Phase 2 — Administration

Phase 2 transformed Sensei from a visibility platform into an administration platform.

The focus shifted from viewing Group Policy to safely managing it.

## Delivered Capabilities

### GPO Management

* Create GPO
* Delete GPO
* Modify GPO Status
* Enable / Disable User Configuration
* Enable / Disable Computer Configuration

### Link Management

* Create Links
* Remove Links
* Enable / Disable Links
* Enforcement Management

### Enterprise Safety

* Write-aware UI
* Confirmation dialogs
* Authorization-aware controls
* Global write mode
* Immediate synchronization

### Modern Administration UX

* Quick action badges
* Modal workflows
* Dynamic UI updates
* Keyboard-aware dialogs
* Real-time state refresh

### Architecture Improvements

* Live Active Directory write operations
* Cache mutation after writes
* Separation of:

  * Object State
  * Link State
  * Inheritance State
  * Authorization State

---

# 🧩 Phase 3 — Audit & Compliance

Phase 3 extends the platform beyond administration and introduces compliance, auditing and operational intelligence.

## Current Focus Areas

### Audit Framework

* Data-driven audit rules
* Data-driven audit findings
* Audit result persistence
* Compliance reporting

### Normalization Framework

* Normalized configuration model
* Alias resolution
* Category mappings
* Centralized normalization services

### Security Analysis

* Microsoft security baseline validation
* Compliance assessment
* Future CIS benchmark support

### Operational Intelligence

* Configuration analysis
* Administrative diagnostics
* Compliance visibility
* Audit insights

---

# 🚀 Architectural Progression

The evolution of Sensei can be summarized in three stages:

| Phase   | Primary Goal       |
| ------- | ------------------ |
| Phase 1 | Visibility         |
| Phase 2 | Administration     |
| Phase 3 | Audit & Compliance |

The long-term vision is to continue evolving the platform toward operational intelligence and enterprise automation while remaining fully compatible with Microsoft's native Group Policy infrastructure.
