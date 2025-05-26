# **Data Infrastructure Team**

## Team Structure Overview

```
Data Infrastructure Team
├── Data Platform Team
│   ├── HDFS, YARN, Spark, Airflow, Kafka, ZooKeeper
│   ├── Helm-based deployments and upgrades
│   ├── Kerberos integration and TLS
│   └── Monitoring, Alerts, and Backup
├── Data Engineering Team
│   ├── Batch and stream ingestion (Lakehouse load)
│   ├── PySpark and Spark SQL transformations
│   ├── Airflow DAG orchestration with GitLab CI
│   ├── Great Expectations + DataHub for lineage
│   └── Auto-generation of data pipelines
├── MLOps Team
│   ├── Feature stores, MLflow, training pipelines (Ray, Kubeflow)
│   ├── Model serving (Seldon, Triton, Ollama) with autoscaling
│   ├── Monitoring and drift detection (Prometheus + Evidently)
│   ├── LangChain, LlamaIndex, Haystack orchestration
│   ├── LLM serving infrastructure (Ollama, vLLM, Triton)
│   └── Expose unified agent & RAG APIs with prompt registry
└── BI Services Team
    ├── Semantic metrics with dbt Metrics
    ├── Star schema and OLAP-wide tables on Lakehouse and StarRocks
    ├── Trino, StarRocks infrastructure
    ├── Superset/Looker dashboards, RLS embedding
    ├── Redis caching, materialized views
    └── Secondary pipelines + automated wide table generation
```
---
---

# **1- Data Platform Team**

## 🧾 Team Summary

| Area | Responsibilities |
|------|------------------|
| **Services Owned** | HDFS, YARN, Spark, Airflow, Kafka, ZooKeeper (on Kubernetes) |
| **Deployment & Upgrades** | Helm charts, Operators, rolling upgrades for zero downtime |
| **Configuration** | JVM tuning, Spark executor resources, Airflow concurrency |
| **Security** | FreeIPA/Kerberos integration, TLS certificates, NetworkPolicies |
| **Monitoring** | Prometheus, Grafana, custom alerts |
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

--- 
---
# **2- Data Engineering Team**

## 🧾 Team Summary

| Area | Responsibilities |
|------|------------------|
| **Scope** | Batch and stream ingestion into data lakehouses; first-class ETL/ELT transforms to storage cluster |
| **Pipeline Types** | Batch and stream pipelines (PySpark + Spark SQL) for ingestion and pre-warehouse transformations |
| **CI/CD** | GitLab CI for DAG validation, job tests, image builds, and GitOps deployment |
| **Lineage & Metadata** | DataHub for column-level lineage, usage tracking, schema registry, and ownership tagging |
| **Quality** | Great Expectations checks, freshness validation, SLA-based alerts |
| **Automation** | Auto-generation of batch and streaming pipelines using standardized templates and metadata |
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
- Pipeline generation tooling and automation logic

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

### 6. Automated Pipeline Generation
- Develop tooling for automatic generation of PySpark and Spark SQL batch/stream pipelines based on metadata, templates, and config files.
- Standardize ingestion and transformation logic for repeatable use across domains.
- Integrate generation logic into GitLab CI workflows and expose via internal developer platform APIs.

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
| Generate new Spark pipeline from metadata using internal template engine | Python, Jinja2, GitLab CI |

---
---
# **3- MLOps Team**

## 🧾 Team Summary

| Area | Responsibilities |
|------|------------------|
| **Scope** | Manage end-to-end ML lifecycle on Kubernetes: feature storage, training orchestration, registry, model serving, and drift monitoring |
| **Pipeline Types** | Automated training and deployment workflows using Argo, Kubeflow, or Airflow |
| **CI/CD** | GitLab CI for model validation, version control, image builds, and GitOps-based rollouts |
| **Drift & Monitoring** | Prometheus and Evidently AI for drift detection, latency and error monitoring |
| **Automation** | Auto-generation of ML pipelines using standardized templates and metadata inputs |
| **Serving** | Inference deployments using Seldon Core, KFServing, Triton Inference Server, or Ollama |
| **On-Call** | PagerDuty-based support for pipeline failures, drift breaches, and incident response |

---

## 🔧 Owns:
- Feature stores using Feast
- Model tracking and registries using MLflow or Weights & Biases
- Training orchestration using Argo Workflows, Kubeflow Pipelines, or Airflow
- Distributed training using Ray
- Model serving with Seldon Core, KFServing, Triton Inference Server, and Ollama
- Drift detection and inference monitoring
- GitLab CI pipelines for automated training and deployment
- Templates and tooling for pipeline auto-generation
- LLM and AI Agent Platform Services (LangChain, LlamaIndex, Haystack, Ollama)
- RAG APIs, prompt registry, memory services, and agent serving backend

---

## 🧩 Core Responsibilities

### 1. Feature Store Management
- Deploy and manage **Feast** on Kubernetes, supporting TTL, streaming joins, and batch backfills.
- Ensure consistency between training and serving-time feature lookups.
- Register, tag, and track feature usage across teams.

### 2. Experiment Tracking & Model Registry
- Operate **MLflow** or **Weights & Biases** as central model and metric repositories.
- Enforce model evaluation thresholds using CI gates.
- Promote models through lifecycle stages (`staging → validated → production`) using GitOps.

### 3. Training Pipelines & Orchestration
- Automate training pipelines using **Kubeflow Pipelines**, **Argo Workflows**, or **Apache Airflow**.
- Utilize **Ray** for distributed training with autoscaling GPU-enabled clusters.
- Chain steps for preprocessing, training, evaluation, containerization, and registry upload.

### 4. Serving & Deployment
- Deploy models using **Seldon Core**, **KFServing**, **Triton Inference Server**, or **Ollama**.
- Define and execute canary, shadow, and blue-green rollouts with **Istio** routing.
- Enforce inference endpoint security via API key authentication or Role-Level Security (RLS).

### 5. Monitoring & Drift Detection
- Track prediction latency, error rates, and feature drift with **Prometheus** and **Evidently AI**.
- Send drift alerts to **Grafana** dashboards or trigger retraining workflows via automation.
- Define SLA metrics and observability rules for inference behavior.

### 6. Automated Pipeline Generation
- Enable generation of training and deployment pipelines from configuration metadata.
- Use internal templates and declarative YAML to scaffold pipelines dynamically.
- Integrate pipeline generation with GitLab CI and internal developer tooling.

### 7. LLM and AI Agent Platform Services
- Deploy and manage backend infrastructure for agent frameworks: **LangChain**, **LlamaIndex**, **Haystack**.
- Host and serve LLMs using **vLLM**, **Triton**, or **Ollama**.
- Expose unified agent APIs such as `/chain/run`, `/rag/query`, and `/memory`.
- Maintain a **Prompt Registry** and **Chain Template Catalog** with versioning and tags.
- Provide vector store backends (e.g., **Weaviate**, **Qdrant**, **PGVector**) for retrieval-augmented generation.
- Manage agent memory and session context via Redis, MongoDB, or graph databases.
- Deliver observability, API security, RBAC, and usage analytics across all agent interfaces.

---

## 📋 Sample Subtasks

| Subtask | Framework / Tool |
|---------|-------------------|
| Deploy Feast Core and register “user_age” feature with TTL 24h | Feast, Kubernetes Operator |
| Configure MLflow server with backend store and GitLab CI model threshold check | MLflow, GitLab CI |
| Build distributed Ray training job triggered by Argo Workflow | Ray, Argo Workflows |
| Serve TensorFlow model via Triton Inference Server with autoscaling | Triton Server, Kubernetes |
| Serve LLM via Ollama with role-based inference access | Ollama, Kubernetes, FreeIPA |
| Setup Evidently monitor for drift on "transaction_amount" and notify Grafana | Evidently AI, Prometheus, Grafana |
| Auto-generate Kubeflow pipeline from metadata and deploy via GitLab CI | Python, Jinja2, GitLab CI, Kubeflow |
| Wrap LangChain agent and expose as REST endpoint with trace logging | LangChain, FastAPI, OpenTelemetry |
| Create REST and gRPC RAG APIs and agent interfaces to enable usage of LLM-based agents | LangChain, Haystack, LlamaIndex, Ollama |

---
---
# **4- BI Services Team (Infra-Level)**

## 🧾 Team Summary

| Area | Responsibilities |
|------|------------------|
| **Scope** | Manage data modeling, data warehouse architecture, OLAP-wide tables, semantic layers, dashboard platforms, and query infrastructure |
| **Modeling & Warehousing** | Design dimensional models, wide tables, and materialized layers on Lakehouse and OLAP |
| **Secondary Pipelines** | Build and automate pipelines that consume ETL outputs and populate BI models |
| **OLAP & Query Engines** | Operate Trino and StarRocks for low-latency, high-concurrency analytics |
| **Semantic Layer** | Define and manage metrics using dbt Metrics|
| **Dashboards** | Maintain and optimize Superset; Add new features |
| **Automation** | Automate secondary pipeline |

---

## 🔧 Owns:
- Data modeling and data warehouse design on the Lakehouse
- Creation of wide and aggregated OLAP tables using StarRocks
- Materialized view orchestration and refresh logic using Airflow
- Semantic metrics definitions using dbt Metrics
- Trino and StarRocks infrastructure and configuration
- dashboard delivery via Superset
- Dashboard performance monitoring, query optimization, and SLA enforcement
- Secondary pipelines for transforming curated ETL outputs into BI tables
- Tooling for auto-generating dashboard-ready data models and pipelines

---

## 🧩 Core Responsibilities

### 1. Data Modeling & Warehouse Architecture
- Design and maintain curated dimensional models in the Lakehouse (Iceberg).
- Develop OLAP-wide tables and aggregates in **StarRocks**.
- Version-control schemas and enforce compatibility via CI pipelines.

### 2. Semantic Layer & Metrics APIs
- Define **dbt Metrics** layers to standardize KPIs across the organization.
- Expose metrics through SQL and RESTful APIs to internal data consumers.
- Maintain backward compatibility and test business logic in metrics pipelines.

### 3. Secondary BI Pipelines
- Build and orchestrate pipelines that consume curated ETL output and produce:
  - Fact and dimension tables in the Lakehouse
  - OLAP-friendly wide tables and pre-aggregates in StarRocks
- Automate pipeline generation using YAML-based metadata and Jinja templates.

### 4. OLAP & Query Engines
- Deploy and tune **Trino** and **StarRocks** on Kubernetes.
- Manage compute resources, query memory, worker pools, and parallelism for concurrency.
- Optimize long-tail and hot-path queries using materialized layers and storage indexes.

### 5. Dashboarding Platforms & Embedding
- Maintain **Superset** platform; handle upgrades, auth, and scale.
- Implement row-level security (RLS) in dashboards and SDKs.
- Develop and publish JavaScript SDKs to embed dashboards in portals.
- Optimize chart rendering, data sources, and default filters for speed.

### 6. Caching & Materializations
- Implement **StarRocks materialized views** for low-latency reporting.
- Schedule refreshes based on upstream data events or timestamps.
- Monitor freshness SLAs for high-priority reports and visuals.

### 7. Monitoring & Performance Auditing
- Monitor BI workloads (query latency, memory, slow queries) using Prometheus and Grafana.
- Run weekly audits and apply optimizations (joins, indexes, filter pushdowns).
- Maintain visual performance benchmarks and SLA dashboards.

---

## 📋 Sample Subtasks

| Subtask | Framework / Tool |
|---------|-------------------|
| Design a star schema in the Lakehouse and version it in dbt repo | dbt-core, Iceberg, GitLab |
| Build OLAP-wide sales aggregate table using StarRocks materialized view | StarRocks |
| Define “Monthly Active Users” metric using dbt Metrics and validate with tests | dbt Metrics |
| Create Redis cache layer in front of Trino for hot dashboard tables | Redis, Helm |
| Automate secondary pipeline YAML to generate wide table DAGs | Python, Jinja2, Airflow, GitLab CI |
| Publish Superset embedding SDK with RLS token support and CI versioning | Superset, JS SDK, Artifactory |
| Deploy and configure Trino with autoscaling worker pool on Kubernetes | Trino Operator, K8s HPA |
| Run weekly slow-query audit on StarRocks and tune joins and indexes | StarRocks, Prometheus, Grafana |


---
---

# ✅ Why Organizing into Four 2-Person Subteams Works Better

---

###  Benefits of Creating Focused Subteams

- **Clear Responsibilities = Faster Problem Resolution**  
  - Each subteam owns a specific area (like platform infrastructure, ML, pipelines, or BI). When something goes wrong, it’s clear who handles it, no delays or confusion.

- **Focused Expertise with Built-in Collaboration**  
  - Engineers can specialize in one domain and develop deep skills, while working closely with a teammate to share context and knowledge.

- **Multiple Projects Move Forward at the Same Time**  
  - Different subteams can work on different priorities without getting in each other’s way—like fixing Spark configs while also launching a new Superset dashboard.

- **Structured Mentoring and Career Growth**  
  - Pairing a less experienced engineer with a more experienced one makes it easier to learn and grow—without needing formal managers for each subteam.

- **Better Resilience to Leave or Turnover**  
  - If someone takes vacation or leaves, their teammate can continue the work. The rest of the team stays productive and unaffected.

- **Flexible and Easy to Grow**  
  - As your team expands, you can add people into each subteam without needing to change how the whole team is organized.

- **Supports Future Business Needs**  
  - If your company later offers parts of the data platform (ML, BI, pipelines) as services to other teams or clients, these subteams already match those service boundaries.

---

### Why This Team Structure Is the Right Choice

Organizing into focused subteams provides:

- **Clear accountability** – Everyone knows who is responsible for each system or service.
- **Faster progress** – More projects can be delivered in parallel without conflicts.
- **Strong reliability** – You always have backup; work doesn’t stop when someone is away.
- **Higher skill levels** – Engineers improve faster by working in a consistent area.
- **Future readiness** – Easy to scale, extend, or align with company-wide products.

This structure creates a clear, resilient, and scalable team that delivers more—without chaos or delays.

---
---

# 🌳 Data Infrastructure Team Structure

This structure shows how an 8-person data infrastructure team is organized under a single team lead, with four specialized subteams. Each subteam currently has two members and operates without a designated subteam lead.

---

###  Team Structure 
```
                         Data Infrastructure Lead
                                  │
        ┌──────────────┬────────────────┬──────────────┐
        ▼              ▼                ▼              ▼
Data Platform    Data Engineering     MLOps        BI Services
     Team             Team             Team            Team
     │                 │                │               │
 ┌───┴───┐         ┌───┴───┐        ┌───┴───┐       ┌───┴───┐
 ▼       ▼         ▼       ▼        ▼       ▼       ▼       ▼
Eng 1   Eng 2     Eng 3   Eng 4    Eng 5   Eng 6   Eng 7   Eng 8
```


---

### Leadership Rules

#### Current Phase: Flat Subteams (2 Members Each)
- No subteam leads yet.
- All 8 engineers report directly to the **Data Infrastructure Lead**.

---

##### Promotion Rule: Subteam Lead When Team Reaches 3 People
- When any subteam grows to **3 or more engineers**, assign a **subteam lead**.
- The subteam lead will:
  - Coordinate day-to-day tasks within the team.
  - Mentor junior members.
  - Represent the team in planning and reviews.
- Subteam leads **are not managers**, but **technical points of contact**.

---

### Responsibilities of the Data Infrastructure Lead
---

#### Organizational Leadership

- **Performance Management**  
  - Conduct regular 1:1s, track individual contributions, and manage performance reviews using clear and consistent evaluation criteria.

- **Shape Up Process Ownership**  
  - Own and lead the Shape Up process within the team—define appetites, pitch high-leverage projects, and guide cycle planning. Ensure pitches are technically feasible and strategically aligned.

- **Mentorship & Career Growth**  
  - Actively support engineers’ professional development through structured growth plans, skill mapping, and feedback loops.

- **Conflict Resolution**  
  - Resolve prioritization or ownership disputes and ensure collaboration across all subteams stays constructive and timely.

- **Cross-Team and Stakeholder Communication**  
  - Act as the main point of contact between the data infrastructure team and other internal teams. Maintain visibility and transparency of work progress, timelines, and delivery risks.

- **On-Call Ownership and Escalation**  
  - Define and manage the on-call rotation, escalation policy, and post-incident review process. Ensure 24/7 coverage across critical systems and coordinate timely resolution of Sev-1 incidents.

---

#### Technical Leadership

- **Architecture Design & Approval**  
  - Lead the design of major components such as secure data lakes, streaming pipelines, ML infra, and analytics stack integrations. Approve proposals and enforce architectural standards.

- **Technical Roadmap Ownership**  
  - Maintain and evolve a unified technical roadmap that feeds into Shape Up pitches, including items like Spark upgrades, Iceberg adoption, ML/LLM stack enhancements, and query federation.

- **Design Technical Solutions**  
  - Participate in designing key systems such as CDC pipelines, ML model deployment flows, Spark-on-YARN optimizations, or security integration patterns.

- **Guide and Participate in Implementation**  
  - Where possible, contribute directly to coding, Helm chart updates, infrastructure automation, or architecture prototyping—especially in high-risk or early-phase work.

- **Review and Monitor Technical Progress**  
  - Run tech check-ins during build cycles, review branch progress, and ensure scopes are being completed with the expected quality and performance.

- **Ensure System Reliability and Security**  
  - Own on-call policy, SLA tracking, TLS/SSO/Kerberos enforcement, and root-cause analysis of platform incidents.

- **Budget and Capacity Planning**  
  - Manage infrastructure costs (GPUs, storage, HP Servers), align spending with Shape Up cycle priorities, and ensure system capacity keeps up with forecasted demand.

---
---

# ✅ Why the Data Team—Not DevOps—Should Own the Data Platform

This document summarizes the key reasons your data infrastructure team—not general DevOps—should run the data platform.

---

## 📌 Key Reasons for Data Platform Ownership

| # | Core Reason | How It Works in Practice |
|---|-------------|---------------------------|
| 1 | Business and goal alignment | Data SLAs (like dashboard speed or freshness) aren’t infrastructure metrics; data team understands both the intent and the knobs |
| 2 | Workload-aware tuning | Data engineers understand query shapes and can adjust Spark/Presto/Pinot accordingly |
| 3 | Faster innovation and upgrades | DevOps typically works on quarterly cycles; data teams release every sprint |
| 4 | Privacy and compliance ownership | Regulations like GDPR require row-level delete logic built into pipelines |
| 5 | Cost optimization and cleanup | Data teams can trace costs to jobs, tables, and query plans—not just VMs or clusters |
| 6 | End-to-end incident resolution | Data Infra can fix issues from logic to infra, while Ops often only sees hardware-level symptoms |
| 7 | Better support interactions | Vendors need both logs and pipeline context; Data Infra can give both at once |
| 8 | Proven industry pattern | Top companies keep data platform under data team, not DevOps |

---

## ✅ Summary

Letting the Data Infrastructure team run the platform results in:

- Better alignment with business goals  
- More performance and cost control  
- Faster fixes and software updates  
- Easier compliance with privacy regulations  
- Industry-proven best practices
