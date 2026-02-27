# GET /namespaces/{namespace}/database-clusters/{dbName}/data-import-jobs

**Resource:** [Database Cluster](../resources/Database-Cluster.md)
**List data import jobs for a database cluster**
**Operation ID:** `listDataImportJobs`

This API lists all data import jobs for the database cluster specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `dbName` | path | string | Yes | Name of the database cluster. Can be found under Metadata["name"] of the DatabaseCluster object. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DataImportJobList](../schemas/Data/DataImportJobList.md)

