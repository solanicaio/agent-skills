# POST /load-balancer-configs

**Resource:** [Load Balancer Config](../resources/Load-Balancer-Config.md)
**Create load balancer config**
**Operation ID:** `createLoadBalancerConfig`

This API creates a new load balancer config.


## Request Body

The load balancer config object to be created

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

