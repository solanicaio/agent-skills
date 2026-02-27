# DataImporter

DataImporter defines a reusable strategy for importing data into a DatabaseCluster.

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
| `spec` | object | No | DataImporterSpec defines the specification of a DataImporter. |
| `status` | object | No |  |

## Nested Fields

### `spec`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `clusterPermissions` | object[] | No | ClusterPermissions defines the cluster-wide permissions required by the data importer.
These permissions are used to generate a ClusterRole for the data importer job. |
| `config` | object | No | Config contains additional configuration defined for the data importer. |
| `databaseClusterConstraints` | object | No | DatabaseClusterConstraints defines compatibility requirements and prerequisites that must be satisfied
by a DatabaseCluster before this data importer can be used with it. This allows the data importer to
express specific requirements about the database configuration needed for successful import operations,
such as required database fields, specific engine configurations, or other database properties.
When a DatabaseCluster references this data importer, the operator will validate the DatabaseCluster
against these constraints before proceeding with the import operation. |
| `description` | string | No | Description is the description of the data importer. |
| `displayName` | string | No | DisplayName is a human-readable name for the data importer. |
| `jobSpec` | object | No | JobSpec is the specification of the data importer job. |
| `permissions` | object[] | No | Permissions defines the permissions required by the data importer.
These permissions are used to generate a Role for the data importer job. |
| `supportedEngines` | string[] | No | SupportedEngines is the list of engines that the data importer supports. |

#### `spec.clusterPermissions`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `apiGroups` | string[] | No | APIGroups is the name of the APIGroup that contains the resources.  If multiple API groups are specified, any action requested against one of
the enumerated resources in any API group will be allowed. "" represents the core API group and "*" represents all API groups. |
| `nonResourceURLs` | string[] | No | NonResourceURLs is a set of partial urls that a user should have access to.  *s are allowed, but only as the full, final step in the path
Since non-resource URLs are not namespaced, this field is only applicable for ClusterRoles referenced from a ClusterRoleBinding.
Rules can either apply to API resources (such as "pods" or "secrets") or non-resource URL paths (such as "/api"),  but not both. |
| `resourceNames` | string[] | No | ResourceNames is an optional white list of names that the rule applies to.  An empty set means that everything is allowed. |
| `resources` | string[] | No | Resources is a list of resources this rule applies to. '*' represents all resources. |
| `verbs` | string[] | Yes | Verbs is a list of Verbs that apply to ALL the ResourceKinds contained in this rule. '*' represents all verbs. |

#### `spec.config`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `openAPIV3Schema` | any | No | OpenAPIV3Schema is the OpenAPI v3 schema of the data importer. |

#### `spec.databaseClusterConstraints`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `requiredFields` | string[] | No | RequiredFields contains a list of fields that must be set in the DatabaseCluster spec.
Each key is a JSON path expressions that points to a field in the DatabaseCluster spec.
For example, ".spec.engine.type" or ".spec.dataSource.dataImport.config.someField". |

#### `spec.jobSpec`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `command` | string[] | No | Command is the command to run the data importer. |
| `image` | string | No | Image is the image of the data importer. |

#### `spec.permissions`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `apiGroups` | string[] | No | APIGroups is the name of the APIGroup that contains the resources.  If multiple API groups are specified, any action requested against one of
the enumerated resources in any API group will be allowed. "" represents the core API group and "*" represents all API groups. |
| `nonResourceURLs` | string[] | No | NonResourceURLs is a set of partial urls that a user should have access to.  *s are allowed, but only as the full, final step in the path
Since non-resource URLs are not namespaced, this field is only applicable for ClusterRoles referenced from a ClusterRoleBinding.
Rules can either apply to API resources (such as "pods" or "secrets") or non-resource URL paths (such as "/api"),  but not both. |
| `resourceNames` | string[] | No | ResourceNames is an optional white list of names that the rule applies to.  An empty set means that everything is allowed. |
| `resources` | string[] | No | Resources is a list of resources this rule applies to. '*' represents all resources. |
| `verbs` | string[] | Yes | Verbs is a list of Verbs that apply to ALL the ResourceKinds contained in this rule. '*' represents all verbs. |

