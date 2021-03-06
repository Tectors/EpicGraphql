# GetAccountWithFriendshipStatus
*Sheesh, this is the 9 operation created.*

Friendship status, could be used as a username lookup.

## Request
| URL | METHOD |
| - | - |
| https://graphql.epicgames.com/partyhub/graphql | POST |

## Query
```graphql
query GetAccountWithFriendshipStatus {
  Account {
    account(email: $email, displayName: $displayName, id: $id) {
      externalAuths {
       externalDisplayName
       type
       __typename
      }
     friendshipStatus
     displayName
     id
     __typename
    }
   __typename
  }
}
```

## Variables
```json
{
   "id": ""
}
```
| VARIABLES | DESCRIPTION | TYPE |
| - | - | - |
| id | An ID of sort. | STRING |

## Payload
```json
{
   "variables": {
      "id": ""
   },
   "query": "query GetAccountWithFriendshipStatus($id: String, $displayName: String, $email: String) { Account { __typename account(id: $id, displayName: $displayName, email: $email) { __typename id displayName friendshipStatus externalAuths { __typename type externalDisplayName } } } }"
}
```