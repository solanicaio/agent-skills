# LoadBalancerConfig

LoadBalancerConfig is the Schema for the Load Balancer Config API.

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
| `spec` | object | No | LoadBalancerConfigSpec defines the desired state of LoadBalancerConfig. |
| `status` | object | No | LoadBalancerConfigStatus defines the observed state of LoadBalancerConfig. |

## Nested Fields

### `spec`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `annotations` | object | No | Annotations key-value pairs to apply as annotations to the load balancer |

### `status`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `inUse` | boolean | No | InUse is a flag that indicates if the config is used by any DB cluster. |
| `lastObservedGeneration` | integer (int64) | No | LastObservedGeneration is the most recent generation observed for this LoadBalancerConfig. |

