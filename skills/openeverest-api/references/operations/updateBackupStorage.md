# PATCH /namespaces/{namespace}/backup-storages/{name}

**Resource:** [Backup Storage](../resources/Backup-Storage.md)
**Update backup storage**
**Operation ID:** `updateBackupStorage`

This API updates the backup storage specified by the `name`. Only the specified fields will be updated.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `name` | path | string | Yes | Name of the backup storage |
| `namespace` | path | string | Yes | Namespace of the backup storage |

## Request Body

The backup storage params. Only the specified fields will be updated.

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpdateBackupStorageParams](../schemas/Update/UpdateBackupStorageParams.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[BackupStorage](../schemas/Backup/BackupStorage.md)

