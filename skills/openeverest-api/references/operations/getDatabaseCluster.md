# GET /namespaces/{namespace}/database-clusters/{name}

**Resource:** [Database Cluster](../resources/Database-Cluster.md)
**Get database cluster**
**Operation ID:** `getDatabaseCluster`

This API gets the database cluster specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `name` | path | string | Yes | Name of the database cluster. Can be found under Metadata["name"] of the DatabaseCluster object. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseCluster](../schemas/Database/DatabaseCluster.md)

