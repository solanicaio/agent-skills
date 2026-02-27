# GET /namespaces/{namespace}/backup-storages

**Resource:** [Backup Storage](../resources/Backup-Storage.md)
**List backup storages**
**Operation ID:** `listBackupStorages`

This API lists all backup storages.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Namespace of the backup storage |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[BackupStoragesList](../schemas/Backup/BackupStoragesList.md)

