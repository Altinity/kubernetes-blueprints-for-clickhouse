# clickhouse-eks

![Version: 0.1.3](https://img.shields.io/badge/Version-0.1.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for ClickHouse running on AWS EKS across AZs using a nodeSelector to pin resources to run on specific VMs types

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| all.metadata.labels.application_group | string | `"eks"` | The name of the application group |
| clickhouse.cluster | string | `"dev"` | Cluster name |
| clickhouse.image | string | `"altinity/clickhouse-server:23.8.8.21.altinitystable"` | ClickHouse server image |
| clickhouse.keeper_name | string | `"keeper-eks"` | Name of the keeper cluster |
| clickhouse.name | string | `"eks"` | Metadata name |
| clickhouse.node_selector | string | `"m6i.large"` | AWS instance type |
| clickhouse.password | string | `nil` | ClickHouse user password |
| clickhouse.service_type | string | `"cluster-ip"` | Possible service types are `cluster-ip`, `internal-loadbalancer` and `external-loadbalancer` |
| clickhouse.storage | string | `"50Gi"` | Storage size for ClickHouse data |
| clickhouse.storage_class_name | string | `"gp2"` | Storage class for ClickHouse data |
| clickhouse.user | string | `"default"` | ClickHouse user name |
| clickhouse.zones | list | `["us-east-1a","us-east-1a","us-east-1c"]` | AWS availability zones for creating replicas |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.13.1](https://github.com/norwoodj/helm-docs/releases/v1.13.1)
