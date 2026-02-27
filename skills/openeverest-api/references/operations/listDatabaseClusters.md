# GET /namespaces/{namespace}/database-clusters

**Resource:** [Database Cluster](../resources/Database-Cluster.md)
**List database clusters**
**Operation ID:** `listDatabaseClusters`

This API lists all database clusters in the specified namespace.


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

[DatabaseClusterList](../schemas/Database/DatabaseClusterList.md)

