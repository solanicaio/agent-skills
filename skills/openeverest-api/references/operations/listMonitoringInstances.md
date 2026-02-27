# GET /namespaces/{namespace}/monitoring-instances

**Resource:** [Monitoring](../resources/Monitoring.md)
**List monitoring instances**
**Operation ID:** `listMonitoringInstances`

This API lists all monitoring instances in a given namespace.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Namespace of the backup storage |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[MonitoringInstancesList](../schemas/Monitoring/MonitoringInstancesList.md)

