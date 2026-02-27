# POST /namespaces/{namespace}/monitoring-instances

**Resource:** [Monitoring](../resources/Monitoring.md)
**Create monitoring instance**
**Operation ID:** `createMonitoringInstance`

This API creates a new monitoring instance.

A monitoring instance object requires `type` to be set.
Based on the `type` the respective key with configuration needs to be set.
Such as, if `type: pmm`, then `pmm` key needs to be provided with a configuration.


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Namespace of the backup storage |

## Request Body

The Monitoring instance object to be created

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [MonitoringInstanceCreateParams](../schemas/Monitoring/MonitoringInstanceCreateParams.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[MonitoringInstance](../schemas/Monitoring/MonitoringInstance.md)

