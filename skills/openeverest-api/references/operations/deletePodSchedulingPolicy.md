# DELETE /pod-scheduling-policies/{policy-name}

**Resource:** [Pod Scheduling Policy](../resources/Pod-Scheduling-Policy.md)
**Delete pod scheduling policy**
**Operation ID:** `deletePodSchedulingPolicy`

This API deletes the pod scheduling policy specified by the `name`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `policy-name` | path | string | Yes | Name of the pod scheduling policy. Can be found under Metadata["name"] of the PodSchedulingPolicy object. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[io.k8s.apimachinery.pkg.apis.meta.v1.Status_v2](../schemas/io-k8s-apimachinery-pkg-apis-meta-v1-Status/io-k8s-apimachinery-pkg-apis-meta-v1-Status-v2.md)

