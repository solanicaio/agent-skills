# GET /cluster-info

**Resource:** [Kubernetes](../resources/Kubernetes.md)
**Cluster info**
**Operation ID:** `getKubernetesClusterInfo`

This API gets the cluster type and the storage classes available in the cluster.


## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[KubernetesClusterInfo](../schemas/Kubernetes/KubernetesClusterInfo.md)

