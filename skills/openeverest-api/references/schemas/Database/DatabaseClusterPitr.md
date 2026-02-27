# DatabaseClusterPitr

point-in-time recovery related data

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `earliestDate` | string (date-time) | No |  |
| `latestDate` | string (date-time) | No |  |
| `latestBackupName` | string | No |  |
| `gaps` | boolean | No | indicates if there are pitr logs gaps detected after this backup was taken |

