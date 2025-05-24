# **Infra Team Structure**

```
Chief Infrastructure & Platform Officer (CIPO)
│
├─ [1] A - Facilities & Physical Infrastructure
├─ [2] B - Core Cloud Infrastructure & Platform
├─ [3] C - Platform Engineering & Developer Tools
├─ [4] D - Data & AI Infrastructure
├─ [5] E - Security, Privacy & Compliance
├─ [6] F - Site Reliability & Monitoring (SRE Core)
├─ [7] G - Cost Management & Capacity Planning
├─ [8] H - Product, UX & Customer Support
└─ [9] I - IT Support & Corporate Services
```

###  What This Structure Means:

Each section is a **team** responsible for a key area in infrastructure. Inside each team are **sub-teams** that handle more specific jobs. This structure helps us organize and manage all physical and cloud systems better.

---
# **A – Facilities & Physical Infrastructure**

```
1A - Facilities & Physical Infrastructure
│
├─ A-1 Buying & Vendor Management
├─ A-2 Inventory & Warehousing
├─ A-3 Server Hardware Setup
└─ A-4 Networking Setup in Datacenter
```

###  What This Team Does:

This team handles everything related to the physical part of the infrastructure. They manage procurement, store equipment, test and install servers, and wire up the datacenter network.

---

### 🔧 Team Details

| Team | Sub-Teams | What They Do |
|------|-----------|--------------|
| **A-1 Buying & Vendor Management** | U-V1 Vendor Relations <br> U-V2 Budget & Planning | Talk to vendors, handle purchase orders, manage budgets |
| **A-2 Inventory & Warehousing** | U-W1 Incoming Equipment <br> U-W2 Asset Records <br> U-W3 Repairs & Disposal | Track incoming items, keep asset records, handle repairs and recycling |
| **A-3 Server Hardware Setup** | U-D1 Hardware Testing <br> U-D2 Server Prep & Imaging <br> U-D3 Rack Installation | Test server parts, install OS/images, put servers into racks |
| **A-4 Networking Setup in Datacenter** | U-N1 Network Cabling <br> U-N2 Switch & Router Setup <br> U-N3 Port Testing | Run cables, configure switches and routers, make sure connections work |

---

### Summary Table

| Team | Description |
|------|-------------|
| **A-1 Buying & Vendor Management** | Handles vendor relations and buying all datacenter equipment. |
| **A-2 Inventory & Warehousing** | Manages stock rooms, keeps track of all hardware, and handles recycling or broken items. |
| **A-3 Server Hardware Setup** | Makes sure servers are working correctly before putting them into production. |
| **A-4 Networking Setup in Datacenter** | Installs and configures networking equipment and cabling inside the datacenter. |

---

### **A – Team Tree View**

```
1A - Facilities & Physical Infrastructure
│
├─ A-1 Buying & Vendor Management
│   ├─ U-V1 Vendor Relations
│   ├─ U-V2 Budget & Planning
│   ├─ Tasks:
│   │   ├─ Talk to vendors
│   │   ├─ Create purchase orders
│   │   └─ Manage costs and budgets
│
├─ A-2 Inventory & Warehousing
│   ├─ U-W1 Incoming Equipment
│   ├─ U-W2 Asset Records
│   ├─ U-W3 Repairs & Disposal
│   ├─ Tasks:
│   │   ├─ Receive equipment
│   │   ├─ Track all devices in records
│   │   ├─ Handle damaged items
│   │   └─ Recycle or dispose items properly
│
├─ A-3 Server Hardware Setup
│   ├─ U-D1 Hardware Testing
│   ├─ U-D2 Server Prep & Imaging
│   ├─ U-D3 Rack Installation
│   ├─ Tasks:
│   │   ├─ Test memory, disks, power, etc.
│   │   ├─ Load OS images or firmware
│   │   └─ Install and label servers in racks
│
└─ A-4 Networking Setup in Datacenter
    ├─ U-N1 Network Cabling
    ├─ U-N2 Switch & Router Setup
    ├─ U-N3 Port Testing
    ├─ Tasks:
    │   ├─ Connect cables to racks
    │   ├─ Configure switches and routers
    │   └─ Test and validate all ports and links
```
---

# **B – Core Cloud Infrastructure & Platform**

```
1B - Core Cloud Infrastructure & Platform
│
├─ B-1 Compute Platform
├─ B-2 Storage Services
└─ B-3 Network, Edge & Service Connectivity
```

## What This Area Does

This area provides the foundational compute, storage, and connectivity services that power every product environment—​from bare‑metal servers and Kubernetes nodes in our private datacentres to the multitenant service‑mesh that secures east‑west traffic. deliver a single, end‑to‑end service‑connectivity platform.

---

## 🔧 Team Details

| Team | Sub‑Units | What They Do |
|------|-----------|--------------|
| **B‑1 Compute Platform** | U‑C1 Cluster‑API <br> U‑C2 NodePool <br> U‑C3 Kernel Lifecycle | Deploy and operate Kubernetes clusters, manage heterogeneous node pools, patch and rollout Linux kernels |
| **B‑2 Storage Services** | U‑S1 Object Storage (Ceph‑S3) <br> U‑S2 Block Storage (RBD) <br> U‑S3 DB‑as‑a‑Service (Vitess) | Provide S3‑compatible object storage, persistent block volumes, and highly available Vitess‑backed MySQL clusters |
| **B‑3 Network, Edge & Service Connectivity** | U‑NE1 Spine‑Leaf BGP‑EVPN <br> U‑NE2 POP / CDN <br> U‑NE3 DNS / IPAM <br> U‑NE4 Istio Ambient Mesh <br> U‑NE5 API Gateway <br> U‑NE6 Feature Flags / Canary | Build & operate the L3/L4 network fabric, edge POPs and CDN, authoritative DNS & IP space, plus L7 mesh (STRICT mTLS), Envoy API gateway, rate‑limit tiers, and canary/feature‑flag rollout automation |

---

## Summary Table

| Team | Description |
|------|-------------|
| **B‑1 Compute Platform** | Runs all Kubernetes control planes and worker pools, including kernel lifecycle management. |
| **B‑2 Storage Services** | Delivers resilient object, block, and managed‑database services for stateful workloads. |
| **B‑3 Network, Edge & Service Connectivity** | Provides unified data‑centre networking, global edge distribution, service‑mesh security, API ingress, and progressive‑delivery tooling. |

---

## **B – Team Tree View**

```
1B - Core Cloud Infrastructure & Platform
│
├─ B-1 Compute Platform
│   ├─ U-C1 Cluster-API
│   ├─ U-C2 NodePool
│   ├─ U-C3 Kernel Lifecycle
│   ├─ Tasks:
│   │   ├─ Manage Kubernetes clusters
│   │   ├─ Configure heterogeneous node pools
│   │   └─ Patch and manage Linux kernels
│
├─ B-2 Storage Services
│   ├─ U-S1 Object Storage (Ceph-S3)
│   ├─ U-S2 Block Storage (RBD)
│   ├─ U-S3 DB-as-a-Service (Vitess)
│   ├─ Tasks:
│   │   ├─ Provide object and block storage
│   │   ├─ Maintain durability & replication
│   │   └─ Run and support Vitess clusters
│
└─ B-3 Network, Edge & Service Connectivity
    ├─ U-NE1 Spine-Leaf BGP-EVPN
    ├─ U-NE2 POP / CDN
    ├─ U-NE3 DNS / IPAM
    ├─ U-NE4 Istio Ambient Mesh
    ├─ U-NE5 API Gateway
    ├─ U-NE6 Feature Flags / Canary
    ├─ Tasks:
    │   ├─ Engineer & operate network fabric
    │   ├─ Run CDN pops & edge routing
    │   ├─ Manage DNS zones & IP space
    │   ├─ Enforce STRICT mTLS via mesh
    │   ├─ Operate Envoy gateway & policies
    │   ├─ Orchestrate canary & feature flags
    │   └─ Maintain p99 latency < 100 ms, network availability ≥ 99.99 %
```
---
# **1C – Platform Engineering & Developer Experience**

```
1C - Platform Engineering & Developer Experience
│
├─ C-1 IDP Core & Self-Service
├─ C-2 CI/CD Platform
├─ C-4 Dev Environment Tooling
└─ C-5 Release Engineering
```

## What This Area Does

Platform Engineering & DevEx gives every developer a smooth path from the first `git init` to a production roll‑out.  
It hosts the internal developer portal, shapes build and deploy pipelines, provides local and shared Kubernetes environments, and runs a predictable release train with instant rollbacks.

---

## 🔧 Team Details

| Team | Sub‑Units | What They Do |
|------|-----------|--------------|
| **C‑1 IDP Core & Self‑Service** | U‑P1 Software Catalog <br> U‑P2 Golden‑Path Scaffolder <br> U‑P3 Dev‑Namespace Plugin | Keep the service catalog fresh, scaffold new projects in <30 s, and give developers a temporary namespace that lasts 72 h |
| **C‑2 CI/CD Platform** | U‑CI1 Build & Cache Farm <br> U‑CI2 Argo CD Control‑Plane <br> U‑CI3 Ephemeral Env Engine | Provide ready‑to‑use build/test pipelines, sign every container image, and spin up short‑lived dev namespaces that clean themselves up |
| **C‑4 Dev Environment Tooling** | U‑DEV1 Local‑K8s Kit <br> U‑DEV2 Dev‑Cluster Provisioner <br> U‑DEV3 Dev‑Secrets & TLS | Offer a one‑command dev bootstrap, keep dev clusters close to prod, and hand out short‑lived secrets & TLS certs |
| **C‑5 Release Engineering** | U‑RE1 SemVer Policy <br> U‑RE2 Release Train Automation <br> U‑RE3 Rollback Orchestrator | Run a bi‑weekly release calendar, publish signed changelogs & SBOMs, and let teams roll back with one click |

---

## Summary Table

| Team | Description |
|------|-------------|
| **C‑1 IDP Core & Self‑Service** | Self‑service portal for metadata, scaffolding, and short‑lived dev namespaces. |
| **C‑2 CI/CD Platform** | End‑to‑end build, test, sign, and deploy pipelines with GitOps control. |
| **C‑4 Dev Environment Tooling** | Local and shared Kubernetes environments that mirror production and automate secrets. |
| **C‑5 Release Engineering** | Predictable release train, signed artefacts, and instant rollbacks. |

---

## **1C – Team Tree View**

```
1C - Platform Engineering & Developer Experience
│
├─ C-1 IDP Core & Self-Service
│   ├─ U-P1 Software Catalog
│   ├─ U-P2 Golden-Path Scaffolder
│   ├─ U-P3 Dev-Namespace Plugin
│   ├─ Tasks:
│   │   ├─ Keep service catalog fresh
│   │   ├─ Scaffold new projects in <30 s
│   │   └─ Give devs a 3‑day namespace
│
├─ C-2 CI/CD Platform
│   ├─ U-CI1 Build & Cache Farm
│   ├─ U-CI2 Argo CD Control-Plane
│   ├─ U-CI3 Ephemeral Env Engine
│   ├─ Tasks:
│   │   ├─ Maintain build & test pipelines
│   │   ├─ Sign container images
│   │   └─ Spin up & auto‑clean dev namespaces
│
├─ C-4 Dev Environment Tooling
│   ├─ U-DEV1 Local-K8s Kit
│   ├─ U-DEV2 Dev-Cluster Provisioner
│   ├─ U-DEV3 Dev-Secrets & TLS
│   ├─ Tasks:
│   │   ├─ Provide one‑command dev bootstrap
│   │   ├─ Keep dev clusters prod‑like
│   │   └─ Hand out short‑lived secrets & certs
│
└─ C-5 Release Engineering
    ├─ U-RE1 SemVer Policy
    ├─ U-RE2 Release Train Automation
    ├─ U-RE3 Rollback Orchestrator
    ├─ Tasks:
    │   ├─ Run bi‑weekly release calendar
    │   ├─ Publish signed changelogs & SBOMs
    │   └─ Offer one‑click rollback
```

---
# **D – Data & AI Infrastructure**

```
1D - Data & AI Infrastructure
│
├─ D-1 Data Platform
├─ D-2 Data Engineering (Lakehouse & Pipelines)
├─ D-3 ML & AI Platform
├─ D-4 Governance & Observability
└─ D-5 BI & Semantic Services
```

### What This Team Does:

This team provides the full data and AI backbone. They manage data clusters, process batch and streaming pipelines, support AI training and serving, enforce data governance, and build BI-friendly models and metrics.

---

### 🔧 Team Details

| Team | Sub-Teams | What They Do |
|------|-----------|--------------|
| **D-1 Data Platform** | U-DP1 Hadoop Cluster Ops (HDFS + YARN) <br> U-DP2 Spark & Trino Engines <br> U-DP3 Kafka Backbone | Maintain data clusters, manage Spark & Trino engines, and operate Kafka for real-time data |
| **D-2 Data Engineering (Lakehouse & Pipelines)** | U-DE1 Lakehouse Ops (Iceberg Catalog) <br> U-DE2 Batch Pipelines (dbt + PySpark) <br> U-DE3 Realtime Pipelines (Flink SQL) | Build and maintain batch and real-time data pipelines and manage data lake schemas |
| **D-3 ML & AI Platform** | U-ML1 Feature Store (Feast) <br> U-ML2 Training (Kubeflow, Ray) <br> U-ML3 Serving (MLflow, Seldon) | Run AI training pipelines, manage features, and deploy models into production |
| **D-4 Governance & Observability** | U-GV1 Metadata Catalog (Atlas) <br> U-GV2 Lineage & DQ (OpenLineage + Soda) <br> U-GV3 Privacy (Ranger, Mask) | Track data lineage, ensure data quality, and apply privacy policies |
| **D-5 BI & Semantic Services** | U-BI1 Data Modeling & Pipeline Dev <br> U-BI2 Wide-Table & Aggregation Store <br> U-BI3 Metric Layer & Query Acceleration | Build BI data models, create materialized views, and optimize dashboard performance |

---

### Summary Table

| Team | Description |
|------|-------------|
| **D-1 Data Platform** | Operates data processing engines and messaging systems at scale. |
| **D-2 Data Engineering** | Designs and runs batch and real-time pipelines in the data lakehouse. |
| **D-3 ML & AI Platform** | Manages ML pipelines from feature generation to live model serving. |
| **D-4 Governance & Observability** | Governs data security, privacy, metadata, and observability. |
| **D-5 BI & Semantic Services** | Prepares data for analytics with semantic layers, pipelines, and indexes. |

---

### **D – Team Tree View**

```
1D - Data & AI Infrastructure
│
├─ D-1 Data Platform
│   ├─ U-DP1 Hadoop Cluster Ops (HDFS + YARN)
│   ├─ U-DP2 Spark & Trino Engines
│   ├─ U-DP3 Kafka Backbone
│   ├─ Tasks:
│   │   ├─ Setup and upgrade clusters
│   │   ├─ Maintain high availability
│   │   └─ Manage streaming backbone
│
├─ D-2 Data Engineering (Lakehouse & Pipelines)
│   ├─ U-DE1 Lakehouse Ops (Iceberg Catalog)
│   ├─ U-DE2 Batch Pipelines (dbt + PySpark)
│   ├─ U-DE3 Realtime Pipelines (Flink SQL)
│   ├─ Tasks:
│   │   ├─ Define Iceberg schemas
│   │   ├─ Run ETL pipelines
│   │   └─ Process real-time data
│
├─ D-3 ML & AI Platform
│   ├─ U-ML1 Feature Store (Feast)
│   ├─ U-ML2 Training (Kubeflow, Ray)
│   ├─ U-ML3 Serving (MLflow, Seldon)
│   ├─ Tasks:
│   │   ├─ Manage training jobs
│   │   ├─ Track model features
│   │   └─ Serve models in production
│
├─ D-4 Governance & Observability
│   ├─ U-GV1 Metadata Catalog (Atlas)
│   ├─ U-GV2 Lineage & DQ (OpenLineage, SodaSQL)
│   ├─ U-GV3 Privacy (Ranger, Mask)
│   ├─ Tasks:
│   │   ├─ Maintain metadata and lineage
│   │   ├─ Run data quality checks
│   │   └─ Apply masking and privacy rules
│
└─ D-5 BI & Semantic Services
    ├─ U-BI1 Data Modeling & Pipeline Dev
    ├─ U-BI2 Wide-Table & Aggregation Store
    ├─ U-BI3 Metric Layer & Query Acceleration
    ├─ Tasks:
    │   ├─ Create and document data models
    │   ├─ Build and refresh wide-table snapshots
    │   └─ Maintain semantic and metric layers
```


# **E – Security, Privacy & Compliance**

```
1E - Security, Privacy & Compliance
│
├─ E-1 Security Engineering
├─ E-2 IAM / Zero-Trust
├─ E-3 Privacy Engineering
└─ E-4 Compliance Operations
```

### What This Team Does:

This team ensures enterprise-wide data security, privacy protections, and regulatory compliance. It manages secure authentication and encryption infrastructure, governs access controls, enforces data protection techniques, and coordinates audit-readiness and policy enforcement.

---

### 🔧 Team Details

| Team | Sub-Teams | What They Do |
|------|-----------|--------------|
| **E-1 Security Engineering** | U-SE1 Red / Blue Team <br> U-SE2 PKI / KMS | Conduct threat assessments, manage security tokens, and scan SBOMs |
| **E-2 IAM / Zero-Trust** | U-IAM1 SSO <br> U-IAM2 SPIFFE / SPIRE | Handle identity systems, enforce zero-trust principles, rotate certs, manage mTLS |
| **E-3 Privacy Engineering** | U-PR1 Differential Privacy <br> U-PR2 Right-to-Erase | Implement privacy-preserving analytics and deletion workflows |
| **E-4 Compliance Operations** | U-CO1 SOC-2 Evidence Collection <br> U-CO2 GDPR Register | Ensure audit readiness and manage compliance documentation |

---

### Summary Table

| Team | Description |
|------|-------------|
| **E-1 Security Engineering** | Performs penetration testing, manages secure token issuance and encryption services. |
| **E-2 IAM / Zero-Trust** | Manages user identity and authentication infrastructure with zero-trust enforcement. |
| **E-3 Privacy Engineering** | Designs systems for user data protection and supports regulatory data deletion. |
| **E-4 Compliance Operations** | Maintains compliance reporting, evidence gathering, and audit policy enforcement. |

---

### **E – Team Tree View**

```
1E - Security, Privacy & Compliance
│
├─ E-1 Security Engineering
│   ├─ U-SE1 Red / Blue Team
│   ├─ U-SE2 PKI / KMS
│   ├─ Tasks:
│   │   ├─ SBOM Scan
│   │   └─ FIPS 140-3 Token Issuance
│
├─ E-2 IAM / Zero-Trust
│   ├─ U-IAM1 Single Sign-On (SSO)
│   ├─ U-IAM2 SPIFFE / SPIRE
│   ├─ Tasks:
│   │   ├─ Cert Rotation (24h)
│   │   └─ Enforce mTLS Everywhere
│
├─ E-3 Privacy Engineering
│   ├─ U-PR1 Differential Privacy
│   ├─ U-PR2 Right-to-Erase
│   ├─ Tasks:
│   │   └─ Iceberg Row-Delete Orchestrator
│
└─ E-4 Compliance Operations
    ├─ U-CO1 SOC-2 Evidence Collection
    ├─ U-CO2 GDPR Register
    ├─ Tasks:
    │   └─ Audit-Gate in Argo-CD
```

# **F – SRE Core (Reliability & Observability)**

```
1F - Reliability & Observability (SRE Core)
│
├─ F-1 Observability Platform
├─ F-2 Incident Command & Response
├─ F-3 Chaos & Resilience Engineering
├─ F-4 Performance & Capacity Reliability
├─ F-5 Reliability Automation & Tooling
└─ F-6 Release & Availability Engineering
```

### What This Team Does:

This team ensures system uptime, performance, and resilience across the entire platform. They build and maintain observability stacks, run incident command practices, engineer chaos and failure simulations, enforce release reliability, and implement automation for long-term stability.

---

### 🔧 Team Details

| Team | Sub-Teams | What They Do |
|------|-----------|--------------|
| **F-1 Observability Platform** | U-OB1 Metrics (Prometheus) <br> U-OB2 Logs (Loki) <br> U-OB3 Traces (Tempo, OTEL) | Operate the telemetry stack including metrics, logs, and traces, with exporters and dashboards |
| **F-2 Incident Command & Response** | U-IC1 PagerDuty Admin <br> U-IC2 Post-Mortem Office | Manage 24/7 on-call duties, run blameless RCA, coordinate major incident response |
| **F-3 Chaos & Resilience Engineering** | U-CH1 Fault-Injection <br> U-CH2 GameDay Program | Execute chaos engineering drills, automate fault injection, run GameDays for resilience |
| **F-4 Performance & Capacity Reliability** | U-PC1 Load-Test Harness <br> U-PC2 Performance Budget Framework | Maintain performance testing and forecasting infrastructure; enforce capacity models |
| **F-5 Reliability Automation & Tooling** | U-RA1 Self-Healing Controllers <br> U-RA2 Toil-Buster Bots | Automate reliability operations using controllers, bots, and chatops tooling |
| **F-6 Release & Availability Engineering** | U-RE1 SLO-Guard Admission Webhook <br> U-RE2 Prod-Readiness Board | Enforce release guardrails using admission control and readiness checklists |

---

### Summary Table

| Team | Description |
|------|-------------|
| **F-1 Observability Platform** | Runs telemetry infrastructure (metrics, logs, traces) to support platform observability. |
| **F-2 Incident Command & Response** | Ensures high availability and incident management through structured on-call response. |
| **F-3 Chaos & Resilience Engineering** | Tests system failure readiness through fault injection and GameDay simulations. |
| **F-4 Performance & Capacity Reliability** | Validates system scalability and performance budgets via load testing and forecasts. |
| **F-5 Reliability Automation & Tooling** | Develops bots and controllers to automatically address recurring issues and reduce toil. |
| **F-6 Release & Availability Engineering** | Protects reliability with deployment checks, rollback mechanisms, and readiness processes. |

---

### **F – Team Tree View**

```
1F - Reliability & Observability (SRE Core – Extended)
│
├─ F-1 Observability Platform
│   ├─ U-OB1 Metrics (Prometheus)
│   ├─ U-OB2 Logs (Loki)
│   ├─ U-OB3 Traces (Tempo + OTEL)
│   ├─ Tasks:
│   │   ├─ Central Telemetry Stack
│   │   ├─ Exporter SDKs, Dashboards
│   │   └─ Multi-tenant Thanos Object Store
│
├─ F-2 Incident Command & Response
│   ├─ U-IC1 PagerDuty Admin
│   ├─ U-IC2 Post-Mortem Office
│   ├─ Tasks:
│   │   ├─ On-call rota, Paging Policy
│   │   ├─ RCA Template, 24h Publish
│   │   └─ Incident Commander Training
│
├─ F-3 Chaos & Resilience Engineering
│   ├─ U-CH1 Fault-Injection (Litmus)
│   ├─ U-CH2 GameDay Program
│   ├─ Tasks:
│   │   ├─ Chaos Scheduling (K8s Faults)
│   │   └─ Quarterly GameDays
│
├─ F-4 Performance & Capacity Reliability
│   ├─ U-PC1 Load-Test Harness
│   ├─ U-PC2 Performance Budget Framework
│   ├─ Tasks:
│   │   ├─ Load Test Library (k6/Locust)
│   │   ├─ Global SLO API & Autoscale
│   │   └─ Feed Capacity Models
│
├─ F-5 Reliability Automation & Tooling
│   ├─ U-RA1 Self-Healing Controllers
│   ├─ U-RA2 Toil-Buster Bots
│   ├─ Tasks:
│   │   ├─ Auto-Remediation for Incidents
│   │   └─ ChatOps Bots for Runbooks
│
└─ F-6 Release & Availability Engineering
    ├─ U-RE1 SLO-Guard Admission Webhook
    ├─ U-RE2 Prod-Readiness Review Board
    ├─ Tasks:
    │   ├─ Block Deploys on SLO Exhaustion
    │   ├─ PRR Checklist + Review
    │   └─ Rollback Scripts
```
# **G – FinOps & Capacity Engineering**

```
1G - FinOps & Capacity Engineering
│
├─ G-1 Cost Analytics
├─ G-2 Budget Governance
├─ G-3 Capacity Modelling
└─ G-4 Efficiency Engineering
```

### What This Team Does:

This team is responsible for optimizing financial efficiency, managing infrastructure budgets, projecting future capacity needs, and engineering cost-effective scaling mechanisms. They align technical capacity planning with financial strategies to ensure scalable, affordable infrastructure growth.

---

### 🔧 Team Details

| Team | Sub-Teams | What They Do |
|------|-----------|--------------|
| **G-1 Cost Analytics** | U-FA1 Kubecost <br> U-FA2 CloudHealth | Monitor and analyze cost data, enforce pre-deployment tagging policies for cost visibility |
| **G-2 Budget Governance** | U-BG1 CapEx Board <br> U-BG2 Charge-Back | Manage budget exposure via APIs, automate reporting with bots, and govern budget limits |
| **G-3 Capacity Modelling** | U-CM1 Prophet Forecast <br> U-CM2 Scenario Planning | Forecast infrastructure needs for long-term planning and optimize spot market purchases |
| **G-4 Efficiency Engineering** | U-EE1 Spot Pool <br> U-EE2 Autoscaler | Engineer autoscaling and rightsizing strategies using spot market and automation tools |

---

### Summary Table

| Team | Description |
|------|-------------|
| **G-1 Cost Analytics** | Provides cost visibility and policy enforcement via tools like Kubecost and CloudHealth. |
| **G-2 Budget Governance** | Establishes budget policies and implements financial observability with Slack and APIs. |
| **G-3 Capacity Modelling** | Builds long-term infrastructure forecasts and spot usage strategies with ML-based planners. |
| **G-4 Efficiency Engineering** | Automates cost-efficient scaling and resource optimization with autoscalers and spot pools. |

---

### **G – Team Tree View**

```
1G - FinOps & Capacity Engineering
│
├─ G-1 Cost Analytics
│   ├─ U-FA1 Kubecost
│   ├─ U-FA2 CloudHealth
│   ├─ Tasks:
│   │   └─ Enforce "Tag-before-Deploy" in Argo-CD
│
├─ G-2 Budget Governance
│   ├─ U-BG1 CapEx Board
│   ├─ U-BG2 Charge-Back
│   ├─ Tasks:
│   │   ├─ Budget API
│   │   └─ /cost-breakdown Slack Bot
│
├─ G-3 Capacity Modelling
│   ├─ U-CM1 Prophet Forecast
│   ├─ U-CM2 Scenario Planning
│   ├─ Tasks:
│   │   ├─ 3-Year DC Expansion Plan
│   │   └─ Spot Market Plan
│
└─ G-4 Efficiency Engineering
    ├─ U-EE1 Spot Pool
    ├─ U-EE2 Autoscaler
    ├─ Tasks:
    │   ├─ Spot Coverage Monitoring
    │   └─ Rightsizing Automation
```

# **H – Product, UX & Customer-Success Division**

```
1H - Product, UX & Customer-Success Division
│
├─ H-1 Product Strategy & Road-mapping
├─ H-2 Product-Ops & Analytics
├─ H-3 Pricing, Packaging & GTM
├─ H-4 UX Research & DevRel
└─ H-5 Customer-Success & Support
```

### What This Team Does:

This division bridges product direction with user needs, go-to-market strategies, customer success, and experience design. It drives roadmap alignment, adoption analytics, pricing strategies, documentation, and onboarding efforts across internal and external stakeholders.

---

### 🔧 Team Details

| Team | Sub-Teams | What They Do |
|------|-----------|--------------|
| **H-1 Product Strategy & Road-mapping** | U-PS1 Market/User Research <br> U-PS2 Opportunity Backlog (Lean Canvas) | Conduct user interviews, analyze competitive markets, maintain quarterly product roadmaps |
| **H-2 Product-Ops & Analytics** | U-PO1 KPI Instrumentation <br> U-PO2 Growth Experiments | Define product metrics, run experiments, and build feature-level ROI insights |
| **H-3 Pricing, Packaging & GTM** | U-PP1 Pricing Model <br> U-PP2 Contracts & SLA | Define pricing plans, maintain SLAs, collaborate on business models with Sales/Finance |
| **H-4 UX Research & DevRel** | U-UX1 Journey Mapping <br> U-DR1 Developer Advocacy | Run UX research, write documentation and articles, support the developer community |
| **H-5 Customer-Success & Support** | U-CS1 Onboarding <br> U-CS2 Technical Account Mgmt. (TAM) | Provide support and training for internal and external product users |

---

### Summary Table

| Team | Description |
|------|-------------|
| **H-1 Product Strategy & Road-mapping** | Guides product direction through market research and stakeholder feedback. |
| **H-2 Product-Ops & Analytics** | Measures success metrics and runs A/B tests for growth and retention. |
| **H-3 Pricing, Packaging & GTM** | Designs pricing models and works with business units to maintain profitability. |
| **H-4 UX Research & DevRel** | Improves developer/user experience and provides learning resources. |
| **H-5 Customer-Success & Support** | Supports onboarding, training, and issue resolution for product users. |

---

### **H – Team Tree View**

```
1H - Product, UX & Customer-Success Division
│
├─ H-1 Product Strategy & Road-mapping
│   ├─ U-PS1 Market/User Research
│   ├─ U-PS2 Opportunity Backlog
│   ├─ Tasks:
│   │   ├─ Monthly User Interviews
│   │   ├─ Competitive/TAM Analysis
│   │   └─ Quarterly Roadmaps
│
├─ H-2 Product-Ops & Analytics
│   ├─ U-PO1 KPI Instrumentation
│   ├─ U-PO2 Growth Experiments
│   ├─ Tasks:
│   │   ├─ Adoption & Churn Metrics
│   │   ├─ A/B Testing
│   │   └─ ROI Models
│
├─ H-3 Pricing, Packaging & GTM
│   ├─ U-PP1 Pricing Model
│   ├─ U-PP2 Contracts & SLA
│   ├─ Tasks:
│   │   ├─ Free vs. Premium Plans
│   │   ├─ Legal DPA/SLA
│   │   └─ Sales/Finance Collab for P&L
│
├─ H-4 UX Research & DevRel
│   ├─ U-UX1 Journey Mapping
│   ├─ U-DR1 Developer Advocacy
│   ├─ Tasks:
│   │   ├─ Backstage Usability Testing
│   │   ├─ Docs, Sample Code, Talks
│
└─ H-5 Customer-Success & Support
    ├─ U-CS1 Onboarding
    ├─ U-CS2 Technical Account Mgmt. (TAM)
    ├─ Tasks:
    │   ├─ Ticket SLA (L1/L2)
    │   └─ Enablement Training
```

# **I – Corporate IT & End-User Services**

```
1I - Corporate IT & End-User Services
│
├─ IT-1 Service Desk & Endpoint Support
├─ IT-2 Enterprise Network Services
├─ IT-3 Systems & Identity Administration
├─ IT-4 Voice & Collaboration Services
└─ IT-5 Asset & Procurement
```

### What This Team Does:

This team supports the enterprise’s technology backbone for internal users. They handle everything from helpdesk tickets and device provisioning to network operations, identity systems, voice services, and IT procurement. They ensure employees are well-supported, connected, and securely provisioned.

---

### 🔧 Team Details

| Team | Sub-Teams | What They Do |
|------|-----------|--------------|
| **IT-1 Service Desk & Endpoint Support** | U-SD1 Ticket Triage <br> U-SD2 MDM Provisioning <br> U-SD3 Knowledge Base | Resolve helpdesk tickets, manage endpoint devices, maintain knowledge articles |
| **IT-2 Enterprise Network Services** | U-NN1 LAN & Wi-Fi <br> U-NN2 WAN & ISP <br> U-NN3 Cabling | Maintain campus and WAN networking infrastructure, ISP liaison, structured cabling |
| **IT-3 Systems & Identity Administration** | U-SI1 AD/SSO/MFA <br> U-SI2 System Admin <br> U-SI3 Storage/File Services | Administer Active Directory, VM/server patching, file servers, and backups |
| **IT-4 Voice & Collaboration Services** | U-VC1 VoIP/PBX <br> U-VC2 Conferencing <br> U-VC3 Call Center Ops | Operate corporate telephony, conferencing tools, and voice recording infrastructure |
| **IT-5 Asset & Procurement** | U-AP1 Procurement <br> U-AP2 Inventory <br> U-AP3 License Management | Manage IT procurement, maintain accurate inventory, and oversee software licensing |

---

### Summary Table

| Team | Description |
|------|-------------|
| **IT-1 Service Desk & Endpoint Support** | Provides support for devices and helpdesk tickets to ensure endpoint readiness. |
| **IT-2 Enterprise Network Services** | Operates and monitors the LAN/WAN networking and structured cabling environment. |
| **IT-3 Systems & Identity Administration** | Maintains identity and access systems, server health, and backup services. |
| **IT-4 Voice & Collaboration Services** | Manages voice infrastructure, conferencing platforms, and internal communications. |
| **IT-5 Asset & Procurement** | Handles purchasing, inventory, and license tracking of corporate IT resources. |

---

### **I – Team Tree View**

```
1I - Corporate IT & End-User Services
│
├─ IT-1 Service Desk & Endpoint Support
│   ├─ U-SD1 Ticket Triage & Remote Support
│   ├─ U-SD2 MDM Provisioning (Intune/Jamf)
│   ├─ U-SD3 Knowledge Base
│   ├─ Tasks:
│   │   ├─ L1/L2 Ticket Response
│   │   ├─ Device Provisioning w/ Golden Image
│   │   └─ Weekly Patch & RMA Management
│
├─ IT-2 Enterprise Network Services
│   ├─ U-NN1 LAN & Wireless
│   ├─ U-NN2 WAN & ISP
│   ├─ U-NN3 Cabling & Ports
│   ├─ Tasks:
│   │   ├─ Switch/Wi-Fi Backbone
│   │   ├─ Internet Bandwidth Monitoring
│   │   └─ Cabling Maintenance
│
├─ IT-3 Systems & Identity Administration
│   ├─ U-SI1 AD/SSO/MFA
│   ├─ U-SI2 Server & VM Admin
│   ├─ U-SI3 File & Storage Services
│   ├─ Tasks:
│   │   ├─ AD/SSO/MFA Policy
│   │   ├─ Server Hardening & Patch
│   │   └─ Backup/DR Implementation
│
├─ IT-4 Voice & Collaboration Services
│   ├─ U-VC1 VoIP & PBX
│   ├─ U-VC2 Conferencing (Teams/Zoom)
│   ├─ U-VC3 Call Center Ops
│   ├─ Tasks:
│   │   ├─ IVR, Queueing & Call Setup
│   │   ├─ Conferencing Tools & Licenses
│   │   └─ QoS Monitoring & Reporting
│
└─ IT-5 Asset & Procurement
    ├─ U-AP1 Procurement & Vendor Contracts
    ├─ U-AP2 Inventory & Warehousing
    ├─ U-AP3 License Management
    ├─ Tasks:
    │   ├─ IT Purchasing Workflow
    │   ├─ Inventory + Barcode Tracking
    │   └─ License CMDB Accuracy
```

