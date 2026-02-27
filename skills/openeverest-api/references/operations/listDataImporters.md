# GET /data-importers

**Resource:** [Data Importer](../resources/Data-Importer.md)
**List data importers**
**Operation ID:** `listDataImporters`

This API lists all data importers in the kubernetes cluster.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `supportedEngines` | query | string[] | No | Filter data importers by supported database engine type. Accepts a comma-separated list. |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[DataImporterList](../schemas/Data/DataImporterList.md)

