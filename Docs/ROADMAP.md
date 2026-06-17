# Roadmap and Vision

## 💡 Vision

GPMP aims to become:

> The modern operational control plane for Active Directory and Group Policy environments.

Rather than replacing Microsoft's infrastructure, GPMP enhances it through:

* Modern administration workflows
* Operational visibility
* Compliance validation
* Security auditing
* Enterprise automation
* Centralized management

The long-term vision is to unify administration, compliance and operational intelligence within a single platform.

---

## 🛣️ Platform Evolution

### Phase 1 — Visibility ✅

Phase 1 established the foundation for modern Group Policy visibility.

Delivered capabilities:

* Organizational Unit navigation
* Group Policy discovery
* GPO inheritance visualization
* Cached metadata architecture
* Search capabilities
* Browser-based administration experience

---

### Phase 2 — Administration ✅

Phase 2 introduced controlled enterprise administration.

Delivered capabilities:

* Live write operations
* GPO enable/disable
* Link enable/disable
* Enforcement management
* HTTPS hosting
* Enterprise authorization model
* Safe-by-default write architecture
* Immediate synchronization workflows

---

### Phase 3 — Audit & Compliance 🚧 Current

Phase 3 expands GPMP beyond administration and introduces compliance and operational intelligence.

Current development areas:

#### Audit Framework

* Data-driven audit rules
* Data-driven audit findings
* Audit result persistence
* Compliance visibility

#### Normalization Framework

* Normalized configuration model
* Alias resolution
* Category mappings
* Centralized key resolution

#### Security Analysis

* Microsoft security baseline validation
* CIS benchmark preparation
* Compliance reporting

#### Administrative Improvements

* Enhanced linked OU visibility
* Advanced inheritance insights
* Create and directly link GPO workflow
* Drag & drop GPO linking
* GPO import/export functionality

#### Operational Visibility

* Improved diagnostics
* Enhanced logging
* Administrative audit trail

---

### Phase 4 — Operational Intelligence

Phase 4 focuses on predictive and enterprise-scale operational workflows.

Planned capabilities:

#### Change Intelligence

* Configuration drift detection
* Scheduled background validation
* Cache vs Active Directory comparison
* Compliance change tracking

#### Safe Change Management

* Dry-run mode
* Impact analysis
* Change preview
* Pre-execution validation

Example:

```text
This change affects:

- 14 Organizational Units
- 320 Users
- 85 Computers
- 12 Servers
```

#### Protection & Recovery

* Automatic backup creation
* Rollback capabilities
* Restore points before write operations

#### Advanced Group Policy Management

* WMI Filter management
* Advanced settings search
* Setting-level impact analysis
* Cross-GPO dependency visibility

#### Platform Scalability

* Multi-domain support
* Forest-wide visibility
* Distributed synchronization

---

### Phase 5 — Enterprise Automation

Future exploration area.

Potential capabilities:

* Compliance dashboards
* Automated remediation
* Policy recommendation engine
* SIEM integration
* Scheduled compliance reporting
* Enterprise workflow automation
* API-driven integrations

---

## ⚠️ Current Limitations

The following areas are currently under active development:

* Centralized NormalizedKeyResolver implementation
* Expanded normalization catalog coverage
* Additional Microsoft Defender audit coverage
* CIS benchmark rule packs
* Enhanced compliance reporting
* Enterprise audit visualization

---

## 🎯 Strategic Direction

GPMP started as a modern web-based alternative to traditional GPMC workflows.

The platform is now evolving into three connected pillars:

### Administration

Managing Group Policy safely and efficiently.

### Compliance

Validating configuration against defined standards.

### Operational Intelligence

Providing visibility into configuration health, risk and change.

The long-term objective is to create a platform that not only manages Group Policy, but actively helps administrators understand, validate and improve their environments.
