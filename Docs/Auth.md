# Authentication & Service Deployment

## 📖 Overview

One of the major milestones of Phase 3 was the introduction of a production-ready authentication and service deployment model.

This milestone solved several challenges that commonly occur when hosting Active Directory management applications as Windows Services.

The result is a deployment model that supports:

* Windows Integrated Authentication
* Active Directory authorization
* Enterprise service accounts
* Active Directory write operations
* Kerberos authentication
* Automated installation workflows

while maintaining secure-by-default behavior.

---

# 🔐 Authentication Model

Sensei uses Windows Integrated Authentication through ASP.NET Core Negotiate Authentication.

Supported authentication methods:

* Kerberos (preferred)
* NTLM (fallback)

User authentication is handled automatically through the browser and Windows security context.

No application-specific user database exists.

---

# 🔒 Authorization Model

Authorization is separated into two independent permission levels:

## Read Access

Allows:

* Viewing Organizational Units
* Viewing Group Policies
* Viewing inheritance information
* Viewing audit results

## Write Access

Allows:

* Creating Group Policies
* Deleting Group Policies
* Modifying GPO status
* Managing GPO links
* Enforcement operations

Authorization is determined through Active Directory group membership using configured RID values.

This allows organizations to delegate permissions without changing application code.

---

# ⚠️ Initial Challenge

During early development the application was executed under:

```text
NT AUTHORITY\SYSTEM
```

While synchronization operations worked correctly, Active Directory write operations failed.

Typical errors included:

```text
Access is denied.
```

or

```text
UnauthorizedAccessException
```

The issue was caused by PowerShell operations executing under the LocalSystem security context.

Although LocalSystem has extensive local privileges, it does not automatically possess the required permissions for delegated Active Directory administration tasks.

---

# 🛠️ Service Account Architecture

To support enterprise write operations, Sensei now runs under a dedicated domain service account.

Example:

```text
DOMAIN\svc-sensei
```

Benefits:

* Explicit permission delegation
* Proper Active Directory auditing
* Controlled security model
* Predictable authorization behavior

All PowerShell operations execute using the service account identity.

---

# 🌐 Kerberos & SPN Requirements

When hosting Sensei as a Windows Service using Windows Authentication, Kerberos requires Service Principal Names (SPNs).

Required examples:

```text
HTTP/servername
HTTP/servername.domain.local
```

Without proper SPN registration:

* Kerberos authentication fails
* Browser authentication may fall back to NTLM
* Authorization behavior may become inconsistent

---

# 🚀 Installation Improvements

The installation framework was extended to automatically prepare the environment.

Implemented improvements include:

## Service Account Support

* Domain service account execution
* Configurable service identity

## Logon Rights

The installer automatically grants:

```text
Log on as a service
```

to the configured service account.

This removes the need for manual Local Security Policy modifications.

## SPN Registration

The installer validates and registers required HTTP SPNs.

This ensures proper Kerberos authentication after deployment.

## Startup Validation

Additional startup validation now verifies:

* Service identity
* Authentication configuration
* Authorization configuration
* PowerShell script path configuration
* Operational mode configuration

Startup diagnostics are written to application logs.

---

# 🔍 Troubleshooting

## Authentication Fails

Verify:

* SPN registration
* Browser Integrated Authentication settings
* Service account configuration

## Write Operations Fail

Verify:

* Service account permissions
* Group Policy delegation
* Active Directory rights

## Service Fails to Start

Verify:

* Log on as a service rights
* Configuration values
* PowerShell script availability

Application startup logs contain detailed diagnostic information.

---

# 🎯 Result

This milestone transformed Sensei from a development-hosted application into a production-ready Windows Service platform.

The platform now supports:

* Enterprise deployment
* Kerberos authentication
* Active Directory authorization
* Delegated administration
* Controlled write operations
* Automated installation workflows

This foundation is required for future compliance, auditing and operational intelligence capabilities.
