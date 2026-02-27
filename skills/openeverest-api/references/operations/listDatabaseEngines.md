# GET /namespaces/{namespace}/database-engines

**Resource:** [Database Engine](../resources/Database-Engine.md)
**List database engines**
**Operation ID:** `listDatabaseEngines`

This API lists all database engines in the specified `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseEngineList](../schemas/Database/DatabaseEngineList.md)

