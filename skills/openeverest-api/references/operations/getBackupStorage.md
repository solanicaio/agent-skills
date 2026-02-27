# GET /namespaces/{namespace}/backup-storages/{name}

**Resource:** [Backup Storage](../resources/Backup-Storage.md)
**Get backup storage**
**Operation ID:** `getBackupStorage`

This API gets the backup storage speciciied by the `name` in the given `namespace`.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `name` | path | string | Yes | Name of the backup storage |
| `namespace` | path | string | Yes | Namespace of the backup storage |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[BackupStorage](../schemas/Backup/BackupStorage.md)

