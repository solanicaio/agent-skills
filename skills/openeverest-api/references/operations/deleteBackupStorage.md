# DELETE /namespaces/{namespace}/backup-storages/{name}

**Resource:** [Backup Storage](../resources/Backup-Storage.md)
**Delete backup storage**
**Operation ID:** `deleteBackupStorage`

This API deletes the backup storage specified by the `name`.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `name` | path | string | Yes | Name of the backup storage |
| `namespace` | path | string | Yes | Namespace of the backup storage |

## Responses

| Status | Description |
|--------|-------------|
| 204 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

