# POST /namespaces/{namespace}/backup-storages

**Resource:** [Backup Storage](../resources/Backup-Storage.md)
**Create backup storage**
**Operation ID:** `createBackupStorage`

This API creates a new backup storage.

**Examples**:
  ```
  {
    "metadata": {
      "name": "s3-storage",
      "namespace": "everest",
    },
    "spec": {
      "type": "s3",
      "bucketName": "bucket1",
      "accessKey": "access_key",
      "secretKey": "secret_key",
      "region": "eu-central-1"
    },
  }
  ```

  ```
  {
    "metadata": {
      "name": "azure-storage",
      "namespace": "everest",
    },
    "spec": {
      "type": "azure",
      "bucketName": "container1",
      "accessKey": "storage_account_name",
      "secretKey": "storage_account_key",
    },
  }
  ```


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Namespace of the backup storage |

## Request Body

The backup storage object to be created

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [CreateBackupStorageParams](../schemas/Create/CreateBackupStorageParams.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[BackupStorage](../schemas/Backup/BackupStorage.md)

