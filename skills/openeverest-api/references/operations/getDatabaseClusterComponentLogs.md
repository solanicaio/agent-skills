# GET /namespaces/{namespace}/database-clusters/{name}/components/{component_name}/logs

**Resource:** [Database Cluster](../resources/Database-Cluster.md)
**Get database cluster component logs**
**Operation ID:** `getDatabaseClusterComponentLogs`

This API gets the logs of the component specified by the `component_name` of the database cluster specified by the `name` and `namespace`.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |
| `name` | path | string | Yes | Name of the database cluster. Can be found under Metadata["name"] of the DatabaseCluster object. |
| `component_name` | path | string | Yes | Name of the component. |
| `container` | query | string | No | Container name. If omitted, the first container in the pod spec is used. |
| `follow` | query | boolean | No | Stream logs continuously |
| `tailLines` | query | integer | No | Number of lines from the end of the logs to show |
| `sinceSeconds` | query | integer | No | Return logs newer than this many seconds |
| `sinceTime` | query | string (date-time) | No | RFC3339 timestamp to start logs from |
| `timestamps` | query | boolean | No | Include timestamps in log lines |
| `previous` | query | boolean | No | Return logs from the previous container instance |
| `limitBytes` | query | integer | No | Maximum bytes to return |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

