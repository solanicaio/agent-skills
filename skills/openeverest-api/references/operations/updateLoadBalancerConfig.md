# PUT /load-balancer-configs/{config-name}

**Resource:** [Load Balancer Config](../resources/Load-Balancer-Config.md)
**Update load balancer config**
**Operation ID:** `updateLoadBalancerConfig`

This API updates a load balancer config specified by the `name`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `config-name` | path | string | Yes | Name of the load balancer config. Can be found under Metadata["name"] of the LoadBalancerConfig object. |

## Request Body

The load balancer config object to be updated

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [LoadBalancerConfig](../schemas/Load/LoadBalancerConfig.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[LoadBalancerConfig](../schemas/Load/LoadBalancerConfig.md)

