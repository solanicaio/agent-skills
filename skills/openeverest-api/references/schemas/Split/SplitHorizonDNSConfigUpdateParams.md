# SplitHorizonDNSConfigUpdateParams

SplitHorizonDNSConfigUpdateParams is the Schema for the splithorizondnsconfigs update API.

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `baseDomainNameSuffix` | string | No | BaseDomainNameSuffix is the base domain name suffix for generating domain names for each Pod in ReplicaSet.
It should be a valid domain name suffix. |
| `certificate` | object | No | Certificate is the TLS certificate and key for the split-horizon DNS configuration. |

## Nested Fields

### `certificate`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ca.crt` | string | Yes | CACert is based64 encoded ca.pem file content.
It is provided as a write-only input field for convenience.
When this field is set, a webhook writes this value in the Secret specified by `.spec.tls.secretName`
and empties this field.
This field is not stored in the API. |
| `ca.key` | string | Yes | CAKey is based64 encoded ca-key.pem file content.
It is provided as a write-only input field for convenience.
When this field is set, a webhook writes this value in the Secret specified by `.spec.tls.secretName`
and empties this field.
This field is not stored in the API. |

