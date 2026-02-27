# GET /namespaces/{namespace}/database-engines/{name}

**Resource:** [Database Engine](../resources/Database-Engine.md)
**Get database engine**
**Operation ID:** `getDatabaseEngine`

This API gets the database engine specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `name` | path | string | Yes | Name of the database engine |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseEngine](../schemas/Database/DatabaseEngine.md)

