# POST /namespaces/{namespace}/database-cluster-backups

**Resource:** [Backup](../resources/Backup.md)
**Create database cluster backup**
**Operation ID:** `createDatabaseClusterBackup`

This API creates a new database cluster backup in the specified `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |

## Request Body

The database cluster backup object to be created

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [DatabaseClusterBackup](../schemas/Database/DatabaseClusterBackup.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 201 | Created success |
| 202 | Accepted |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseClusterBackup](../schemas/Database/DatabaseClusterBackup.md)

