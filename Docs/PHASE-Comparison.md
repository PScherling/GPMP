# Sensei Release-Phase Comparison

This page provides an indeph view on the improvmenets started with "Pahse 1" of project "Sensei".

---

## 📈 Phase Comparison (Quick Look)

| Feature | Phase 1 (RC1) | Phase 2 (RC2) |
|---|---|---|
| OU Tree Visualization | ✅ | ✅ |
| GPO Object Search | ✅ | ✅ |
| GPO HTML Report Rendering | ✅ | ✅ |
| Inheritance Visualization | ✅ | ✅ |
| Read-only Architecture | ✅ | ✅ |
| Windows Authentication | ✅ | ✅ |
| RID-based Authorization | ✅ | ✅ |
| Global Write Protection | ✅ | ✅ |
| Release Channels / Labels | ✅ | ✅ |
| Initial Startup Sync | ✅ | ✅ |
| Sync History | ✅ | ✅ |
| Self-contained Deployment | ✅ | ✅ |
| Windows Service Support | ✅ | ✅ |
| PostgreSQL Backend | ✅ | ✅ |
| GPO Status Changes | ❌ | ✅ |
| GPO Link Enable / Disable | ❌ | ✅ |
| GPO Enforcement Toggle | ❌ | ✅ |
| Quick-action Badges | ❌ | ✅ |
| Instant UI Refresh After Changes | ❌ | ✅ |
| Write-aware UI Controls | ❌ | ✅ |
| Confirmation Dialogs | ❌ | ✅ |
| Audit Logging Foundation | ⚠️ Basic | ✅ Improved |
| Live AD Write Operations | ❌ | ✅ |
| Cached DB State Updates | ❌ | ✅ |
| Enterprise-safe Write Model | ❌ | ✅ |
| Direct vs Inherited Link Logic | ⚠️ Visual Only | ✅ Interactive |
| Real-time GPO Link Management | ❌ | ✅ |
| Create GPO Workflow | ❌ | ✅ |
| Modal-based Write Dialogs | ❌ | ✅ |
| Interactive Write Modals | ❌ | ✅ |
| Live Cache Mutation After Writes | ❌ | ✅ |
| Dynamic Badge State Refresh | ❌ | ✅ |
| Reusable Write Confirmation Framework | ❌ | ✅ |
| Keyboard-aware Modal UX | ❌ | ✅ |

<br>

### Interpretation

| Symbol | Meaning |
|---|---|
| ✅ | Implemented |
| ❌ | Not implemented |
| ⚠️ | Partial / basic implementation |

<br>

---

<br>

## 🧩 New in Phase 2

Phase 2 introduces the first production-grade write operations.

The portal is no longer only a visualization layer — it now supports controlled Active Directory modifications directly from the web UI.

### ✅ Implemented Write Operations

#### GPO Object Management
- Create new GPOs
<img alt="image" src="Assets/gpo-create.png" />
<br>
<br>

- Delete existing GPOs
<img alt="image" src="Assets/gpo-delete.png" />
<br>
<br>

- Change GPO status:
  - All settings enabled
  - User configuration disabled
  - Computer configuration disabled
  - Entire GPO disabled
<img alt="image" src="Assets/change-gposettings.png" />
<br>
<br>


#### GPO Link Management
- Link GPO to an OU
<img alt="image" src="Assets/link-gpo.png" />
<br>
<br>

- Interactive quick-action badges
<img alt="image" src="Assets/quick-badges.png" />
<br>
<br>

- Enable / Disable GPO Links
<img alt="image" src="Assets/disable-link.png" />
<br>
<br>

- Enforce / remove enforcement
<img alt="image" src="Assets/enforce-gpo.png" />
<br>
<br>

- Remove GPO Link from OUs
<img alt="image" src="Assets/remove-linked-gpo.png" />
<br>
<br>

- Immediate UI refresh after changes

<br>

#### Write UX
- Modal-based confirmation dialogs
- Write-aware UI controls
- Keyboard-aware write dialogs
- Real-time badge refresh
- Dynamic write state visibility

### ✅ Core Functionality & Management
- Active Directory OU Tree visualization
- GPO object listing and filtering
- GPO details & HTML report rendering
- GPO inheritance view
- Searching across all Group Policy Objects and matching based on 'Name', 'Description' or 'Content'. Match is Highlighted for instant visibillity.
- Instant visibillity of link status, enforcement and enabled or disabled Group Policy Objects
- Live GPO write operations
- Quick-action inheritance management
- Link enforcement toggling
- Write-aware badges and controls

### 🔒 Enterprise Safety Features
- Global write mode toggle
- Separate read/write authorization
- Write-aware UI
- Confirmation dialogs
- Audit logging foundation
- Controlled PowerShell execution layer

### ⚡ Live UI Improvements
- Instant badge updates
- Real-time inheritance refresh
- Dynamic write-state rendering
- Improved action visibility
- Release-aware toolbar

### 🖥️ Modern UI Workflow

Phase 2 RC2 introduces a more modern operational workflow inspired by contemporary admin portals rather than legacy MMC tooling.

Implemented UX improvements include:

- Modal-based write dialogs
- Interactive quick-action badges
- Real-time UI refresh after changes
- Dynamic toolbar state awareness
- Context-sensitive write controls
- Instant inheritance updates
- Write-operation visibility separation
- Keyboard-aware dialog handling

The portal now behaves more like a modern management platform instead of a static administration console.


### 🧠 Architecture Improvements
- Cached database updates after write operations
- Optimistic UI refresh strategy
- Better separation between:
  - GPO object state
  - GPO link state
  - inheritance behavior

#### Stylesheet Structure

The UI styling is split into focused stylesheet files:

- `stylesheet_main.css` – base layout, panels, tree, details and report view
- `stylesheet_toolbar.css` – toolbar, release badges, sync state and authorization display
- `stylesheet_modal.css` – modal dialogs and write-confirmation UX
- `stylesheet_misc.css` – reusable badges, GPO list styling and utility classes

 
### 📘 Important Terminology

Sensei differentiates between:

| Type | Meaning |
|------|----------|
| GPO Status | Object-level configuration state (enabled/disabled settings) |
| GPO Link State | Whether a GPO link is linked or unlinked on a container |
| Enforcement | Whether the GPO overrides inheritance blocking |
| Link Scope | Whether the GPO is directly linked or inherited |

This separation avoids ambiguity and mirrors real enterprise Group Policy behavior.


---

## 🧩 Features (Phase 1)

### ✅ Core Functionality
- Active Directory OU Tree visualization
- GPO object listing and filtering
- GPO details & HTML report rendering
- GPO inheritance view
- Searching across all Group Policy Objects and matching based on 'Name', 'Description' or 'Content'. Match is Highlighted for instant visibillity.
- Instant visibillity of link status, enforcement and enabled or disabled Group Policy Objects

### 🔐 Security & Access Control
- Windows Authentication (Negotiate / Kerberos / NTLM)
- Group-based authorization (via SID / RID)
- Read / Write separation
- Global write toggle (safe-by-default)

### ⚙️ Backend
- ASP.NET Core (.NET 10)
- PostgreSQL database
- Entity Framework Core
- PowerShell integration (GPO reporting & sync)

### 🔄 Sync System
- Manual sync (GPOs, OUs, inheritance, reports)
- Initial startup sync (optional)
- Sync history tracking

### 🧪 Deployment
- Self-contained publish (no Visual Studio required)
- Windows Service installation
- Automated prerequisite script (RSAT, PostgreSQL, DB setup)

