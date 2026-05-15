# Configuration Example

## 🧠 Configuration

Configuration is stored in:

appsettings.json

Example
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Host=localhost;Port=5432;Database=gpoportal;Username=gpoportal_app;Password=Your-Password"
  },
  "GpoPortal": {
    "Version": "0.0.1",
    "ReleaseChannel": "dev",
    "ReleaseLabel": "RC1",
    "AllowWriteOperations": false,
    "RunInitialSyncOnStartup": true,
    "ReadAccessGroupRids": [512, 519],
    "WriteAccessGroupRids": [512],
  
    "ReadAccessGroupNames": [
        "Template-Group"
      ],
    "WriteAccessGroupNames": [
      "Template-Admins"
    ],
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
        "Url": "http://localhost:5015"
      }
    }
  },
  "AllowedHosts": "*"
}

```
