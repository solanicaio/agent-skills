# PodSchedulingPolicy

PodSchedulingPolicy is the Schema for the Pod Scheduling Policy API.

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
| `spec` | object | No | PodSchedulingPolicySpec defines the desired state of PodSchedulingPolicy. |
| `status` | object | No | PodSchedulingPolicyStatus defines the observed state of PodSchedulingPolicy. |

## Nested Fields

### `spec`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `affinityConfig` | object | No | AffinityConfig is a configuration for the affinity settings depending on the engine type. |
| `engineType` | enum: pxc, postgresql, psmdb | Yes | EngineType is type of DB engine that this policy can be applied to. |

#### `spec.affinityConfig`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `postgresql` | object | No | PostgreSQL is the affinity configuration for the PostgreSQL DB clusters. |
| `psmdb` | object | No | PSMDB is the affinity configuration for the PSMDB DB clusters. |
| `pxc` | object | No | PXC is the affinity configuration for the PXC DB clusters. |

### `status`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `inUse` | boolean | No | InUse is a flag that indicates if the policy is used by any DB cluster. |
| `lastObservedGeneration` | integer (int64) | No | LastObservedGeneration is the most recent generation observed for this PodSchedulingPolicy. |

