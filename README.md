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
