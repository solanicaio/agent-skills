# GET /namespaces/{namespace}/database-clusters/{cluster-name}/backups

**Resource:** [Backup](../resources/Backup.md)
**List database cluster backups**
**Operation ID:** `listDatabaseClusterBackups`

This API lists all database cluster backups in the specified `namespace`.


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

[DatabaseClusterBackupList](../schemas/Database/DatabaseClusterBackupList.md)

