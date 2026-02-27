# DELETE /namespaces/{namespace}/monitoring-instances/{name}

**Resource:** [Monitoring](../resources/Monitoring.md)
**Delete monitoring instnace**
**Operation ID:** `deleteMonitoringInstance`

This API deletes the monitoring instance specified by the `name`.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `name` | path | string | Yes | Name of the monitoring instance |
| `namespace` | path | string | Yes | Namespace of the Monitoring instance |

## Responses

| Status | Description |
|--------|-------------|
| 204 | Successful operation |
| 400 | Unsuccessful operation |
| 404 | Monitoring instance not found |
| 500 | Internal server error |

