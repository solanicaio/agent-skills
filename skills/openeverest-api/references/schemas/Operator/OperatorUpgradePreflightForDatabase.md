# OperatorUpgradePreflightForDatabase

Operator upgrade preflight check results for a database

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | No | Name of the database cluster |
| `message` | string | No |  |
| `pendingTask` | enum: ready, notReady, restart... | No | Pending task for the database cluster |

