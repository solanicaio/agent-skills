# POST /namespaces/{namespace}/database-clusters/{dbName}/secret

**Resource:** [Database Cluster](../resources/Database-Cluster.md)
**Create a secret for the given database cluster**
**Operation ID:** `createDatabaseClusterSecret`

This API creates a secret for the database cluster specified by the `name` and `namespace`


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `dbName` | path | string | Yes | Name of the database cluster |
| `namespace` | path | string | Yes | Name of the namespace |
| `secretName` | query | string | No | Optional name of the secret to be created. If not provided, a random name will be generated. |

## Request Body

The Secret object to be created

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [Secret](../schemas/Secret/Secret.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[Secret](../schemas/Secret/Secret.md)

