# SplitHorizonDNSConfig

SplitHorizonDNSConfig is the Schema for the splithorizondnsconfigs API.

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
| `spec` | object | Yes | Spec defines the desired state of SplitHorizonDNSConfig |
| `status` | object | No | Status defines the observed state of SplitHorizonDNSConfig |

## Nested Fields

### `spec`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `baseDomainNameSuffix` | string | Yes | BaseDomainNameSuffix is the base domain name suffix for generating domain names for each Pod in ReplicaSet.
It should be a valid domain name suffix. |
| `tls` | object | Yes | TLS is the TLS configuration for the split-horizon DNS configuration. |

#### `spec.tls`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `certificate` | object | No | Certificate is the TLS certificate and key for the split-horizon DNS configuration. |
| `secretName` | string | Yes | SecretName is the name of the secret containing the TLS certificate and key for the split-horizon DNS configuration. |

### `status`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `inUse` | boolean | No | InUse is a flag that indicates if the config is used by any DB cluster. |
| `lastObservedGeneration` | integer (int64) | No | LastObservedGeneration is the most recent generation observed for this SplitHorizonDNSConfig. |

