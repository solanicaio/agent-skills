# DatabaseCluster

DatabaseCluster is the Schema for the databaseclusters API.

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
| `spec` | object | No | DatabaseClusterSpec defines the desired state of DatabaseCluster. |
| `status` | object | No | DatabaseClusterStatus defines the observed state of DatabaseCluster. |

## Nested Fields

### `spec`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowUnsafeConfiguration` | boolean | No | AllowUnsafeConfiguration field used to ensure that the user can create configurations unfit for production use.

Deprecated: AllowUnsafeConfiguration will not be supported in the future releases. |
| `backup` | object | No | Backup is the backup specification |
| `dataSource` | object | No | DataSource defines a data source for bootstraping a new cluster |
| `engine` | object | Yes | Engine is the database engine specification |
| `engineFeatures` | object | No | EngineFeatures represents configuration of additional features for the database engine. |
| `monitoring` | object | No | Monitoring is the monitoring configuration |
| `paused` | boolean | No | Paused is a flag to stop the cluster |
| `podSchedulingPolicyName` | string | No | PodSchedulingPolicyName is the name of the PodSchedulingPolicy CR that defines rules for DB cluster pods allocation across the cluster. |
| `proxy` | object | No | Proxy is the proxy specification. If not set, an appropriate
proxy specification will be applied for the given engine. A
common use case for setting this field is to control the
external access to the database cluster. |
| `sharding` | object | No | Sharding is the sharding configuration. PSMDB-only |

#### `spec.backup`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `enabled` | boolean | No | Enabled is a flag to enable backups
Deprecated. Please use db.spec.backup.schedules[].enabled to control each schedule separately and db.spec.backup.pitr.enabled to control PITR. |
| `pitr` | object | No | PITR is the configuration of the point in time recovery |
| `schedules` | object[] | No | Schedules is a list of backup schedules |

#### `spec.dataSource`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `backupSource` | object | No | BackupSource is the backup source to restore from |
| `dataImport` | object | No | DataImport allows importing data from an external backup source. |
| `dbClusterBackupName` | string | No | DBClusterBackupName is the name of the DB cluster backup to restore from |
| `pitr` | object | No | PITR is the point-in-time recovery configuration |

#### `spec.engine`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `config` | string | No | Config is the engine configuration |
| `crVersion` | string | No | CRVersion is the desired version of the CR to use with the
underlying operator.
If unspecified, everest-operator will use the same version as the operator.

NOTE: Updating this property post installation may lead to a restart of the cluster. |
| `replicas` | integer (int32) | No | Replicas is the number of engine replicas |
| `resources` | object | No | Resources are the resource limits for each engine replica.
If not set, resource limits are not imposed |
| `storage` | object | Yes | Storage is the engine storage configuration |
| `type` | enum: pxc, postgresql, psmdb | Yes | Type is the engine type |
| `userSecretsName` | string | No | UserSecretsName is the name of the secret containing the user secrets |
| `version` | string | No | Version is the engine version |

#### `spec.engineFeatures`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `psmdb` | object | No | PSMDB represents additional features for the PSMDB engine. |

#### `spec.monitoring`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `monitoringConfigName` | string | No | MonitoringConfigName is the name of a monitoringConfig CR.
The MonitoringConfig must be created in the same namespace as the DatabaseCluster. |
| `resources` | object | No | Resources defines resource limitations for the monitoring. |

#### `spec.proxy`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `config` | string | No | Config is the proxy configuration |
| `expose` | object | No | Expose is the proxy expose configuration |
| `replicas` | integer (int32) | No | Replicas is the number of proxy replicas |
| `resources` | object | No | Resources are the resource limits for each proxy replica.
If not set, resource limits are not imposed |
| `type` | enum: mongos, haproxy, proxysql... | No | Type is the proxy type |

#### `spec.sharding`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `configServer` | object | Yes | ConfigServer represents the sharding configuration server settings |
| `enabled` | boolean | Yes | Enabled defines if the sharding is enabled |
| `shards` | integer (int32) | Yes | Shards defines the number of shards |

### `status`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `activeStorage` | string | No | ActiveStorage is the storage used in cluster (psmdb only) |
| `conditions` | object[] | No | Conditions contains the observed conditions of the DatabaseCluster. |
| `crVersion` | string | No | CRVersion is the observed version of the CR used with the underlying operator. |
| `dataImportJobName` | string | No | DataImportJobName refers to the DataImportJob that is used to import data into the cluster.
This is set only when .spec.dataSource.dataImport is set. |
| `details` | string | No | Details provides full status of the upstream cluster as a plain text. |
| `engineFeatures` | object | No | EngineFeaturesStatus represents additional features statuses for the database engine. |
| `hostname` | string | No | Hostname is the hostname where the cluster can be reached |
| `message` | string | No | Message is extra information about the cluster |
| `observedGeneration` | integer (int64) | No | ObservedGeneration is the most recent generation observed for this DatabaseCluster. |
| `port` | integer (int32) | No | Port is the port where the cluster can be reached |
| `ready` | integer (int32) | No | Ready is the number of ready pods |
| `recommendedCRVersion` | string | No | RecommendedCRVersion indicates the target version that the underlying CR should be updated to.
When this field is set, it means the CR is running an outdated version and requires an update.
The following restrictions apply until the CR is updated to the recommended version:
- The operator cannot be upgraded
- The database engine version (.spec.engine.version) cannot be modified
This field is unset when the CR is already running at the latest recommended version. |
| `size` | integer (int32) | No | Size is the total number of pods |
| `status` | string | No | Status is the status of the cluster |

#### `status.conditions`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `lastTransitionTime` | string (date-time) | Yes | lastTransitionTime is the last time the condition transitioned from one status to another.
This should be when the underlying condition changed.  If that is not known, then using the time when the API field changed is acceptable. |
| `message` | string | Yes | message is a human readable message indicating details about the transition.
This may be an empty string. |
| `observedGeneration` | integer (int64) | No | observedGeneration represents the .metadata.generation that the condition was set based upon.
For instance, if .metadata.generation is currently 12, but the .status.conditions[x].observedGeneration is 9, the condition is out of date
with respect to the current state of the instance. |
| `reason` | string | Yes | reason contains a programmatic identifier indicating the reason for the condition's last transition.
Producers of specific condition types may define expected values and meanings for this field,
and whether the values are considered a guaranteed API.
The value should be a CamelCase string.
This field may not be empty. |
| `status` | enum: True, False, Unknown | Yes | status of the condition, one of True, False, Unknown. |
| `type` | string | Yes | type of condition in CamelCase or in foo.example.com/CamelCase. |

#### `status.engineFeatures`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `psmdb` | object | No | PSMDB represents additional features statuses for the PSMDB engine. |

