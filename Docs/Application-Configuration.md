# Configuration Example

## 🧠 Configuration

Configuration is stored in:

appsettings.production.json

Example
```json
{
    "GpoPortal":  {
                      "InitialSyncReports":  false,
                      "AllowWriteOperations":  false,
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
                                      "Http":  {
                                                   "Url":  "http://localhost:5015"
                                               }
                                  }
                },
    "ConnectionStrings":  {
                              "DefaultConnection":  null
                          }
}

```
