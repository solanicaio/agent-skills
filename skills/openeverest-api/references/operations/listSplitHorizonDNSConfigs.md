# GET /namespaces/{namespace}/engine-features/split-horizon-dns-configs

**Resource:** [SplitHorizonDNSConfig](../resources/SplitHorizonDNSConfig.md)
**List Split-Horizon DNS Config instances.**
**Operation ID:** `listSplitHorizonDNSConfigs`

This API lists all Split-Horizon DNS Config instances in a given namespace.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Namespace of the Split-Horizon DNS Config instance. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[SplitHorizonDNSConfigList](../schemas/Split/SplitHorizonDNSConfigList.md)

