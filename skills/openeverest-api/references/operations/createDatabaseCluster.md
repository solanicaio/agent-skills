# POST /namespaces/{namespace}/database-clusters

**Resource:** [Database Cluster](../resources/Database-Cluster.md)
**Create database cluster**
**Operation ID:** `createDatabaseCluster`

This API creates a new database cluster in the specified namespace.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |

## Request Body

The database cluster object to be created

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [DatabaseCluster](../schemas/Database/DatabaseCluster.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 201 | Created successfully |
| 202 | Accepted |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseCluster](../schemas/Database/DatabaseCluster.md)

