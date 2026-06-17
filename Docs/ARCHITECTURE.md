# Application Architecture

## 🏗️ High-Level Architecture

Sensei follows a layered architecture designed to separate presentation, business logic, data persistence and Active Directory interaction.

```text
┌─────────────────────────────┐
│         Browser UI          │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│      ASP.NET Core API       │
│                             │
│ • Authentication            │
│ • Authorization             │
│ • GPO Management            │
│ • Audit Engine              │
│ • Synchronization Services  │
│ • Normalization Services    │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│      PostgreSQL Database    │
│                             │
│ • Cached GPO Metadata       │
│ • Audit Results             │
│ • Audit Rules               │
│ • Audit Findings            │
│ • Normalization Catalog     │
│ • Application Configuration │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│   PowerShell Execution      │
│          Layer              │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│ Active Directory / GPMC     │
│ Windows Infrastructure      │
└─────────────────────────────┘
```

---

## 🧩 Core Components

### Web UI

The browser-based frontend provides a modern administrative interface for:

* Group Policy management
* Inheritance visualization
* Audit visibility
* Compliance reporting
* Operational workflows

The frontend communicates exclusively through the ASP.NET Core API.

---

### ASP.NET Core API

The API acts as the central orchestration layer.

Responsibilities include:

* Authentication
* Authorization
* Business logic
* Audit processing
* Synchronization workflows
* Configuration management
* PowerShell orchestration

The API contains no direct Group Policy logic and instead delegates infrastructure operations to dedicated PowerShell execution services.

---

### PostgreSQL Database

Sensei uses PostgreSQL as its operational data store.

The database persists:

* Cached Active Directory information
* Cached Group Policy information
* Audit results
* Audit findings
* Audit rules
* Normalization catalogs
* Application configuration
* Operational metadata

The database is considered the application's source of operational truth.

---

### PowerShell Execution Layer

PowerShell serves as the infrastructure integration layer.

Responsibilities include:

* GPO synchronization
* OU synchronization
* Inheritance collection
* Report collection
* GPO administration
* Link management
* Active Directory interaction

This layer allows Sensei to remain fully compatible with Microsoft's native Group Policy infrastructure.

---

## 🔐 Authentication & Authorization

Sensei uses Windows Integrated Authentication.

Authorization is separated into:

* Read access
* Write access

Access decisions are based on Active Directory group RID membership.

This allows organizations to delegate administrative permissions without modifying application code.

---

## 🔄 Synchronization Architecture

Sensei operates on a cache-first architecture.

Infrastructure data is synchronized into PostgreSQL and consumed by the user interface.

Benefits include:

* Faster UI response times
* Reduced Active Directory load
* Consistent operational visibility
* Improved scalability

Synchronization currently supports:

* Organizational Units
* Group Policy Objects
* GPO Links
* Inheritance Information
* GPO Reports

---

## 🛡️ Write Architecture Philosophy

Sensei follows a deliberately controlled enterprise write model.

Write operations are:

* Disabled by default
* Separately authorized
* Explicitly visible in the UI
* Confirmation protected
* Operationally logged
* Immediately synchronized after execution

The architecture intentionally separates:

* Object State
* Link State
* Inheritance State
* Authorization State
* Operational Mode
* UI Visibility

This separation allows enterprise-safe administration while maintaining clear visibility into administrative impact.

---

## 🔍 Audit Architecture

The audit subsystem is designed around a data-driven model.

Audit behavior is not hardcoded into the application.

Instead, audit logic is defined through:

* Rule Packs
* Findings Packs
* Normalization Catalogs

This approach allows new compliance checks to be introduced without requiring application code changes.

---

## 🧠 Normalization Architecture

Raw Group Policy settings can originate from different report structures and policy categories.

The normalization framework transforms these raw settings into standardized Normalized Keys.

This provides:

* Consistent audit processing
* Rule reusability
* Simplified compliance validation
* Future baseline compatibility

The normalization framework is built around:

* Normalization Catalogs
* Alias Definitions
* Category Mappings
* Resolver Services

---

## 🚀 Architectural Vision

Phase 1 established visibility.

Phase 2 introduced controlled administration.

Phase 3 introduces compliance, auditing and operational intelligence.

The long-term goal is to evolve Sensei into a unified operational control plane for Active Directory environments while remaining fully compatible with Microsoft's native infrastructure.
