# GET /pod-scheduling-policies

**Resource:** [Pod Scheduling Policy](../resources/Pod-Scheduling-Policy.md)
**List pod scheduling policies**
**Operation ID:** `listPodSchedulingPolicy`

This API lists all pod scheduling policies in the kubernetes cluster.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `engineType` | query | enum: pxc, psmdb, postgresql | No | Database engine type that Pod Scheduling Policy is applicable to. |
| `hasRules` | query | boolean | No | Return list of Pod Scheduling Policy that has at least 1 rule. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[PodSchedulingPolicyList](../schemas/Pod/PodSchedulingPolicyList.md)

