# POST /namespaces/{namespace}/database-engines/upgrade-plan/approval

**Resource:** [Operators](../resources/Operators.md)
**Upgrade database engine operators**
**Operation ID:** `approveUpgradePlan`

This API upgrades all database engine operators in the specified namespace.

Added in v1.1.0, it is recommended to use this API for operator upgrades.
The older upgrade APIs are deprecated and will be removed in v1.2.0


## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `namespace` | path | string | Yes | Name of the namespace |

## Request Body

Request for upgrading the database engine operators

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [UpgradePlanApproval](../schemas/Upgrade/UpgradePlanApproval.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successful operation |
| 400 | Unsuccessful operation |
| 500 | Internal server error |

