# SetNotificationSettings
*Sheesh, this is the 25 operation created.*

Set party and friend requests notifications in one request!

## Request
| URL | METHOD |
| - | - |
| https://graphql.epicgames.com/partyhub/graphql | POST |

## Query
```graphql
mutation SetNotificationSettings($friendRequestNotificationSettings: NotificationSettingsInput!, $partyNotificationSettings: NotificationSettingsInput!, $namespace: String!) {
  Friends {
    setNotificationSettings(data: $friendRequestNotificationSettings) {
     status
     success
      offline {
       suppress_all
       __typename
      }
     __typename
    }
   __typename
  }
  PartySettings {
    setNotificationSettings(value: $partyNotificationSettings, namespace: $namespace) {
     status
     success
      offline {
       suppress_all
       __typename
      }
     __typename
    }
   __typename
  }
}
```

## Variables
```json
{
   "friendRequestNotificationSettings": {},
   "partyNotificationSettings": {},
   "namespace": ""
}
```
| VARIABLES | DESCRIPTION | TYPE |
| - | - | - |
| friendRequestNotificationSettings | None | object |
| partyNotificationSettings | None | object |
| namespace | The short/full name of the game. | String |

## Payload
```json
{
   "variables": {
      "namespace": "",
      "partyNotificationSettings": {
         "offline": {
            "suppress_all": Boolean
         }
      },
      "friendRequestNotificationSettings": {
         "offline": {
            "suppress_all": Boolean
         }
      }
   },
   "query": "mutation SetNotificationSettings($namespace: String!, $partyNotificationSettings: NotificationSettingsInput!, $friendRequestNotificationSettings: NotificationSettingsInput!) { PartySettings { __typename setNotificationSettings(namespace: $namespace, value: $partyNotificationSettings) { __typename offline { __typename suppress_all } success status } } Friends { __typename setNotificationSettings(data: $friendRequestNotificationSettings) { __typename offline { __typename suppress_all } success status } } }"
}
```