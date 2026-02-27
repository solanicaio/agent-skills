# DELETE /namespaces/{namespace}/engine-features/split-horizon-dns-configs/{name}

**Resource:** [SplitHorizonDNSConfig](../resources/SplitHorizonDNSConfig.md)
**Delete Split-Horizon DNS Config instance.**
**Operation ID:** `deleteSplitHorizonDNSConfig`

This API deletes the Split-Horizon DNS Config instance specified by the `name`.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `name` | path | string | Yes | Name of the Split-Horizon DNS Config instance. |
| `namespace` | path | string | Yes | Namespace of the Split-Horizon DNS Config instance. |

## Responses

| Status | Description |
|--------|-------------|
| 204 | Successful operation |
| 400 | Unsuccessful operation |
| 404 | Split-Horizon DNS Config instance not found |
| 500 | Internal server error |

