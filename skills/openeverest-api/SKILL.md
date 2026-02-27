---
name: openeverest-api
description: OpenEverest API operations guide. Use this skill when interacting with OpenEverest endpoints for authentication, database cluster lifecycle management, backups/restores, monitoring, infrastructure policies, and related schema-driven requests.
license: Apache-2.0
metadata:
  author: solanica
  version: "1.0.0"
  organization: Solanica
  date: February 2026
  abstract: Comprehensive OpenEverest API skill for self-hosted deployments. Includes authentication guidance, resource indexes, operation-level request/response details, and schema references for accurate agent-driven API execution across database clusters, backups, restores, monitoring, scheduling, load balancing, and DNS configuration.
  api-version: "1.0.0"
  openapi-version: "3.0.2"
---

# OpenEverest schema

# Authentication

## How to Use This Skill

This API documentation is split into multiple files for on-demand loading.

**Directory structure:**
```
references/
├── resources/      # 14 resource index files
├── operations/     # 59 operation detail files
└── schemas/        # 27 schema groups, 61 schema files
```

**Navigation flow:**
1. Find the resource you need in the list below
2. Read `references/resources/<resource>.md` to see available operations
3. Read `references/operations/<operation>.md` for full details
4. If an operation references a schema, read `references/schemas/<prefix>/<schema>.md`

## Base URL

- `/v1`

## Authentication

Supported methods: **BearerAuth**. See `references/authentication.md` for details.

## API endpoints

OpenEverest is a self-hosted platform. The API endpoints are determined by the installation and are not fixed. Please refer to your OpenEverest installation documentation for the correct base URL and endpoints. This skill requires the user to provide the correct API endpoint for their OpenEverest installation when making requests.

## Resources

- **Database Cluster** → `references/resources/Database-Cluster.md` (11 ops) - Everything related to the Database Clusters
- **Restore** → `references/resources/Restore.md` (5 ops) - Everything related to the Database Cluster Restore
- **Backup Storage** → `references/resources/Backup-Storage.md` (5 ops) - Everything related to the Backup storage
- **Monitoring** → `references/resources/Monitoring.md` (5 ops) - Everything related to monitoring
- **Pod Scheduling Policy** → `references/resources/Pod-Scheduling-Policy.md` (5 ops) - Everything related to policies for allocating DB c
- **Load Balancer Config** → `references/resources/Load-Balancer-Config.md` (5 ops)
- **SplitHorizonDNSConfig** → `references/resources/SplitHorizonDNSConfig.md` (5 ops)
- **Backup** → `references/resources/Backup.md` (4 ops) - Everything related to the Database Cluster Backups
- **Authentication & Authorization** → `references/resources/Authentication-Authorization.md` (3 ops) - Everything related to authentication and authoriza
- **General info** → `references/resources/General-info.md` (3 ops) - General information about the Everest installation
- **Database Engine** → `references/resources/Database-Engine.md` (3 ops) - Everything related to the Database Engines
- **Kubernetes** → `references/resources/Kubernetes.md` (2 ops) - Everything related to the Kubernetes Clusters
- **Operators** → `references/resources/Operators.md` (2 ops) - Everything related to the Database Engine Operator
- **Data Importer** → `references/resources/Data-Importer.md` (1 ops)
