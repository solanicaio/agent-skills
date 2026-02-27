# PUT /pod-scheduling-policies/{policy-name}

**Resource:** [Pod Scheduling Policy](../resources/Pod-Scheduling-Policy.md)
**Update pod scheduling policy**
**Operation ID:** `updatePodSchedulingPolicy`

This API updates a pod scheduling policy specified by the `name`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `policy-name` | path | string | Yes | Name of the pod scheduling policy. Can be found under Metadata["name"] of the PodSchedulingPolicy object. |

## Request Body

The pod scheduling policy object to be updated

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [PodSchedulingPolicy](../schemas/Pod/PodSchedulingPolicy.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[PodSchedulingPolicy](../schemas/Pod/PodSchedulingPolicy.md)

