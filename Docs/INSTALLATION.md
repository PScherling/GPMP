# Installation Instructions

The obvious part first! Before you consider using this solution, you need to setup an active-directory in the first place, like you would do to use GPMC. I will not provide any documentation how to establish that, because there are many guides out there ;)


## 📦 Installation (Quick Start)

### 1. Extract the zip package
<img alt="image" src="Assets/zip-package.png" />


### 2. Prerequisites Installation

Open PowerShell with administrative rights and go into the this directory.

```powershell
cd "D:\Temp\GPO-Portal\GpoPortal-dev-RC-2-v0.0.7\tools"
```

<img alt="image" src="Assets/set-location.png" />


#### Installation of the database (Internet Connection required!)
Run:

```powershell
.\Install-GpoPortalPrereqs.ps1 -InstallPostgres -CreateDatabase
```

This will:
- Install required RSAT features
- Download and install PostgreSQL with dependencies
- Create database & user
- Validate connectivity

<img alt="image" src="Assets/prereq-installation.png" /><br><br>

If you don't have an internet connection, you have to provide the postgresql installer file. e.g.:
```powershell
.\Install-GpoPortalPrereqs.ps1 -InstallPostgres -CreateDatabase -PostgresInstallerPath ".\tools\postgresql-installer.exe" 
```
<br>

### 2. Install the Application

Run:

```powershell
.\Install-GpoPortal.ps1 -OpenFirewall -ApplyMigrations -RunInitialSyncOnStartup
```

This will:
- Deploy application to C:\Program Files\GpoPortal
- Register Windows Service
- Apply DB schema
- Creates Log directory in C:\ProgramData\GpoPortal
- Optionally trigger initial sync

<img alt="image" src="Assets/app-installation.png" /><br>

GPO-Portal is ready now.

<br><br>

### 3. Access UI
You can access the UI direct via the url in your favourite web browser or you execute the created desktop shortcut.
- http://localhost:5015/
- <img alt="image" src="Assets/desktop-icon.png" /> 



Authentication:
<img alt="image" src="Assets/authentication.png" /><br>


Initial Report-Sync after first logon:
An initial sync is running after the logon. You have to run the 'Report Sync' manually to enable accurate GPO Settings/report-content search. It is recommended but it takes a while depending how much Group Policy Objects you have in your system.  

<img alt="image" src="Assets/initial-sync.png" /><br><br>


#### DEV MODE
In developer builds, the application runs per default in "Read-only mode". This means, you can't make any write operations or any other changes.
<img alt="image" src="Assets/read-only.png" /><br>

You can change this setting in the applications production configuration file:
```explorer
C:\Program Files\GpoPortal\appsettings.Production.json
```

Find and set with 'Notepad++':
```json
"AllowWriteOperations":  true
```

You need to restart the gpo-portal service after changing the configration file in order to take effect:
```powershell
Restart-Service GpoPortal
```
<img alt="image" src="Assets/write-mode.png" /><br>



---


## 📦 Uninstallation

Run:

```powershell
.\Uninstall-GpoPortal.ps1 -RemovePostgreSql
```

This will:
- Stop and remove the GpoPortal Windows service
- Delete installation files
- Remove desktop shortcuts
- Uninstall PostgreSQL and clean up its data directory (if -RemovePostgreSql is specified)

<img alt="image" src="Assets/uninstallation.png" />

---
