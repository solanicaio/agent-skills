# POST /namespaces/{namespace}/database-cluster-restores

**Resource:** [Restore](../resources/Restore.md)
**Create database cluster restore**
**Operation ID:** `createDatabaseClusterRestore`

This API creates a new database cluster restore in the specified `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |

## Request Body

The database cluster restore object to be created

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [DatabaseClusterRestore](../schemas/Database/DatabaseClusterRestore.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 201 | Created success |
| 202 | Accepted |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseClusterRestore](../schemas/Database/DatabaseClusterRestore.md)

