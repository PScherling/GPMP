# Architecture

## 🏗️ High-Level Architecture

GPMP follows a layered architecture designed for:

- browser-based administration
- centralized metadata management
- controlled write operations
- Active Directory integration
- operational safety

---

## 📐 Architecture Flow

```text
[ Browser UI ]

        ↓

[ ASP.NET Core API ]

        ↓

[ PostgreSQL Database ]

        ↓

[ PowerShell Integration Layer ]

        ↓

[ Active Directory / GPMC ]
```

---

## 🧩 Component Overview

### Browser UI

The frontend provides a modern web-based administration experience for Group Policy environments.

Responsibilities include:

- OU tree rendering
- inheritance visualization
- GPO search
- modal-driven operational workflows
- write-aware UI rendering
- live state updates after operations

The frontend communicates exclusively through the REST API layer.

<br>

### ASP.NET Core API

The backend API acts as the central orchestration layer.

Responsibilities include:

- authentication & authorization
- API endpoints
- write validation
- operational safety controls
- cache synchronization
- database interaction
- PowerShell execution control

The API separates read and write responsibilities internally to support safer operational workflows.

<br>

### PostgreSQL Database

GPMP uses PostgreSQL as a centralized metadata cache.

The database stores:

- GPO metadata
- OU information
- inheritance relationships
- report content
- synchronization state
- operational metadata

Active Directory remains the authoritative source of truth.

The database is designed to improve:

- UI responsiveness
- searching
- filtering
- operational visibility
- synchronization efficiency

<br>

### PowerShell Integration Layer

GPMP uses controlled PowerShell execution for interaction with Microsoft Group Policy infrastructure.

Responsibilities include:

- GPO synchronization
- report generation
- write operations
- inheritance discovery
- Active Directory integration

PowerShell acts as the bridge between GPMP and native Microsoft Group Policy APIs.

<br>

### Active Directory / GPMC

GPMP does not replace Microsoft Group Policy infrastructure.

Instead, it builds a modern operational layer on top of:

- Active Directory
- Group Policy Management Console APIs
- native GroupPolicy PowerShell modules

This ensures compatibility with existing enterprise environments.

---

## 🛡️ Write Operation Philosophy

GPMP follows a deliberately controlled write model.

Write operations are:

- disabled globally by default
- separated from read permissions
- confirmation protected
- visually isolated in the UI
- synchronized immediately after execution

<br>

The architecture intentionally separates:

- GPO object state
- GPO link state
- inheritance behavior
- UI visibility
- authorization capability
- operational mode

This separation helps reduce ambiguity and improves operational clarity.

---

## 🔐 Authorization Model

GPMP uses Windows Authentication with RID-based authorization.

This avoids localization issues across different Active Directory languages and naming conventions.

Examples:

- Group	RID
- Domain Admins	512
- Enterprise Admins	519

Authorization is evaluated independently for:

- read access
- write access

---

## 🔄 Synchronization Concept

GPMP uses a cache-driven synchronization model.

Synchronization workflows include:

- GPO metadata sync
- OU structure sync
- inheritance sync
- report synchronization

After write operations, affected cache entries are updated immediately to keep the UI synchronized with Active Directory state.

---

## ⚡ Design Goals

The architecture focuses on:

- operational clarity
- centralized visibility
- safer workflows
- responsiveness
- maintainability
- extensibility
- modern administration concepts

while remaining fully compatible with Microsoft’s native Group Policy ecosystem.

---

🧠 Long-Term Vision

The long-term goal of GPMP is to evolve into a modern operational platform for enterprise Group Policy management.

Planned architectural expansion areas include:

- scheduled background synchronization
- advanced auditing
- delegated RBAC models
- multi-domain awareness
- approval workflows
- WMI filter management
- security filtering management
- API-driven automation workflows
