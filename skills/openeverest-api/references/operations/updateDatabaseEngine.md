# PUT /namespaces/{namespace}/database-engines/{name}

**Resource:** [Database Engine](../resources/Database-Engine.md)
**Update database engine**
**Operation ID:** `updateDatabaseEngine`

This API updates the database engine specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `name` | path | string | Yes | Name of the database engine |

## Request Body

The database cluster object to be updated

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [DatabaseEngine](../schemas/Database/DatabaseEngine.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseEngine](../schemas/Database/DatabaseEngine.md)

