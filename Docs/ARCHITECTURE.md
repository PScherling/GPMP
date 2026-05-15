# Application Architecture

## 🏗️ Architecture Model
[ Browser UI ]

↓

[ ASP.NET Core API ]

↓

[ PostgreSQL Database ]

↓

[ PowerShell + AD / GPMC ]

---

## 🛡️ Write Architecture Philosophy

Sensei follows a deliberately controlled enterprise write model.

Write operations are:

- disabled globally by default
- separately authorized from read operations
- visually separated in the UI
- confirmation-protected
- audit-aware
- immediately synchronized back into cache state

This allows the platform to safely evolve from a visualization tool into a real enterprise management system without sacrificing operational safety.

The architecture intentionally differentiates between:

- object state
- link state
- inheritance behavior
- UI write visibility
- authorization capability
- global operational mode

This separation is critical for enterprise-safe Active Directory management.
