# PUT /namespaces/{namespace}/database-clusters/{name}

**Resource:** [Database Cluster](../resources/Database-Cluster.md)
**Update database cluster**
**Operation ID:** `updateDatabaseCluster`

This API updates a database cluster specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `name` | path | string | Yes | Name of the database cluster. Can be found under Metadata["name"] of the DatabaseCluster object. |

## Request Body

The database cluster object to be updated

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [DatabaseCluster](../schemas/Database/DatabaseCluster.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseCluster](../schemas/Database/DatabaseCluster.md)

