# PATCH /namespaces/{namespace}/monitoring-instances/{name}

**Resource:** [Monitoring](../resources/Monitoring.md)
**Update monitoring instance**
**Operation ID:** `updateMonitoringInstance`

This API updates the monitoring instance specified by the `name`.

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `name` | path | string | Yes | Name of the monitoring instance |
| `namespace` | path | string | Yes | Namespace of the Monitoring instance |

## Request Body

The monitoring instance object to be updated.

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [MonitoringInstanceUpdateParams](../schemas/Monitoring/MonitoringInstanceUpdateParams.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 404 | Monitoring instance not found |
| 500 | Internal server error |

**Success Response Schema:**

[MonitoringInstance](../schemas/Monitoring/MonitoringInstance.md)

