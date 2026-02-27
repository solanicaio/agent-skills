# GET /namespaces/{namespace}/database-clusters/{name}/credentials

**Resource:** [Database Cluster](../resources/Database-Cluster.md)
**Get database cluster credentials**
**Operation ID:** `getDatabaseClusterCredentials`

This API gets the credentials for the database cluster specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `name` | path | string | Yes | Name of the database cluster. Can be found under Metadata["name"] of the DatabaseCluster object. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DatabaseClusterCredential](../schemas/Database/DatabaseClusterCredential.md)

