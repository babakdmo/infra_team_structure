# **Data Platform Team**

## 🧾 Team Summary

| Area | Responsibilities |
|------|------------------|
| **Services Owned** | HDFS, YARN, Spark, Airflow, Kafka, ZooKeeper (on Kubernetes) |
| **Deployment & Upgrades** | Helm charts, Operators, rolling upgrades for zero downtime |
| **Configuration** | JVM tuning, Spark executor resources, Airflow concurrency |
| **Security** | FreeIPA/Kerberos integration, TLS certificates, NetworkPolicies |
| **Monitoring** | Prometheus, Grafana, Loki, custom alerts |
| **Backup & DR** | Snapshots, failover scripts, disaster recovery testing |

---

## 🔧 Owns:
- HDFS
- YARN
- Airflow
- Spark
- ZooKeeper
- Kafka  
(All deployed and managed on Kubernetes)

---

## 🧩 Core Responsibilities

### 1. Service Deployment & Upgrades
- Package and deploy services using Helm charts or Operators:
  - HDFS NameNode/DataNode
  - Spark Operator
  - Airflow with KubernetesExecutor
  - Kafka and ZooKeeper clusters
- Plan and execute **rolling upgrades** for Hadoop, Spark, and Airflow to ensure **zero downtime**.

### 2. Configuration & Tuning
- Tune HDFS replication, JVM GC settings for NameNode.
- Configure Spark executor memory and core settings.
- Tune Airflow parallelism and DAG concurrency.
- Manage YARN queue capacities and scheduler settings (FIFO vs FAIR).

### 3. Security & Access
- Integrate FreeIPA/Kerberos inside Kubernetes pods for HDFS/YARN auth.
- Issue and rotate TLS certs for internal services.
- Apply Kubernetes NetworkPolicies for inter-service access control.

### 4. Observability & Alerting
- Deploy Prometheus exporters for:
  - HDFS
  - YARN
  - Spark
- Set up Grafana dashboards and Loki/EFK for logging.
- Define alerts for:
  - Disk saturation
  - Failed jobs
  - Scheduler throughput drops

### 5. Backup, Recovery & Disaster Recovery (DR)
- Automate:
  - HDFS NameNode metadata snapshots (fsimage/JN edits)
  - Airflow DB dumps
- Script:
  - NameNode failover
  - ZooKeeper quorum recovery
- Quarterly test of restore and recovery processes.

---

## 📋 Sample Subtasks

| Subtask | Framework / Tool |
|---------|-------------------|
| Install HDFS via Helm and configure DataNode volumes | Helm, Kubernetes CSI |
| Deploy SparkOperator and submit PySpark job with dynamic allocation | Spark Operator |
| Setup Airflow with PostgreSQL backend and Git-based DAG sync | Airflow Helm Chart, GitSync |
| Create PrometheusRule for HDFS under-replicated blocks and Slack alerts | Prometheus, Alertmanager |
| Schedule daily Airflow metadata backup to S3 (MinIO) | Kubernetes CronJob, MinIO CSI |


# **Data Engineering Team**

## 🧾 Team Summary

| Area | Responsibilities |
|------|------------------|
| **Scope** | Batch and stream ingestion into data lakehouses; first-class ETL/ELT transforms to storage cluster |
| **Pipeline Types** | Batch and stream pipelines (PySpark + Spark SQL) for ingestion and pre-warehouse transformations |
| **CI/CD** | GitLab CI for DAG validation, job tests, image builds, and GitOps deployment |
| **Lineage & Metadata** | DataHub for column-level lineage, usage tracking, schema registry, and ownership tagging |
| **Quality** | Great Expectations checks, freshness validation, SLA-based alerts |
| **On-Call** | PagerDuty-based rotation for failure handling and SLA violations |

---

## 🔧 Owns:
- Batch and stream ingestion jobs
- PySpark & Spark SQL-based transformation pipelines
- Airflow DAGs for orchestration
- GitLab CI pipelines for continuous delivery
- Great Expectations suites for validation
- DataHub for end-to-end lineage and metadata
- Lakehouse table formats (Iceberg) and catalogs (Hive Metastore, Nessie)

---

## 🧩 Core Responsibilities

### 1. Batch & Stream Ingestion (Lakehouse Load)
- Ingest ETL/ELT data from batch and stream sources directly into the data lakehouse.
- Operate and maintain Kafka Connect clusters and Debezium connectors for real-time CDC.
- Detect schema drift, log changes, and trigger upstream notifications via GitLab issues.

### 2. First-Class Transformations
- Use **PySpark** and **Spark SQL** to perform scalable, first-class transformations during ingestion.
- Enrich, deduplicate, and validate data before it is written to Iceberg-based lakehouse tables.
- Design and manage schema evolution and partitioning strategies in **Iceberg** using **Hive Metastore** and **Project Nessie** catalogs.

### 3. Workflow Orchestration
- Author robust **Apache Airflow DAGs** supporting backfills, SLAs, retries, branching, and parametrization.
- Automate validation, testing, and deployment of pipelines using **GitLab CI** and **GitOps** practices.

### 4. Data Quality & Lineage
- Define and execute **Great Expectations** checks for completeness, accuracy, and business rules.
- Use **DataHub** to register lineage and metadata from PySpark, Spark SQL, dbt, and Airflow pipelines.
- Enforce structured metadata: ownership, sensitivity tagging, and field-level masking policies.

### 5. Monitoring & SLA Enforcement
- Track pipeline metrics like lag, freshness, and row volumes via **Prometheus**.
- Trigger alerts using custom **PrometheusRules** and **Alertmanager** integrations.
- Respond to incidents with a documented on-call process, runbooks, and postmortem workflows.

---

## 📋 Sample Subtasks

| Subtask | Framework / Tool |
|---------|-------------------|
| Configure Kafka Connect for CDC streaming from Postgres | Kafka Connect, Debezium |
| Build PySpark transformation for deduplicating and enriching product catalog | PySpark, Spark SQL |
| Write transformed output as Iceberg tables with Hive/Nessie catalog | Iceberg, Hive Metastore, Nessie |
| Define Great Expectations suite for validating null-free and non-negative metrics | Great Expectations |
| Automate DAG container build and deploy via GitLab CI to Kubernetes | GitLab CI, Airflow |
| Emit lineage metadata from Spark jobs and Airflow DAGs to DataHub | DataHub SDK, PySpark, Airflow |
