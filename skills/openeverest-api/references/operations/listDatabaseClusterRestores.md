# GET /namespaces/{namespace}/database-clusters/{cluster-name}/restores

**Resource:** [Restore](../resources/Restore.md)
**List database cluster restores**
**Operation ID:** `listDatabaseClusterRestores`

This API lists all database cluster restores for a database cluster specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `cluster-name` | path | string | Yes | Name of the database cluster. Can be found under Metadata["name"] of the DatabaseCluster object. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseClusterRestoreList](../schemas/Database/DatabaseClusterRestoreList.md)

