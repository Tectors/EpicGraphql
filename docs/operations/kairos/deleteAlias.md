# deleteAlias

Remove a nickname.

## Request
| URL | METHOD |
| - | - |
| https://graphql.epicgames.com/partyhub/graphql | POST |

## Query
```graphql
mutation deleteAlias($friendId: String!) { Friends { __typename deleteAlias(friendId: $friendId) { __typename success } } }
```

## Variables
```json
{
   "friendId": ""
}
```
| VARIABLES | DESCRIPTION | TYPE |
| - | - | - |
| friendId | A friend ID. | STRING |

## Payload
```json
{
   "operationName": "deleteAlias",
   "variables": {},
   "query": "mutation deleteAlias($friendId: String!) { Friends { __typename deleteAlias(friendId: $friendId) { __typename success } } }"
}
```