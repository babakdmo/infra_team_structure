# Google (Alphabet) – Data Infrastructure Sub-Teams

This document describes the key sub-teams in Google's data infrastructure division. Each team has a specific role and uses a set of technologies to do its job.

---

## 📊 Sub-Team Overview Table

| **Sub-Team Name**             | **What the Team Does**                                                                                         | **Technologies Used**                         |
|------------------------------|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Global Storage & Metadata    | Manages huge amounts of data storage, handles backups across regions, protects data, plans for storage needs     | Colossus (GFS v2), Bigtable, Spanner, GCS     |
| Batch & Interactive Analytics| Runs large SQL queries, schedules batch jobs, and keeps project costs separate                                   | BigQuery, Dataflow, Dataproc, Composer        |
| Streaming & Ingest           | Handles real-time data flow and syncing using event streaming and low-latency systems                            | Cloud Pub/Sub, Datastream → Dataflow          |
| ML Platform Services         | Supports model training and serving, manages machine learning features and TPU devices                          | Vertex AI, TFX, Feast, TPU-Ops                |
| Data Governance & Quality    | Tracks data, ensures it meets rules, and manages cost and usage transparency                                     | Dataplex, Data Catalog                         |

---

## 🌳 Team Structure Tree

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

## ☁️ Platform

All sub-teams and services are built and operated using **Google Cloud** infrastructure.


# Amazon (AWS + Amazon Retail) – Data Infrastructure Sub-Teams

This document outlines the major data infrastructure sub-teams at Amazon, including both AWS and Amazon Retail. Each team has specific goals and works with particular tools to manage, process, and analyze data.

---

## 📊 Sub-Team Overview Table

| **Sub-Team Name**             | **What the Team Does**                                                                                         | **Technologies Used**                                 |
|------------------------------|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Amazon Consumer Data Platform (ACDP) | Manages commerce data lake, performs batch ETL, and supports offline machine learning models               | EMR (Hadoop/Spark), Redshift, Glue Catalog, S3 Lake    |
| Real-time Streaming Platform  | Handles real-time event ingestion and transformation, delivering data reliably to the lake                     | Kinesis family, MSK (Kafka), Flink                     |
| ML Services Platform          | Provides tools for model training, feature storage, fairness scans, and hosted notebooks                        | SageMaker, Feature Store, Clarify                      |
| Lake Governance & FinOps      | Controls access, checks data format rules, and manages cost visibility and reporting                            | Lake Formation, AQUA, Cost Explorer                    |

---

## 🌳 Team Structure Tree

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

## ☁️ Platform

All of the above teams and tools operate on **Amazon Web Services (AWS)** infrastructure.

# Microsoft (Core AI – Platform & Tools) – Data Infrastructure Sub-Teams

This document outlines the key sub-teams within Microsoft's Core AI group, focusing on platforms and tools used to manage AI workloads, models, telemetry, and compliance.

---

## 📊 Sub-Team Overview Table

| **Sub-Team Name**            | **What the Team Does**                                                                                             | **Technologies Used**                                     |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Data & Model Infrastructure | Manages the lakehouse and data warehouse platforms for internal AI workloads                                        | Fabric (OneLake, Synapse), Kusto, Data Factory             |
| AI Super-computer & Runtime | Runs and optimizes large AI models on powerful GPU clusters, using training and serving runtimes                    | Azure AI Foundry, DeepSpeed, ONNX-Runtime                  |
| Developer Insights & Telemetry | Collects and visualizes logs, traces, and metrics for all models and pipelines                                   | Azure Monitor, Kusto Log Analytics                         |
| Governance & Compliance      | Ensures AI systems comply with regulations like GDPR and EU AI Act; handles secure computation and key management   | Purview, Confidential Compute, KeyVault                    |

---

## 🌳 Team Structure Tree

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

## ☁️ Platform

These teams and tools operate on **Microsoft Azure**. Kubernetes fabric and data center networking are part of **Azure Core** and are used by Core AI but not owned by it.

---
---

# Meta (Facebook) – Data Infrastructure Sub-Teams

This document outlines the primary sub-teams in Meta's data infrastructure organization. Each team handles specific responsibilities related to data storage, analytics, machine learning, and governance.

---

## 📊 Sub-Team Overview Table

| **Sub-Team Name**               | **What the Team Does**                                                                                         | **Technologies Used**                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Storage Foundations            | Manages massive cold and hot storage systems, including media object storage and compression layers            | HDFS, Zippy, Haystack                                 |
| Batch & Interactive Analytics  | Runs large-scale data processing and querying systems using Spark and Presto, powered by a custom ETL engine    | Presto, Spark, Laser                                  |
| Real-time Streaming & Observability | Provides real-time monitoring and observability of system behavior with ultra-low latency                     | Scuba, Scribe, MemSQL                                 |
| ML Infrastructure              | Supports the entire ML pipeline including training, feature engineering, and model serving                      | FBLearner, PyTorch Edge, Ares                         |
| Metadata & Data Governance     | Maintains a central catalog, data ownership tracking, and enforces data governance policies                     | DataHub, RAMP                                         |

---

## 🌳 Team Structure Tree

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

## ☁️ Platform

These services and tools are developed and operated internally within **Meta’s own data centers and infrastructure**.
