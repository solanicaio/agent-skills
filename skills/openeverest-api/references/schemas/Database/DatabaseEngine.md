# DatabaseEngine

DatabaseEngine is the Schema for the databaseengines API.

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
| `spec` | object | No | DatabaseEngineSpec is a spec for a database engine. |
| `status` | object | No | DatabaseEngineStatus defines the observed state of DatabaseEngine. |

## Nested Fields

### `spec`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowedVersions` | string[] | No |  |
| `secretKeys` | object | No | SecretKeys contains the definition of the various Secrets that
the given DBEngine supports.
This information acts like metadata for the Everest UI to guide the users
in filling out the correct Secret keys for their clusters. |
| `type` | string | Yes | EngineType stands for the supported database engines. Right now it's only pxc
and psmdb. However, it can be ps, pg and any other source. |

#### `spec.secretKeys`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `user` | object[] | No | User secret keys are used to store the details of the users. |

### `status`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `availableVersions` | object | No | Versions struct represents available versions of database engine components. |
| `operatorUpgrade` | object | No | OperatorUpgrade contains the status of the operator upgrade. |
| `operatorVersion` | string | No |  |
| `pendingOperatorUpgrades` | object[] | No |  |
| `status` | string | No | EngineState represents state of engine in a k8s cluster. |

#### `status.availableVersions`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `backup` | object | No | ComponentsMap is a map of database engine components. |
| `engine` | object | No | ComponentsMap is a map of database engine components. |
| `proxy` | object | No |  |
| `tools` | object | No |  |

#### `status.operatorUpgrade`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `installPlanRef` | object | No | InstallPlanRef is a reference to the InstallPlan object created for the operator upgrade.

We do not recommended approving this InstallPlan directly from the Kubernetes API.
This is because this InstallPlan may also upgrade other operators in the namespace and that
can have unintended consequences.
This behaviour is not a bug from Everest, but an unfortunate limitation of OLM.
We suggest using the Everest API/UI to handle operator upgrades, which will perform a series
of checks and safely upgrade all operators in the namespace. |
| `message` | string | No |  |
| `phase` | string | No | UpgradePhase represents the phase of the operator upgrade. |
| `startedAt` | string (date-time) | No |  |
| `targetVersion` | string | No | TargetVersion is the version to which the operator should be upgraded. |

#### `status.pendingOperatorUpgrades`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `installPlanRef` | object | No | InstallPlanRef is a reference to the InstallPlan object created for the operator upgrade.

We do not recommended approving this InstallPlan directly from the Kubernetes API.
This is because this InstallPlan may also upgrade other operators in the namespace and that
can have unintended consequences.
This behaviour is not a bug from Everest, but an unfortunate limitation of OLM.
We suggest using the Everest API/UI to handle operator upgrades, which will perform a series
of checks and safely upgrade all operators in the namespace. |
| `targetVersion` | string | No | TargetVersion is the version to which the operator should be upgraded. |

