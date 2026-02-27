# DatabaseClusterRestore

DatabaseClusterRestore is the Schema for the databaseclusterrestores API.

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
| `spec` | object | No | DatabaseClusterRestoreSpec defines the desired state of DatabaseClusterRestore. |
| `status` | object | No | DatabaseClusterRestoreStatus defines the observed state of DatabaseClusterRestore. |

## Nested Fields

### `spec`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `dataSource` | object | Yes | DataSource defines a data source for restoration. |
| `dbClusterName` | string | Yes | DBClusterName defines the target database cluster name that needs to be restored from backup. |

#### `spec.dataSource`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `backupSource` | object | No | BackupSource is the backup source to restore from.
Shall be set either this field or DBClusterBackupName. |
| `dbClusterBackupName` | string | No | DBClusterBackupName is the name of the DB cluster backup to restore from.
Shall be set either this field or BackupSource. |
| `pitr` | object | No | PITR is the point-in-time recovery configuration.
May be set in addition to DBClusterBackupName or BackupSource to perform PITR restore. |

### `status`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `completed` | string (date-time) | No |  |
| `inUse` | boolean | No | InUse is a flag that indicates if this restore resource is being used to restore DB cluster from backup. |
| `message` | string | No |  |
| `state` | string | No | RestoreState represents state of restoration. |

