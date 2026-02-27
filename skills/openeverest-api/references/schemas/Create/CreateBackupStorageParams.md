# CreateBackupStorageParams

Backup storage parameters

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | A user defined string name of the storage in the DNS name format https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#dns-label-names |
| `description` | string | No |  |
| `type` | enum: s3, azure | Yes |  |
| `bucketName` | string | Yes | The cloud storage bucket/container name |
| `accessKey` | string | Yes |  |
| `secretKey` | string | Yes |  |
| `url` | string | No |  |
| `region` | string | No |  |
| `allowedNamespaces` | string[] | No | List of namespaces allowed to use this backup storage |
| `verifyTLS` | boolean | No |  |
| `forcePathStyle` | boolean | No |  |

