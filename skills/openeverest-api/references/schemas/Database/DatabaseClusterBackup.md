# DatabaseClusterBackup

DatabaseClusterBackup is the Schema for the databaseclusterbackups API.

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `apiVersion` | string | No | APIVersion defines the versioned schema of this representation of an object.
Servers should convert recognized schemas to the latest internal value, and
may reject unrecognized values.
More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#resources |
| `kind` | string | No | Kind is a string value representing the REST resource this object represents.
Servers may infer this from the endpoint the client submits requests to.
Cannot be updated.
In CamelCase.
More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#types-kinds |
| `metadata` | object | No |  |
| `spec` | object | No | DatabaseClusterBackupSpec defines the desired state of DatabaseClusterBackup. |
| `status` | object | No | DatabaseClusterBackupStatus defines the observed state of DatabaseClusterBackup. |

## Nested Fields

### `spec`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `backupStorageName` | string | Yes | BackupStorageName is the name of the BackupStorage used for backups.
The BackupStorage must be created in the same namespace as the DatabaseCluster. |
| `dbClusterName` | string | Yes | DBClusterName is the original database cluster name. |

### `status`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `completed` | string (date-time) | No | Completed is the time when the job was completed. |
| `created` | string (date-time) | No | Created is the timestamp of the upstream backup's creation. |
| `destination` | string | No | Destination is the full path to the backup. |
| `gaps` | boolean | Yes | Gaps identifies if there are gaps detected in the PITR logs |
| `inUse` | boolean | No | InUse is a flag that indicates if this restore resource is being used to restore DB cluster from backup. |
| `latestRestorableTime` | string (date-time) | No | LatestRestorableTime is the latest time that can be used for PITR restore |
| `state` | string | No | State is the DatabaseBackup state. |

