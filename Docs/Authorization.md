# Authorization

# 🔐 Authorization Model

GPMP uses Windows Authentication together with RID-based authorization to control access to the platform.

The authorization model is designed to:

- avoid localization issues
- separate read and write permissions
- support enterprise Active Directory environments
- provide predictable access control behavior

---

# 🪪 Authentication

GPMP supports:

- Windows Negotiate Authentication
- Kerberos
- NTLM

Authentication is handled through ASP.NET Core and integrated directly with Active Directory.

This enables seamless browser-based authentication inside domain environments.

---

# 🛡️ Authorization Philosophy

GPMP separates:

- authentication
- read permissions
- write permissions
- operational mode

This separation allows the platform to:

- safely expose visibility features
- restrict operational capabilities
- disable write operations globally when required
- provide safer administrative workflows

---

# 🧩 RID-Based Authorization

Instead of validating localized Active Directory group names, GPMP validates access using well-known Relative Identifiers (RIDs).

Examples:

| Group | RID |
|---|---|
| Domain Admins | 512 |
| Enterprise Admins | 519 |

This ensures compatibility across:

- English Active Directory environments
- German Active Directory environments
- localized domain deployments
- mixed-language enterprise infrastructures

For example:

| Language | Group Name |
|---|---|
| English | Domain Admins |
| German | Domänen-Admins |

Although the visible names differ, the RID remains identical.

---

# 🔄 Read vs Write Access

GPMP differentiates between:

| Access Type | Purpose |
|---|---|
| Read Access | View GPOs, inheritance, reports and metadata |
| Write Access | Perform live Group Policy operations |

This separation allows organizations to provide visibility access without automatically granting operational write permissions.

---

# ⚠️ Global Write Protection

Write operations are additionally protected through a global operational switch.

Even authorized users cannot execute write operations when global write mode is disabled.

This provides an additional operational safety layer.

---

# 🧠 Security Goals

The authorization model is designed to provide:

- predictable authorization behavior
- localization-independent validation
- operational safety
- enterprise compatibility
- safer browser-based administration workflows

while remaining fully integrated with native Microsoft Active Directory authentication mechanisms.
