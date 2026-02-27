# GET /namespaces/{namespace}/database-cluster-backups/{name}

**Resource:** [Backup](../resources/Backup.md)
**Get database cluster backup**
**Operation ID:** `getDatabaseClusterBackup`

This API gets the database cluster backup specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `name` | path | string | Yes | Name of the database cluster backup. Can be found under Metadata["name"] of the DatabaseClusterBackup object. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseClusterBackup](../schemas/Database/DatabaseClusterBackup.md)

