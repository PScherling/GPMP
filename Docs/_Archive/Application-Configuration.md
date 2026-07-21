# Configuration Example

## 🧠 Configuration

Configuration is stored in:

appsettings.json

Example
```json
{
  "GpoPortal": {
    "Version": "0.0.1",
    "ReleaseChannel": "dev",
    "ReleaseLabel": "RC1",
    "RedirectHttp": false,
	"WriteExecutionMode": "ServiceAccount",
    "AllowWriteOperations": true,
    "RunInitialSyncOnStartup": true,
    "InitialSyncReports": false,
    "AuthorizationDomain": null,
    "ReadAccessGroupRids": [512, 519],
    "WriteAccessGroupRids": [512],  
    "ReadAccessGroupNames": [
        "Template-Group"
      ],
    "WriteAccessGroupNames": [
      "Template-Admins"
    ],
  },
  "Sync": {
	"AutoSyncOnAccess": true,
	"AutoSyncMinimumIntervalMinutes": 15,
	"ReportDeltaSyncEnabled": true
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "Kestrel": {
    "Endpoints": {
      "Http": {
        "Url": "gpmpsrv.remedy.local:5015"
      },
      "Https": {
		        "Url": "https://gpmpsrv.remedy.local:5016",
		        "Certificate": {
			        "Subject": "gpmpsrv.remedy.local",
			        "Store": "My",
			        "Location": "LocalMachine",
			        "Thumbprint": "1234567890ABCDEF1234567890ABCDEF12345678",
			        "AllowInvalid": false
		        }
	        }
    }
  },
  "AllowedHosts": "*",
  "ConnectionStrings":  {
        "DefaultConnection":  null
    }
}

```
