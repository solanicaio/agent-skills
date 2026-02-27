# Database Cluster

Everything related to the Database Clusters

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/namespaces/{namespace}/database-clusters` | List database clusters | [View](../operations/listDatabaseClusters.md) |
| POST | `/namespaces/{namespace}/database-clusters` | Create database cluster | [View](../operations/createDatabaseCluster.md) |
| GET | `/namespaces/{namespace}/database-clusters/{name}` | Get database cluster | [View](../operations/getDatabaseCluster.md) |
| PUT | `/namespaces/{namespace}/database-clusters/{name}` | Update database cluster | [View](../operations/updateDatabaseCluster.md) |
| DELETE | `/namespaces/{namespace}/database-clusters/{name}` | Delete database cluster | [View](../operations/deleteDatabaseCluster.md) |
| GET | `/namespaces/{namespace}/database-clusters/{name}/credentials` | Get database cluster credentials | [View](../operations/getDatabaseClusterCredentials.md) |
| GET | `/namespaces/{namespace}/database-clusters/{name}/pitr` | Get the Point-in-Time recovery info | [View](../operations/getDatabaseClusterPitr.md) |
| GET | `/namespaces/{namespace}/database-clusters/{name}/components` | Get database cluster components | [View](../operations/getDatabaseClusterComponents.md) |
| GET | `/namespaces/{namespace}/database-clusters/{name}/components/{component_name}/logs` | Get database cluster component logs | [View](../operations/getDatabaseClusterComponentLogs.md) |
| GET | `/namespaces/{namespace}/database-clusters/{dbName}/data-import-jobs` | List data import jobs for a database cluster | [View](../operations/listDataImportJobs.md) |
| POST | `/namespaces/{namespace}/database-clusters/{dbName}/secret` | Create a secret for the given database cluster | [View](../operations/createDatabaseClusterSecret.md) |
