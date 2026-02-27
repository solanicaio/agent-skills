# GET /namespaces/{namespace}/monitoring-instances/{name}

**Resource:** [Monitoring](../resources/Monitoring.md)
**Get monitoring instance**
**Operation ID:** `getMonitoringInstance`

This API gets the monitoring instance specified by the `name`.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `name` | path | string | Yes | Name of the Monitoring instance |
| `namespace` | path | string | Yes | Namespace of the Monitoring instance |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 404 | Monitoring instance not found |
| 500 | Internal server error |

**Success Response Schema:**

[MonitoringInstance](../schemas/Monitoring/MonitoringInstance.md)

