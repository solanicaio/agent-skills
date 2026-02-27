# GET /load-balancer-configs

**Resource:** [Load Balancer Config](../resources/Load-Balancer-Config.md)
**List load balancer configs**
**Operation ID:** `listLoadBalancerConfig`

This API lists all load balancer configs in the kubernetes cluster.


## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[LoadBalancerConfigList](../schemas/Load/LoadBalancerConfigList.md)

