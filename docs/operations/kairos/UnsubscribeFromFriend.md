# UnsubscribeFromFriend

Unsubscribe from a friend. (Removes notifications from that friend)

## Request
| URL | METHOD |
| - | - |
| https://graphql.epicgames.com/partyhub/graphql | POST |

## Query
```graphql
mutation UnsubscribeFromFriend($friendID: String!) { PresenceV2 { __typename unSubscribeUser(namespace: "_", publisherId: $friendID) { __typename success } } }
```

## Variables
```json
{
   "friendID": ""
}
```
| VARIABLES | DESCRIPTION | TYPE |
| - | - | - |
| friendID | None | None |

## Payload
```json
{
   "operationName": "UnsubscribeFromFriend",
   "variables": {},
   "query": "mutation UnsubscribeFromFriend($friendID: String!) { PresenceV2 { __typename unSubscribeUser(namespace: \"_\", publisherId: $friendID) { __typename success } } }"
}
```