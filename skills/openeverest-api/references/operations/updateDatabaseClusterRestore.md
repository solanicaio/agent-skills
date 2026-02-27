# PUT /namespaces/{namespace}/database-cluster-restores/{name}

**Resource:** [Restore](../resources/Restore.md)
**Update database cluster restore**
**Operation ID:** `updateDatabaseClusterRestore`

This API updates the database cluster restore specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `name` | path | string | Yes | Name of the database cluster restore. Can be found under Metadata["name"] of the DatabaseClusterRestore object. |

## Request Body

The database cluster restore object to be updated

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [DatabaseClusterRestore](../schemas/Database/DatabaseClusterRestore.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 201 | Created successful |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseClusterRestore](../schemas/Database/DatabaseClusterRestore.md)

