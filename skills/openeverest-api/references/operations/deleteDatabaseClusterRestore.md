# DELETE /namespaces/{namespace}/database-cluster-restores/{name}

**Resource:** [Restore](../resources/Restore.md)
**Delete database cluster restore**
**Operation ID:** `deleteDatabaseClusterRestore`

This API deletes the database cluster restore specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `name` | path | string | Yes | Name of the database cluster restore. Can be found under Metadata["name"] of the DatabaseClusterRestore object. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[io.k8s.apimachinery.pkg.apis.meta.v1.Status_v2](../schemas/io-k8s-apimachinery-pkg-apis-meta-v1-Status/io-k8s-apimachinery-pkg-apis-meta-v1-Status-v2.md)

