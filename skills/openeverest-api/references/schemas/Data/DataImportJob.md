# DataImportJob

DataImportJob is the schema for the dataimportjobs API.

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `apiVersion` | string | No | APIVersion defines the versioned schema of this representation of an object.
Servers should convert recognized schemas to the latest internal value, and
may reject unrecognized values.
More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#resources |
| `kind` | string | No | Kind is a string value representing the REST resource this object represents.
Servers may infer this from the endpoint the client submits requests to.
Cannot be updated.
In CamelCase.
More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#types-kinds |
| `metadata` | object | No |  |
| `spec` | object | No |  |
| `status` | object | No |  |

## Nested Fields

### `spec`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `config` | object | No | Config defines the configuration for the data import job.
These options are specific to the DataImporter being used and must conform to
the schema defined in the DataImporter's .spec.config.openAPIV3Schema. |
| `dataImporterName` | string | Yes | DataImporterName is the data importer to use for the import. |
| `source` | object | Yes | Source is the source of the data to import. |
| `targetClusterName` | string | Yes | TargetClusterName is the reference to the target cluster. |

#### `spec.source`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `path` | string | No | Path is the path to the directory to import the data from.
This may be a path to a file or a directory, depending on the data importer. |
| `s3` | object | No | S3 contains the S3 information for the data import. |

### `status`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `completedAt` | string (date-time) | No | CompletedAt is the time when the data import job completed successfully. |
| `jobName` | string | No | JobName is the reference to the job that is running the data import. |
| `lastObservedGeneration` | integer (int64) | No | LastObservedGeneration is the last observed generation of the data import job. |
| `message` | string | No | Message is the message of the data import job. |
| `startedAt` | string (date-time) | No | StartedAt is the time when the data import job started. |
| `state` | string | No | State is the current state of the data import job. |

