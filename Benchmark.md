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
