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

### 🔧 Team Details

| Team | Sub-Teams | What They Do |
|------|-----------|--------------|
| **A-1 Buying & Vendor Management** | U-V1 Vendor Relations <br> U-V2 Budget & Planning | Talk to vendors, handle purchase orders, manage budgets |
| **A-2 Inventory & Warehousing** | U-W1 Incoming Equipment <br> U-W2 Asset Records <br> U-W3 Repairs & Disposal | Track incoming items, keep asset records, handle repairs and recycling |
| **A-3 Server Hardware Setup** | U-D1 Hardware Testing <br> U-D2 Server Prep & Imaging <br> U-D3 Rack Installation | Test server parts, install OS/images, put servers into racks |
| **A-4 Networking Setup in Datacenter** | U-N1 Network Cabling <br> U-N2 Switch & Router Setup <br> U-N3 Port Testing | Run cables, configure switches and routers, make sure connections work |

### Summary Table

| Team | Description |
|------|-------------|
| **A-1 Buying & Vendor Management** | Handles vendor relations and buying all datacenter equipment. |
| **A-2 Inventory & Warehousing** | Manages stock rooms, keeps track of all hardware, and handles recycling or broken items. |
| **A-3 Server Hardware Setup** | Makes sure servers are working correctly before putting them into production. |
| **A-4 Networking Setup in Datacenter** | Installs and configures networking equipment and cabling inside the datacenter. |

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
# **B – Core Cloud Infrastructure & Platform**

```
1B - Core Cloud Infrastructure & Platform
│
├─ B-1 Compute Platform
├─ B-2 Storage Services
└─ B-3 Network & Edge
```

### 💡 What This Team Does:

This team builds and manages the technical backbone of our private cloud. They take care of Kubernetes clusters, cloud storage, and software-defined networking across datacenters and edge locations.

---

### 🔧 Team Details

| Team | Sub-Teams | What They Do |
|------|-----------|--------------|
| **B-1 Compute Platform** | U-C1 Cluster-API <br> U-C2 NodePool <br> U-C3 Kernel Lifecycle | Deploy and manage Kubernetes clusters, handle different node types, manage and update Linux kernels |
| **B-2 Storage Services** | U-S1 Object Storage (Ceph-S3) <br> U-S2 Block Storage (RBD) <br> U-S3 DB-as-a-Service (Vitess) | Provide different storage options: object storage for files, block storage for volumes, and hosted databases |
| **B-3 Network & Edge** | U-N1 Spine-Leaf BGP-EVPN <br> U-N2 POP / CDN <br> U-N3 DNS / IPAM | Manage datacenter networking, optimize data delivery, and take care of DNS and IP address planning |

---

### **B – Team Tree View**

```
1B - Core Cloud Infrastructure & Platform
│
├─ B-1 Compute Platform
│   ├─ U-C1 Cluster-API
│   ├─ U-C2 NodePool
│   ├─ U-C3 Kernel Lifecycle
│   ├─ Tasks:
│   │   ├─ Manage Kubernetes clusters
│   │   ├─ Configure node pools
│   │   └─ Patch and manage Linux kernels
│
├─ B-2 Storage Services
│   ├─ U-S1 Object Storage (Ceph-S3)
│   ├─ U-S2 Block Storage (RBD)
│   ├─ U-S3 DB-as-a-Service (Vitess)
│   ├─ Tasks:
│   │   ├─ Provide object and block storage
│   │   ├─ Maintain storage reliability
│   │   └─ Run and support database hosting
│
└─ B-3 Network & Edge
    ├─ U-N1 Spine-Leaf BGP-EVPN
    ├─ U-N2 POP / CDN
    ├─ U-N3 DNS / IPAM
    ├─ Tasks:
    │   ├─ Build and manage network fabric
    │   ├─ Operate CDN and edge routing
    │   └─ Manage DNS zones and IP space
```
