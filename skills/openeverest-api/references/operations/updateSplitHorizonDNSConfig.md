# PATCH /namespaces/{namespace}/engine-features/split-horizon-dns-configs/{name}

**Resource:** [SplitHorizonDNSConfig](../resources/SplitHorizonDNSConfig.md)
**Update Split-Horizon DNS Config instance.**
**Operation ID:** `updateSplitHorizonDNSConfig`

This API updates the Split-Horizon DNS Config instance specified by the `name`.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `name` | path | string | Yes | Name of the Split-Horizon DNS Config instance. |
| `namespace` | path | string | Yes | Namespace of the SplitHorizonDNSConfig instance. |

## Request Body

The Split-Horizon DNS Config instance object to be updated.

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [SplitHorizonDNSConfigUpdateParams](../schemas/Split/SplitHorizonDNSConfigUpdateParams.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 404 | Split-Horizon DNS Config instance not found |
| 500 | Internal server error |

**Success Response Schema:**

[SplitHorizonDNSConfig](../schemas/Split/SplitHorizonDNSConfig.md)

