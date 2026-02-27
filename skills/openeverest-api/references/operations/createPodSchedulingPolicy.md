# POST /pod-scheduling-policies

**Resource:** [Pod Scheduling Policy](../resources/Pod-Scheduling-Policy.md)
**Create pod scheduling policy**
**Operation ID:** `createPodSchedulingPolicy`

This API creates a new pod scheduling policy.


## Request Body

The pod scheduling policy object to be created

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

