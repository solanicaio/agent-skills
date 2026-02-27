# GET /namespaces/{namespace}/database-engines/upgrade-plan

**Resource:** [Operators](../resources/Operators.md)
**Get upgrade plan**
**Operation ID:** `getUpgradePlan`

This API lists pending operator upgrades in the given namespace.

Additionally, it also returns a list of pending action items that need to be performed 
before and after upgrading a database operator.

Added in v1.1.0, it is recommended to use this API for operator upgrades.
The older upgrade APIs are deprecated and will be removed in v1.2.0


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

**Success Response Schema:**

[UpgradePlan](../schemas/Upgrade/UpgradePlan.md)

