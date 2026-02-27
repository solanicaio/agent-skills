# DELETE /load-balancer-configs/{config-name}

**Resource:** [Load Balancer Config](../resources/Load-Balancer-Config.md)
**Delete load balancer config**
**Operation ID:** `deleteLoadBalancerConfig`

This API deletes the load balancer config specified by the `name`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `config-name` | path | string | Yes | Name of the load balancer config. Can be found under Metadata["name"] of the LoadBalancerConfig object. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[io.k8s.apimachinery.pkg.apis.meta.v1.Status_v2](../schemas/io-k8s-apimachinery-pkg-apis-meta-v1-Status/io-k8s-apimachinery-pkg-apis-meta-v1-Status-v2.md)

