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
