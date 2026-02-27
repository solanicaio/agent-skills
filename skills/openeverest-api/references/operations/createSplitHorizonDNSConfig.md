# POST /namespaces/{namespace}/engine-features/split-horizon-dns-configs

**Resource:** [SplitHorizonDNSConfig](../resources/SplitHorizonDNSConfig.md)
**Create Split-Horizon DNS Config for PSMDB.**
**Operation ID:** `createSplitHorizonDNSConfig`

This API creates a new Split-Horizon DNS Config instance.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Namespace of the Split-Horizon DNS Config instance. |

## Request Body

The Split-Horizon DNS Config instance object to be created.

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [SplitHorizonDNSConfig](../schemas/Split/SplitHorizonDNSConfig.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[SplitHorizonDNSConfig](../schemas/Split/SplitHorizonDNSConfig.md)

