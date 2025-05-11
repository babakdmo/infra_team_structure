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
