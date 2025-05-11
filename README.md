# **Infra Team Structure**

```
Chief Infrastructure & Platform Officer  (CIPO)
│
├─ 1A  Facilities & Physical Infra
├─ 1B  Core Cloud Infra & Platform
├─ 1C  Platform Engineering & Developer Experience
├─ 1D  Data & AI Infrastructure
├─ 1E  Security, Privacy & Compliance
├─ 1F  Reliability & Observability  (SRE Core)
└─ 1G  FinOps & Capacity Engineering
```
## **1A – Facilities & Physical Infrastructure**

This document outlines the internal squads, sub-units, responsibilities, and KPIs for the Facilities & Physical Infrastructure department.

## 📌 Organizational Breakdown

| Squad | Internal Units (Sub-Teams) | Responsibilities | KPIs / Objectives |
|-------|----------------------------|------------------|-------------------|
| **A-1 Procurement & Vendor Operations** | U-V1 Vendor Relations  <br> U-V2 CapEx Planning | RFP/RFQ processes, SLA negotiation, TCO management | ≥ 8% cost savings <br> Lead time ≤ 90 days |
| **A-2 Warehouse & Inventory** | U-W1 Inbound Logistics <br> U-W2 CMDB / Asset Management <br> U-W3 RMA / Disposal | Barcode + RFID tracking, accurate CMDB, RMA processing, electronic waste management | 100% inventory accuracy <br> RMA turnaround ≤ 5 days |
| **A-3 Datacenter Testing & Installation** | U-D1 Burn-In Testing <br> U-D2 Racking & Cabling <br> U-D3 Site SAT (Site Acceptance Test) | 48h soak test, fiber cabling, LLDP labeling | DOA < 0.3% <br> Installation time ≤ 7 days |

## **1A – Facilities & Physical Infrastructure Tree**

```
1A Facilities & Physical Infra
│
├─ A-1 Procurement & Vendor Ops
│   ├─ U-V1 Vendor Relations
│   ├─ U-V2 CapEx Planning
│   ├─ Responsibilities:
│   │   ├─ RFP/RFQ Processes
│   │   ├─ SLA Negotiation
│   │   └─ TCO Management
│   └─ KPIs:
│       ├─ Cost Savings ≥ 8%
│       └─ Lead Time ≤ 90 days
│
├─ A-2 Warehouse & Inventory
│   ├─ U-W1 Inbound Logistics
│   ├─ U-W2 CMDB / Asset Management
│   ├─ U-W3 RMA / Disposal
│   ├─ Responsibilities:
│   │   ├─ Barcode + RFID Tracking
│   │   ├─ Accurate CMDB
│   │   ├─ RMA Processing
│   │   └─ e-Waste Management
│   └─ KPIs:
│       ├─ 100% Inventory Accuracy
│       └─ RMA Turnaround ≤ 5 days
│
└─ A-3 Datacenter Test & Install
    ├─ U-D1 Burn-In Testing
    ├─ U-D2 Racking & Cabling
    ├─ U-D3 Site SAT
    ├─ Responsibilities:
    │   ├─ 48h Soak Test
    │   ├─ Fiber Optic Cabling
    │   └─ LLDP Labeling
    └─ KPIs:
        ├─ DOA < 0.3%
        └─ Installation ≤ 7 days
```

## **1B – Core Cloud Infrastructure & Platform**

This document outlines the squads, internal units, detailed responsibilities, and KPIs for the Core Cloud Infrastructure & Platform department.

> **Governance Boundary:**  
> The 1B squad is the sole authority for Kernel versions, CNI/CSI integrations, and GPU NodePool configurations. All other layers are consumers of its APIs only.

---

## 📌 Organizational Breakdown

| Squad | Internal Units (Sub-Teams) | Responsibilities | KPIs / Objectives |
|-------|----------------------------|------------------|-------------------|
| **B-1 Compute Platform** | U-C1 Cluster-API <br> U-C2 NodePool <br> U-C3 Kernel Lifecycle | Kubernetes v1.30, GPU/CPU pools, CRI-O, Kernel patching ≤ 48h | API Uptime ≥ 99.95% |
| **B-2 Storage Services** | U-S1 Object Storage (Ceph-S3) <br> U-S2 Block Storage (RBD) <br> U-S3 DB-aaS (Vitess) | Replication / Erasure Coding, Quality of Service, PV provisioning | Durability 11×9 <br> P95 latency < 5ms |
| **B-3 Network & Edge** | U-N1 Spine-Leaf BGP-EVPN <br> U-N2 POP / CDN <br> U-N3 DNS / IPAM | SRv6, TLS offloading, Anycast VIPs | Packet loss < 0.01% |
| **B-4 Firmware & HW Enablement** | U-H1 BMC / BIOS <br> U-H2 SecureBoot / TPM | Firmware automation, SBOM (Software Bill of Materials) generation | Firmware lag < 2 versions |

---

## **1B – Core Cloud Infrastructure & Platform Tree**

```
1B Core Cloud Infra & Platform
│
├─ B-1 Compute Platform
│   ├─ U-C1 Cluster-API
│   ├─ U-C2 NodePool
│   ├─ U-C3 Kernel Lifecycle
│   ├─ Responsibilities:
│   │   ├─ Kubernetes v1.30
│   │   ├─ GPU/CPU Pools
│   │   ├─ CRI-O Runtime
│   │   └─ Kernel Patch ≤ 48h
│   └─ KPIs:
│       └─ API Uptime ≥ 99.95%
│
├─ B-2 Storage Services
│   ├─ U-S1 Object Storage (Ceph-S3)
│   ├─ U-S2 Block Storage (RBD)
│   ├─ U-S3 DB-aaS (Vitess)
│   ├─ Responsibilities:
│   │   ├─ Replication / Erasure Coding
│   │   ├─ Quality of Service (QoS)
│   │   └─ Persistent Volume Provisioning
│   └─ KPIs:
│       ├─ Durability: 11×9
│       └─ P95 Latency < 5ms
│
├─ B-3 Network & Edge
│   ├─ U-N1 Spine-Leaf BGP-EVPN
│   ├─ U-N2 POP / CDN
│   ├─ U-N3 DNS / IPAM
│   ├─ Responsibilities:
│   │   ├─ SRv6 Routing
│   │   ├─ TLS Offload
│   │   └─ Anycast VIPs
│   └─ KPIs:
│       └─ Packet Loss < 0.01%
│
└─ B-4 Firmware & HW Enablement
    ├─ U-H1 BMC / BIOS
    ├─ U-H2 SecureBoot / TPM
    ├─ Responsibilities:
    │   ├─ Firmware Automation
    │   └─ SBOM (Software Bill of Materials)
    └─ KPIs:
        └─ Firmware Lag < 2 Versions
```

## **1C – Platform Engineering & Developer Experience**

This document outlines the squads, sub-units, responsibilities, tech stack, measurable KPIs/SLOs, and key inter-team dependencies for developer experience and platform enablement.

> **Note:**  
> LTFC = Lead-Time-for-Change (from commit to stable deployment in Dev)

---

## 📌 Organizational Breakdown

| Squad | Sub-Units | Responsibilities & Outputs | Key Stack & Tools | KPI / SLO | Critical Dependencies |
|-------|-----------|-----------------------------|--------------------|-----------|------------------------|
| **C-1 IDP Core & Self-Service** | U-P1 Software Catalog <br> U-P2 Golden-Path Scaffolder <br> U-P3 Dev-Namespace Plugin | Maintain Backstage metadata, scaffold project ≤ 30s, create Dev namespace+SA with TTL=72h | Backstage 0.21, Terraform Provider, Knative Plugin | LTFC < 60 min <br> Catalog Coverage ≥ 95% | 1B (Cluster-API), 1E (RBAC/TTL Policy) |
| **C-2 CI/CD Platform** | U-CI1 Build & Cache Farm <br> U-CI2 Argo CD Control-Plane <br> U-CI3 Ephemeral Env Engine | App/DAG/Helm templates, container signing, dev-$BRANCH namespaces with auto-clean | ArgoCD 2.10, Tekton, Cosign, Vault CSI | ≥ 20 Deploys/day <br> Failed Pipelines < 2% | 1F (Build Metrics), 1E (Cosign Keys) |
| **C-3 Runtime Services / Service Mesh** | U-R1 Istio Ambient Mesh <br> U-R2 API Gateway <br> U-R3 Feature Flags / Canary | STRICT mTLS, 10 min Canary-to-Prod, Tiered Rate-Limit | Istio 1.23, Envoy, Flagger, Flagsmith SaaS | p99 < 100ms <br> Canary Abort FP < 1% | 1F (SLO Metrics), 1E (OIDC) |
| **C-4 Dev Environment Tooling** | U-DEV1 Local-K8s Kit <br> U-DEV2 Dev-Cluster Provisioner <br> U-DEV3 Dev-Secrets & TLS | “dev bootstrap” for Mac/Linux, upgrade Dev Cluster w/ prod, Vault Dev TTL=24h | Kind, Tilt, Cluster-API, cert-manager, Vault | Dev Bootstrap Success > 95% <br> Dev API Uptime ≥ 99% | 1B (Dev Infra), 1E (Vault Policies) |
| **C-5 Release Engineering** | U-RE1 SemVer Policy <br> U-RE2 Release Train <br> U-RE3 Rollback Orchestrator | Bi-weekly release calendar, signed changelogs/SBOMs, 1-click rollback in Backstage | GitHub Actions, Syft, Argo Rollouts | Rollback < 30s <br> On-Time Release ≥ 90% | 1G (Cost Impact), 1F (Error Budget Abort) |

---

## **1C – Platform Engineering & DevEx Tree**

```
1C Platform Engineering & Developer Experience
│
├─ C-1 IDP Core & Self-Service
│   ├─ U-P1 Software Catalog
│   ├─ U-P2 Golden-Path Scaffolder
│   ├─ U-P3 Dev-Namespace Plugin
│   ├─ Responsibilities:
│   │   ├─ Backstage metadata maintenance
│   │   ├─ Project scaffolding ≤ 30s
│   │   └─ Namespace+SA with TTL=72h
│   └─ KPIs:
│       ├─ LTFC < 60 min
│       └─ Catalog Coverage ≥ 95%
│
├─ C-2 CI/CD Platform
│   ├─ U-CI1 Build & Cache Farm
│   ├─ U-CI2 Argo CD Control-Plane
│   ├─ U-CI3 Ephemeral Env Engine
│   ├─ Responsibilities:
│   │   ├─ GitOps Pipelines & Templates
│   │   ├─ Container signing (Cosign)
│   │   └─ Dev Namespaces w/ cleanup
│   └─ KPIs:
│       ├─ Deploys/day ≥ 20
│       └─ Failed Pipelines < 2%
│
├─ C-3 Runtime Services / Service Mesh
│   ├─ U-R1 Istio Ambient Mesh
│   ├─ U-R2 API Gateway (Envoy)
│   ├─ U-R3 Feature Flag / Canary
│   ├─ Responsibilities:
│   │   ├─ STRICT mTLS policy
│   │   ├─ Canary rollout ≤ 10 min
│   │   └─ Tier-based Rate Limit
│   └─ KPIs:
│       ├─ p99 latency < 100ms
│       └─ Canary Abort FP < 1%
│
├─ C-4 Dev Environment Tooling
│   ├─ U-DEV1 Local-K8s Kit
│   ├─ U-DEV2 Dev-Cluster Provisioner
│   ├─ U-DEV3 Dev-Secrets & TLS
│   ├─ Responsibilities:
│   │   ├─ Dev bootstrap kit (Mac/Linux)
│   │   ├─ Upgrade Dev w/ Prod parity
│   │   └─ Vault TTL = 24h
│   └─ KPIs:
│       ├─ Dev Bootstrap > 95%
│       └─ Dev Cluster Uptime ≥ 99%
│
└─ C-5 Release Engineering
    ├─ U-RE1 SemVer Policy
    ├─ U-RE2 Release Train Automation
    ├─ U-RE3 Rollback Orchestrator
    ├─ Responsibilities:
    │   ├─ Bi-weekly Release Calendar
    │   ├─ Signed Changelog & SBOM
    │   └─ 1-Click Rollback
    └─ KPIs:
        ├─ Rollback < 30s
        └─ On-Time Releases ≥ 90%
```

## **1D – Data & AI Infrastructure**

This updated version of the Data & AI Infrastructure layer introduces a complete and detailed structure including sub-units, responsibilities, core stack, measurable KPIs/SLOs, and inter-layer dependencies.

---

## 📌 Organizational Breakdown

| Squad | Sub-Units | End-to-End Responsibilities | Core Stack | KPI / SLO | Critical Dependencies |
|-------|-----------|-----------------------------|------------|-----------|------------------------|
| **D-1 Data Platform** | U-DP1 Hadoop Cluster Ops (HDFS + YARN) <br> U-DP2 Spark & Trino Engines <br> U-DP3 Kafka Backbone | Cluster setup/upgrade, capacity management, high availability | Hadoop 3.x, Spark 3.5, Trino 442, Kafka 3.7 | NameNode Uptime ≥ 99.9% <br> Job Fail < 1% <br> ISR ≤ 1 | PVC/GPU from 1B <br> ACL/SSL from 1E <br> SLO from 1F |
| **D-2 Data Engineering (Lakehouse & Pipelines)** | U-DE1 Lakehouse Ops (Iceberg Catalog) <br> U-DE2 Batch Pipelines (dbt + PySpark) <br> U-DE3 Realtime Pipelines (Flink SQL) | Iceberg schema design, batch ETL/ELT, real-time exactly-once streaming | Iceberg 1.5, dbt-core 1.9, PySpark, Flink 1.20 | Freshness ≤ 15 min <br> P99 Latency < 5s <br> DTI ≥ 0.9 | Kafka & Spark from D-1 <br> Lineage/Mask from D-4 |
| **D-3 ML & AI Platform** | U-ML1 Feature Store (Feast) <br> U-ML2 Training (Kubeflow, Ray) <br> U-ML3 Serving (MLflow, Seldon) | Feature → Train → Serve, Drift Monitoring, Canary Release | Feast 0.40, Kubeflow 2, Ray 3, MLflow 2.11 | Drift Alert < 10 min <br> p99 Serving < 50ms | GPU from 1B <br> Budget from 1G |
| **D-4 Governance & Observability** | U-GV1 Metadata Catalog (Atlas) <br> U-GV2 Lineage & DQ (OpenLineage + Soda) <br> U-GV3 Privacy (Ranger, Mask) | Metadata management, 100% lineage coverage, masking, GDPR deletion | Atlas 3, OpenLineage, SodaSQL, Ranger 3 | GDPR Ticket ≤ 72h <br> PII Incident = 0 | Policy with 1E <br> Tenant Alert with 1F |
| **D-5 BI & Semantic Services (Updated)** | U-BI1 Data Modeling & Pipeline Dev (dbt Semantic + Star/Vault) <br> U-BI2 Wide-Table & Aggregation Store (Materialized Views, Column Pruning) <br> U-BI3 Metric Layer & Query Acceleration (dbt-metrics, Cube.js, Caching) | Dimensional & Data Vault modeling, documented in dbt Docs <br> dbt/Flink pipelines for wide-tables and aggregate snapshots <br> Maintain materialized views, indexes, z-ordering <br> Semantic & Metric Layer for BI tools like Superset/Tableau | dbt Semantic Layer, Cube.js, Flink, MV/Indexing | Dashboard Latency P95 < 30s | Catalog from D-4 <br> Queries from 1C |

---

## **1D – Data & AI Infrastructure Tree**

```
1D Data & AI Infrastructure
│
├─ D-1 Data Platform
│   ├─ U-DP1 Hadoop Cluster Ops (HDFS + YARN)
│   ├─ U-DP2 Spark & Trino Engines
│   ├─ U-DP3 Kafka Backbone
│   ├─ Responsibilities:
│   │   ├─ Cluster Deployment & Upgrade
│   │   ├─ Capacity & HA Management
│   └─ KPIs:
│       ├─ NameNode Uptime ≥ 99.9%
│       ├─ Job Fail < 1%
│       └─ ISR ≤ 1
│
├─ D-2 Data Engineering (Lakehouse & Pipelines)
│   ├─ U-DE1 Lakehouse Ops (Iceberg Catalog)
│   ├─ U-DE2 Batch Pipelines (dbt + PySpark)
│   ├─ U-DE3 Realtime Pipelines (Flink SQL)
│   ├─ Responsibilities:
│   │   ├─ Iceberg Schema Design
│   │   ├─ Batch & Real-time ETL/ELT
│   │   └─ Exactly-Once Streaming
│   └─ KPIs:
│       ├─ Freshness ≤ 15 min
│       ├─ P99 Latency < 5s
│       └─ DTI ≥ 0.9
│
├─ D-3 ML & AI Platform
│   ├─ U-ML1 Feature Store (Feast)
│   ├─ U-ML2 Training (Kubeflow, Ray)
│   ├─ U-ML3 Serving (MLflow, Seldon)
│   ├─ Responsibilities:
│   │   ├─ Feature → Train → Serve
│   │   ├─ Drift Monitoring
│   │   └─ Canary Release
│   └─ KPIs:
│       ├─ Drift Alert < 10 min
│       └─ Serving p99 < 50ms
│
├─ D-4 Governance & Observability
│   ├─ U-GV1 Metadata Catalog (Atlas)
│   ├─ U-GV2 Lineage & DQ (OpenLineage, SodaSQL)
│   ├─ U-GV3 Privacy (Ranger, Mask)
│   ├─ Responsibilities:
│   │   ├─ Full Metadata & Lineage
│   │   ├─ Masking Policy & GDPR Delete
│   └─ KPIs:
│       ├─ GDPR Ticket ≤ 72h
│       └─ PII Incident = 0
│
└─ D-5 BI & Semantic Services 
    ├─ U-BI1 Data Modeling & Pipeline Dev
    ├─ U-BI2 Wide-Table & Aggregation Store
    ├─ U-BI3 Metric Layer & Query Acceleration
    ├─ Responsibilities:
    │   ├─ Dimensional & Vault Modeling in dbt Docs
    │   ├─ Pipelines for Wide-Tables & Aggregates
    │   ├─ Materialized Views, Indexing, Z-Order
    │   └─ BI Metric Layer for Superset/Tableau
    └─ KPIs:
        └─ Dashboard Latency P95 < 30s
```
## **1E – Security, Privacy & Compliance**

---

## 📌 Organizational Breakdown

| Squad | Sub-Units | Added Responsibilities | KPI / SLO |
|-------|-----------|-------------------------|-----------|
| **E-1 Security Engineering** | U-SE1 Red / Blue Team <br> U-SE2 PKI / KMS | SBOM Scanning, FIPS 140-3 compliant token issuance | CVE MTTP < 12 hours |
| **E-2 IAM / Zero-Trust** | U-IAM1 SSO <br> U-IAM2 SPIFFE / SPIRE | 24h certificate rotation, mTLS everywhere | SSO p95 < 200ms |
| **E-3 Privacy Engineering** | U-PR1 Differential Privacy <br> U-PR2 Right-to-Erase | Orchestration of Iceberg Row-Level Delete | Privacy P0 = 0 |
| **E-4 Compliance Operations** | U-CO1 SOC-2 Evidence Collection <br> U-CO2 GDPR Register | “Audit Gate” enforcement in Argo-CD | Audit Pass = 100% |

---

## **1E – Security, Privacy & Compliance Tree**

```
1E Security, Privacy & Compliance
│
├─ E-1 Security Engineering
│   ├─ U-SE1 Red / Blue Team
│   ├─ U-SE2 PKI / KMS
│   ├─ Responsibilities:
│   │   ├─ SBOM Scan
│   │   └─ FIPS 140-3 Token Issuance
│   └─ KPI:
│       └─ CVE MTTP < 12h
│
├─ E-2 IAM / Zero-Trust
│   ├─ U-IAM1 Single Sign-On (SSO)
│   ├─ U-IAM2 SPIFFE / SPIRE
│   ├─ Responsibilities:
│   │   ├─ Cert Rotation (24h)
│   │   └─ Enforce mTLS Everywhere
│   └─ KPI:
│       └─ SSO p95 < 200ms
│
├─ E-3 Privacy Engineering
│   ├─ U-PR1 Differential Privacy
│   ├─ U-PR2 Right-to-Erase
│   ├─ Responsibilities:
│   │   └─ Iceberg Row-Delete Orchestrator
│   └─ KPI:
│       └─ Privacy P0 = 0
│
└─ E-4 Compliance Ops
    ├─ U-CO1 SOC-2 Evidence Collection
    ├─ U-CO2 GDPR Register
    ├─ Responsibilities:
    │   └─ Audit-Gate in Argo-CD
    └─ KPI:
        └─ Audit Pass = 100%
```
## **1F – SRE Core (Reliability & Observability)**

This document captures the full structure, responsibilities, tools, KPIs, and cross-layer interfaces for the extended Reliability & Observability domain.

> **Note:** This layer **does not directly interface with 1D – Data & AI Infrastructure**.

---

## 📌 Organizational Breakdown

| Squad (Sub-Team) | Internal Units | Primary Responsibilities & Deliverables | Typical Stack / Tools | Key KPIs / SLOs | Critical Interfaces |
|------------------|----------------|------------------------------------------|------------------------|------------------|----------------------|
| **F-1 Observability Platform** | U-OB1 Metrics (Prometheus) <br> U-OB2 Logs (Loki) <br> U-OB3 Traces (Tempo, OTEL) | Central telemetry for all clusters/PoPs/VMs, exporter SDKs, dashboards, Thanos object store | Prometheus, Thanos, Loki, Tempo, Grafana, Jsonnet | Thanos Availability ≥ 99.95% <br> Cardinality Error < 0.1% | ◄ 1B (scrape endpoints) <br> ◄ 1C (CI metrics) <br> ◄ 1E (audit logs) |
| **F-2 Incident Command & Response** | U-IC1 PagerDuty Admin <br> U-IC2 Post-Mortem Office | 24/7 on-call, triage bridges, blameless RCA within 24h, IC training | PagerDuty, Slack bot, Zoom bridge, Incident SDK | MTTD < 5 min <br> MTTR < 30 min (Sev-1) | ◄ 1B/1C (owner escalations) <br> ◄ 1E (security incidents) |
| **F-3 Chaos & Resilience Engineering** | U-CH1 Fault-Injection <br> U-CH2 GameDay Program | Automated K8s chaos experiments, GameDay scenarios, publish resilience score | LitmusChaos, ChaosMesh, Gremlin | Resilience Score ≥ 0.90 | ◄ 1B (fault targets) <br> ◄ 1F-2 (incident drills) |
| **F-4 Performance & Capacity Reliability** | U-PC1 Load-Test Harness <br> U-PC2 Performance Budget Framework | k6/Locust libraries, SLO-budget API, feed capacity models to FinOps | k6, Locust, Python forecast, HPA/vPA | SLO Miss < 2% / quarter | ◄ 1C (pipeline perf) <br> ◄ 1G (capacity models) |
| **F-5 Reliability Automation & Tooling** *(new)* | U-RA1 Self-Healing Controllers <br> U-RA2 Toil-Buster Bots | Kubernetes controllers & Lambdas to auto-resolve recurring issues, chatops bots for runbooks | Go, Python, controller-runtime, Slack API | Toil Hours / Shift < 2h | ◄ 1F-2 (incident types) <br> ◄ 1B (cluster APIs) |
| **F-6 Release & Availability Engineering** *(new)* | U-RE1 SLO-Guard Admission Webhook <br> U-RE2 Prod-Readiness Board | Enforce error-budget guardrails, PRR checklist & reviews, rollback scripts | Gatekeeper/OPA, Argo Rollouts, Syft, ADR templates | Rollback Success = 100% <br> PRR Turnaround < 5 days | ◄ 1C (CI/CD gate) <br> ◄ 1B (webhooks) |

---

## **1F – SRE Core (Reliability & Observability) Tree**

```
1F Reliability & Observability (SRE Core – Extended)
│
├─ F-1 Observability Platform
│   ├─ U-OB1 Metrics (Prometheus)
│   ├─ U-OB2 Logs (Loki)
│   ├─ U-OB3 Traces (Tempo + OTEL)
│   ├─ Responsibilities:
│   │   ├─ Central Telemetry Stack
│   │   ├─ Exporter SDKs, Dashboards
│   │   └─ Multi-tenant Thanos Object Store
│   └─ KPIs: Thanos ≥ 99.95%, Cardinality Error < 0.1%
│
├─ F-2 Incident Command & Response
│   ├─ U-IC1 PagerDuty Admin
│   ├─ U-IC2 Post-Mortem Office
│   ├─ Responsibilities:
│   │   ├─ On-call rota, Paging Policy
│   │   ├─ RCA Template, 24h Publish
│   │   └─ Incident Commander Training
│   └─ KPIs: MTTD < 5 min, MTTR < 30 min
│
├─ F-3 Chaos & Resilience Engineering
│   ├─ U-CH1 Fault-Injection (Litmus)
│   ├─ U-CH2 GameDay Program
│   ├─ Responsibilities:
│   │   ├─ Chaos Scheduling (K8s Faults)
│   │   └─ Quarterly GameDays
│   └─ KPIs: Resilience Score ≥ 0.90
│
├─ F-4 Performance & Capacity Reliability
│   ├─ U-PC1 Load-Test Harness
│   ├─ U-PC2 Performance Budget Framework
│   ├─ Responsibilities:
│   │   ├─ Load Test Library (k6/Locust)
│   │   ├─ Global SLO API & Autoscale
│   │   └─ Feed Capacity Models
│   └─ KPIs: SLO Miss < 2% / Q
│
├─ F-5 Reliability Automation & Tooling
│   ├─ U-RA1 Self-Healing Controllers
│   ├─ U-RA2 Toil-Buster Bots
│   ├─ Responsibilities:
│   │   ├─ Auto-Remediation for Incidents
│   │   └─ ChatOps Bots for Runbooks
│   └─ KPIs: Toil < 2h / Shift
│
└─ F-6 Release & Availability Engineering
    ├─ U-RE1 SLO-Guard Admission Webhook
    ├─ U-RE2 Prod-Readiness Review Board
    ├─ Responsibilities:
    │   ├─ Block Deploys on SLO Exhaustion
    │   ├─ PRR Checklist + Review
    │   └─ Rollback Scripts
    └─ KPIs: 100% Rollback Success, PRR < 5d
```
