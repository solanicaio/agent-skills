# BackupStorage

Backup storage information

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `type` | enum: s3, azure | Yes |  |
| `namespace` | string | No |  |
| `name` | string | Yes |  |
| `description` | string | No |  |
| `bucketName` | string | Yes |  |
| `url` | string | No |  |
| `region` | string | No |  |
| `verifyTLS` | boolean | No |  |
| `forcePathStyle` | boolean | No |  |
| `allowedNamespaces` | string[] | No | List of namespaces allowed to use this backup storage |

