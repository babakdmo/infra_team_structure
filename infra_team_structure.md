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
