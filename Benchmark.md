# 1- Google (Alphabet) – Data Infrastructure Sub-Teams

This document describes the key sub-teams in Google's data infrastructure division. Each team has a specific role and uses a set of technologies to do its job.

---

### 📊 Sub-Team Overview Table

| **Sub-Team Name**             | **What the Team Does**                                                                                         | **Technologies Used**                         |
|------------------------------|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Global Storage & Metadata    | Manages huge amounts of data storage, handles backups across regions, protects data, plans for storage needs     | Colossus (GFS v2), Bigtable, Spanner, GCS     |
| Batch & Interactive Analytics| Runs large SQL queries, schedules batch jobs, and keeps project costs separate                                   | BigQuery, Dataflow, Dataproc, Composer        |
| Streaming & Ingest           | Handles real-time data flow and syncing using event streaming and low-latency systems                            | Cloud Pub/Sub, Datastream → Dataflow          |
| ML Platform Services         | Supports model training and serving, manages machine learning features and TPU devices                          | Vertex AI, TFX, Feast, TPU-Ops                |
| Data Governance & Quality    | Tracks data, ensures it meets rules, and manages cost and usage transparency                                     | Dataplex, Data Catalog                         |

---

### 🌳 Team Structure Tree

```
Google Data Infrastructure
├── Global Storage & Metadata
│   └── Tools: Colossus (GFS v2), Bigtable, Spanner, GCS
├── Batch & Interactive Analytics
│   └── Tools: BigQuery, Dataflow, Dataproc, Composer
├── Streaming & Ingest
│   └── Tools: Cloud Pub/Sub, Datastream → Dataflow
├── ML Platform Services
│   └── Tools: Vertex AI, TFX, Feast, TPU-Ops
└── Data Governance & Quality
    └── Tools: Dataplex, Data Catalog
```

### ☁️ Platform

All sub-teams and services are built and operated using **Google Cloud** infrastructure.

---
---

# 2- Amazon (AWS + Amazon Retail) – Data Infrastructure Sub-Teams

This document outlines the major data infrastructure sub-teams at Amazon, including both AWS and Amazon Retail. Each team has specific goals and works with particular tools to manage, process, and analyze data.

---

### 📊 Sub-Team Overview Table

| **Sub-Team Name**             | **What the Team Does**                                                                                         | **Technologies Used**                                 |
|------------------------------|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Amazon Consumer Data Platform (ACDP) | Manages commerce data lake, performs batch ETL, and supports offline machine learning models               | EMR (Hadoop/Spark), Redshift, Glue Catalog, S3 Lake    |
| Real-time Streaming Platform  | Handles real-time event ingestion and transformation, delivering data reliably to the lake                     | Kinesis family, MSK (Kafka), Flink                     |
| ML Services Platform          | Provides tools for model training, feature storage, fairness scans, and hosted notebooks                        | SageMaker, Feature Store, Clarify                      |
| Lake Governance & FinOps      | Controls access, checks data format rules, and manages cost visibility and reporting                            | Lake Formation, AQUA, Cost Explorer                    |

---

### 🌳 Team Structure Tree

```
Amazon Data Infrastructure
├── Amazon Consumer Data Platform (ACDP)
│   └── Tools: EMR (Hadoop/Spark), Redshift, Glue Catalog, S3 Lake
├── Real-time Streaming Platform
│   └── Tools: Kinesis family, MSK (Kafka), Flink
├── ML Services Platform
│   └── Tools: SageMaker, Feature Store, Clarify
└── Lake Governance & FinOps
    └── Tools: Lake Formation, AQUA, Cost Explorer
```

---

### ☁️ Platform

All of the above teams and tools operate on **Amazon Web Services (AWS)** infrastructure.

---
---

# 3- Microsoft (Core AI – Platform & Tools) – Data Infrastructure Sub-Teams

This document outlines the key sub-teams within Microsoft's Core AI group, focusing on platforms and tools used to manage AI workloads, models, telemetry, and compliance.

---

### 📊 Sub-Team Overview Table

| **Sub-Team Name**            | **What the Team Does**                                                                                             | **Technologies Used**                                     |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Data & Model Infrastructure | Manages the lakehouse and data warehouse platforms for internal AI workloads                                        | Fabric (OneLake, Synapse), Kusto, Data Factory             |
| AI Super-computer & Runtime | Runs and optimizes large AI models on powerful GPU clusters, using training and serving runtimes                    | Azure AI Foundry, DeepSpeed, ONNX-Runtime                  |
| Developer Insights & Telemetry | Collects and visualizes logs, traces, and metrics for all models and pipelines                                   | Azure Monitor, Kusto Log Analytics                         |
| Governance & Compliance      | Ensures AI systems comply with regulations like GDPR and EU AI Act; handles secure computation and key management   | Purview, Confidential Compute, KeyVault                    |

---

### 🌳 Team Structure Tree

```
Microsoft Core AI – Platform & Tools
├── Data & Model Infrastructure
│   └── Tools: Fabric (OneLake, Synapse), Kusto, Data Factory
├── AI Super-computer & Runtime
│   └── Tools: Azure AI Foundry, DeepSpeed, ONNX-Runtime
├── Developer Insights & Telemetry
│   └── Tools: Azure Monitor, Kusto Log Analytics
└── Governance & Compliance
    └── Tools: Purview, Confidential Compute, KeyVault
```

---

### ☁️ Platform

These teams and tools operate on **Microsoft Azure**. Kubernetes fabric and data center networking are part of **Azure Core** and are used by Core AI but not owned by it.

---
---

# 4-  Meta (Facebook) – Data Infrastructure Sub-Teams

This document outlines the primary sub-teams in Meta's data infrastructure organization. Each team handles specific responsibilities related to data storage, analytics, machine learning, and governance.

---

### 📊 Sub-Team Overview Table

| **Sub-Team Name**               | **What the Team Does**                                                                                         | **Technologies Used**                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Storage Foundations            | Manages massive cold and hot storage systems, including media object storage and compression layers            | HDFS, Zippy, Haystack                                 |
| Batch & Interactive Analytics  | Runs large-scale data processing and querying systems using Spark and Presto, powered by a custom ETL engine    | Presto, Spark, Laser                                  |
| Real-time Streaming & Observability | Provides real-time monitoring and observability of system behavior with ultra-low latency                     | Scuba, Scribe, MemSQL                                 |
| ML Infrastructure              | Supports the entire ML pipeline including training, feature engineering, and model serving                      | FBLearner, PyTorch Edge, Ares                         |
| Metadata & Data Governance     | Maintains a central catalog, data ownership tracking, and enforces data governance policies                     | DataHub, RAMP                                         |

---

### 🌳 Team Structure Tree

```
Meta Data Infrastructure
├── Storage Foundations
│   └── Tools: HDFS, Zippy, Haystack
├── Batch & Interactive Analytics
│   └── Tools: Presto, Spark, Laser
├── Real-time Streaming & Observability
│   └── Tools: Scuba, Scribe, MemSQL
├── ML Infrastructure
│   └── Tools: FBLearner, PyTorch Edge, Ares
└── Metadata & Data Governance
    └── Tools: DataHub, RAMP
```

---

### ☁️ Platform

These services and tools are developed and operated internally within **Meta’s own data centers and infrastructure**.

---
---

# 5- Netflix – Data Infrastructure Sub-Teams

This document outlines the major data infrastructure sub-teams within Netflix, detailing their roles and the tools they use to manage, process, and analyze data.

---

### 📊 Sub-Team Overview Table

| **Sub-Team Name**                | **What the Team Does**                                                                                          | **Technologies Used**                                               |
|----------------------------------|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Incremental & Batch Platform     | Manages Iceberg tables on S3, runs Spark jobs on Titus, and provides workflow APIs via Maestro                  | Apache Iceberg, Spark on Titus, Maestro IPS, Dataproc for burst     |
| Realtime & Operational Streaming | Handles real-time telemetry, live debugging data streams, and feeds system health dashboards                    | Mantis, Keystone Streams, Kafka, Flink SQL (“Data-Mesh” service)    |
| ML / Experimentation Platform    | Supports full model development, A/B testing, feature storage, and experiment tracking                          | Metaflow, Feast (in-house), Keystone Experiment, Atlas for metrics  |
| Data Governance & Catalog        | Maintains schema registry, applies privacy tags, tracks data usage and cost                                     | DataHub (fork), Atlas with cost tracking hooks                      |

---

### 🌳 Team Structure Tree

```
Netflix Data Infrastructure
├── Incremental & Batch Platform
│   └── Tools: Apache Iceberg, Spark on Titus, Maestro IPS, Dataproc for burst
├── Realtime & Operational Streaming
│   └── Tools: Mantis, Keystone Streams, Kafka, Flink SQL “Data-Mesh” service
├── ML / Experimentation Platform
│   └── Tools: Metaflow, Feast (in-house), Keystone Experiment, Atlas for model metrics
└── Data Governance & Catalog
    └── Tools: DataHub (fork), Atlas cost hooks
```

---

### ☁️ Platform

These systems are developed and run on **Netflix's internal infrastructure**, including Titus (Netflix's container platform) and other open-source and custom technologies.

---
---

# 6- Uber – Data Infrastructure Sub-Teams

This document outlines the main sub-teams within Uber’s data infrastructure organization. Each team plays a key role in managing batch, streaming, ML platforms, and data governance systems.

---

### 📊 Sub-Team Overview Table

| **Sub-Team Name**          | **What the Team Does**                                                                                       | **Technologies Used**                                               |
|---------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Batch Data Platform       | Manages petabyte-scale ETL and SQL workloads; also leads migration from on-prem to Google Cloud                | Hadoop (YARN), Spark, Presto, Hive → GCP Dataproc                   |
| Streaming Platform        | Maintains real-time streaming systems with strong delivery guarantees and low-latency analytics                | Kafka/MSK, Flink, Pinot cluster mesh                                |
| ML / Feature Platform     | Manages ML model lifecycle and ensures parity between real-time and batch features across the company           | Michelangelo, internal Feature-Store, Ray for DL jobs               |
| Data Governance & FinOps  | Handles data cost tracking, lineage metadata, and alerts on data quality issues                                | DataCentral, UDMS mesh annotations                                  |

---

### 🌳 Team Structure Tree

```
Uber Data Infrastructure
├── Batch Data Platform
│   └── Tools: Hadoop (YARN), Spark, Presto, Hive → GCP Dataproc
├── Streaming Platform
│   └── Tools: Kafka/MSK, Flink, Pinot cluster mesh
├── ML / Feature Platform
│   └── Tools: Michelangelo, internal Feature-Store, Ray for DL jobs
└── Data Governance & FinOps
    └── Tools: DataCentral, UDMS mesh annotations
```

---

### ☁️ Platform

- **Batch and Streaming are sibling teams** due to scaling demands (e.g., Kafka ingress over 4 PB/day).
- **Fabric** components (Kubernetes, Vault, Networking) are handled by a separate **Compute Platform** team.
- **Michelangelo** is part of the **Data Infrastructure** org.

---
---

# 7- LinkedIn – Data Infrastructure Sub-Teams

This document outlines the major sub-teams within LinkedIn's data infrastructure organization. Each team is responsible for critical components that manage, process, or serve data and machine learning features.

---

### 📊 Sub-Team Overview Table

| **Sub-Team Name**           | **What the Team Does**                                                                                      | **Technologies Used**                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Streams Infra              | Handles the capture and processing of over 4 trillion events per day; distributes data to analytical systems | Kafka, Samza, Brooklin connectors                   |
| Offline Data Platform      | Manages the HDFS data lake, Spark/Presto clusters, and prepares data for OLAP analytics with Pinot           | Hadoop, Spark, Presto, Pinot-Offline “Hoptimator”   |
| AI Feature & Model Serving | Provides tools and platforms for machine learning feature management and online inference                    | Pro-ML, DALI, Vespa search                          |
| Metadata / Governance      | Maintains LinkedIn’s enterprise-wide data catalog, ownership graph, and policy-as-code systems                | DataHub OSS                                         |

---

### 🌳 Team Structure Tree

```
LinkedIn Data Infrastructure
├── Streams Infra
│   └── Tools: Kafka, Samza, Brooklin connectors
├── Offline Data Platform
│   └── Tools: Hadoop, Spark, Presto, Pinot-Offline “Hoptimator”
├── AI Feature & Model Serving
│   └── Tools: Pro-ML, DALI, Vespa search
└── Metadata / Governance
    └── Tools: DataHub OSS
```

---

### ☁️ Platform

All of these services are developed and maintained within **LinkedIn’s own data centers** and use a combination of internal and open-source tools, some of which (like DataHub) were originally developed at LinkedIn.

---
---

# 8- Spotify – Data Infrastructure Sub-Teams

This document describes the primary sub-teams in Spotify’s data infrastructure organization. Each team is responsible for a distinct area of the data platform, from ingestion and processing to machine learning and governance.

---

### 📊 Sub-Team Overview Table

| **Sub-Team Name**               | **What the Team Does**                                                                                         | **Technologies Used**                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Data Collection & Ingest       | Handles event collection from clients and music metadata using a publish-subscribe messaging system            | Google PubSub, custom Kafka, protobuf schemas                           |
| Processing & Orchestration     | Runs batch data pipelines and asset workflows in Scala using Beam and orchestrates using Dagster                | Dagster, Apache Beam/Scio, Dataflow                                     |
| ML & Personalisation Platform  | Supports full ML pipeline including audio feature extraction and serving with internal tools                    | Klio (Beam-based), Salem (TF-Serving wrapper), ML Home portal           |
| Data Management / Lakehouse    | Manages lakehouse specifications, schema consistency, and data access                                           | Iceberg tables on GCS, BigQuery, Backstage plug-ins                     |
| Governance Chapter             | Ensures data quality, privacy policies, persona tagging, and tracks data lineage and costs                      | Datacraft, Midas quality audits                                         |

---

### 🌳 Team Structure Tree

```
Spotify Data Infrastructure
├── Data Collection & Ingest
│   └── Tools: Google PubSub, custom Kafka, protobuf schemas
├── Processing & Orchestration
│   └── Tools: Dagster, Apache Beam/Scio, Dataflow
├── ML & Personalisation Platform
│   └── Tools: Klio, Salem, ML Home portal
├── Data Management / Lakehouse
│   └── Tools: Iceberg tables on GCS, BigQuery, Backstage plug-ins
└── Governance Chapter
    └── Tools: Datacraft, Midas quality audits
```

---

### ☁️ Platform

Spotify runs its data infrastructure primarily on **Google Cloud Platform (GCP)** and uses a mix of open-source, custom-built, and third-party tools to manage the entire data lifecycle.

---
---

# 9- Shopify – Data Infrastructure Sub-Teams

This document outlines the major sub-teams in Shopify’s data infrastructure organization. Each team focuses on specific aspects of the data lifecycle, from ingestion and streaming to lakehouse management and ML platform engineering.

---

### 📊 Sub-Team Overview Table

| **Sub-Team Name**         | **What the Team Does**                                                                                       | **Technologies Used**                                               |
|--------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Lakehouse Team           | Manages a single Iceberg table layer with support for federated and OLAP queries                              | Iceberg on S3, Trino, ClickHouse                                     |
| Streaming Data           | Ingests real-time buyer signals, runs Flink applications, and handles CDC from MySQL                          | Kafka/Flink, Debezium, Flink SQL                                     |
| Merlin ML Platform       | Provides full training, serving, and monitoring for ML models related to fraud detection and promotions       | Merlin (Ray Train/Tune, Kubeflow), FeatureDSL                        |
| Data Trust Chapter       | Enforces GDPR compliance, data quality standards, and runs auditing tools                                      | Great Expectations, Monte Carlo, “Data Trust” checklist              |

---

### 🌳 Team Structure Tree

```
Shopify Data Infrastructure
├── Lakehouse Team
│   └── Tools: Iceberg on S3, Trino, ClickHouse
├── Streaming Data
│   └── Tools: Kafka/Flink, Debezium, Flink SQL
├── Merlin ML Platform
│   └── Tools: Merlin (Ray Train/Tune, Kubeflow), FeatureDSL
└── Data Trust Chapter
    └── Tools: Great Expectations, Monte Carlo, Data Trust checklist
```

---

### ☁️ Platform

- Shopify uses **S3** as the data lake backend, and its infrastructure is engineered around open formats and cloud-native platforms.
- **Production Engineers** at Shopify manage Kubernetes and CI, but **do not own Iceberg or Merlin**—those are owned by the respective data platform teams.

---
---

# 10- Airbnb – Data Infrastructure Sub-Teams

This document outlines the core sub-teams in Airbnb's data infrastructure organization. Each team is responsible for part of the platform, ranging from batch processing to machine learning and metadata management.

---

### 📊 Sub-Team Overview Table

| **Sub-Team Name**          | **What the Team Does**                                                                                     | **Technologies Used**                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Metric & Batch Platform   | Provides a central metric layer and manages Spark-based ETL pipelines across the company                    | Minerva metric platform, Spark, Hive, Airflow               |
| Realtime Platform         | Delivers low-latency data for search, pricing, and operational use cases                                    | Kafka, Flink, Pinot                                         |
| ML Infrastructure         | Supports the full lifecycle of machine learning, including feature engineering, training, and serving       | Bighead, Zipline Feature Store, Redspot notebooks           |
| Data Management & Catalog | Maintains Airbnb’s data catalog, cost visibility tools, and privacy scanning                                | Metis, DataPortal, Amundsen lineage                         |

---

### 🌳 Team Structure Tree

```
Airbnb Data Infrastructure
├── Metric & Batch Platform
│   └── Tools: Minerva metric platform, Spark, Hive, Airflow
├── Realtime Platform
│   └── Tools: Kafka, Flink, Pinot
├── ML Infrastructure
│   └── Tools: Bighead, Zipline FS, Redspot notebooks
└── Data Management & Catalog
    └── Tools: Metis, DataPortal, Amundsen lineage
```

---

### ☁️ Platform

- Airbnb’s infrastructure is organized so that **Bighead ML Platform** is part of the **Data Infrastructure** team. This allows ML models to be deployed without relying on separate DevOps ticket workflows.
