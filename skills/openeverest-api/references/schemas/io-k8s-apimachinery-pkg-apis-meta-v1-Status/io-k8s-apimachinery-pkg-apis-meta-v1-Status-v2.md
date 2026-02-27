# io.k8s.apimachinery.pkg.apis.meta.v1.Status_v2

Status is a return value for calls that don't return other objects.

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `apiVersion` | string | No | APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#resources |
| `code` | integer (int32) | No | Suggested HTTP return code for this status, 0 if not set. |
| `details` | [io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails_v2](io-k8s-apimachinery-pkg-apis-meta-v1-StatusDetails-v2.md) | No |  |
| `kind` | string | No | Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#types-kinds |
| `message` | string | No | A human-readable description of the status of this operation. |
| `metadata` | [io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta](io-k8s-apimachinery-pkg-apis-meta-v1-ListMeta.md) | No |  |
| `reason` | string | No | A machine-readable description of why this operation is in the "Failure" status. If this value is empty there is no information available. A Reason clarifies an HTTP status code but does not override it. |
| `status` | string | No | Status of the operation. One of: "Success" or "Failure". More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#spec-and-status |

