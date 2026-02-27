# DELETE /namespaces/{namespace}/database-cluster-backups/{name}

**Resource:** [Backup](../resources/Backup.md)
**Delete database cluster backup**
**Operation ID:** `deleteDatabaseClusterBackup`

This API deletes the database cluster backup specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `name` | path | string | Yes | Name of the database cluster backup. Can be found under Metadata["name"] of the DatabaseClusterBackup object. |
| `cleanupBackupStorage` | query | boolean | No | If set, remove the backed up data from storage |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[io.k8s.apimachinery.pkg.apis.meta.v1.Status_v2](../schemas/io-k8s-apimachinery-pkg-apis-meta-v1-Status/io-k8s-apimachinery-pkg-apis-meta-v1-Status-v2.md)

