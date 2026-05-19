# Configuration Example

## 🧠 Configuration

The main configuration for the application is stored in: **C:\Program Files\GPM-Portal\appsettings.production.json**

Example
```json
{
    "GpoPortal":  {
                      "InitialSyncReports":  false,
                      "AllowWriteOperations":  false,
                      "RedirectHttp": false,
                      "AuthorizationDomain": null,
                      "ReadAccessGroupRids":  [
                                                  512,
                                                  519
                                              ],
                      "WriteAccessGroupRids":  [
                                                   512
                                               ],
                      "ReadAccessGroupNames":  [

                                               ],
                      "WriteAccessGroupNames":  [

                                                ],
                      "RunInitialSyncOnStartup":  true
                  },
    "Kestrel":  {
                    "Endpoints":  {
                                      "Https":  {
                                                    "Url":  "https://gpmpsrv.remedy.local:5016",
                                                    "Certificate":  {
                                                                        "Subject":  "gpmpsrv.remedy.local",
                                                                        "AllowInvalid":  false,
                                                                        "Thumbprint":  "1234567890ABCDEF1234567890ABCDEF12345678",
                                                                        "Location":  "LocalMachine",
                                                                        "Store":  "My"
                                                                    }
                                                },
                                      "Http":  {
                                                   "Url":  "http://localhost:5015"
                                               }
                                  }
                },
    "AllowedHosts": "*",
    "Logging": {
        "LogLevel": {
          "Default": "Information",
          "Microsoft.AspNetCore": "Warning"
        }
    },
    "ConnectionStrings":  {
                              "DefaultConnection":  null
                          }
}

```
