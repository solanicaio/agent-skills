# GET /permissions

**Resource:** [Authentication & Authorization](../resources/Authentication-Authorization.md)
**Get user permissions**
**Operation ID:** `getUserPermissions`

This API returns a list of permissions for the user that is currently logged in.

*Example:*
Assume the following RBAC policy, and users `alice` and `bob`:
```
p, role:dev, namespaces, read, *
p, role:dev, database-engines, *, */*
p, role:dev, database-clusters, *, */*
p, bob, database-clusters, *, */*
g, alice, role:dev
```
The API will return the following permissions for `alice`:
```
{
  "permissions": [
    [
        "alice",
        "namespaces",
        "read",
        "*"
    ],
    [
        "alice",
        "database-engines",
        "*",
        "*/*"
    ],
    [
        "alice",
        "database-clusters",
        "*",
        "*/*"
    ]
  ]
}
```
And the following permissions for `bob`:
```
{
  "permissions": [
    [
        "bob",
        "database-clusters",
        "*",
        "*/*"
    ]
  ]
}
```


## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[UserPermissions](../schemas/User/UserPermissions.md)

