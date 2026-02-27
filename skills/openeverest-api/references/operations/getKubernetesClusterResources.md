# GET /resources

**Resource:** [Kubernetes](../resources/Kubernetes.md)
**Cluster resources**
**Operation ID:** `getKubernetesClusterResources`

This API gets the capacity and available resources of the Kubernetes cluster.


## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[KubernetesClusterResources](../schemas/Kubernetes/KubernetesClusterResources.md)

