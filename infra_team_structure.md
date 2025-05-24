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

### What This Team Does:

This team handles everything physical in the infrastructure. They buy and manage equipment, keep inventory, test and set up servers, and build the datacenter network.

---

### 🔧 Team Details

| Team | Scope | What They Do |
|------|-------|--------------|
| **A-1 Buying & Vendor Management** | Vendor Relations, Budgeting | Work with suppliers, create purchase orders, manage datacenter hardware budgets |
| **A-2 Inventory & Warehousing** | Receiving, Tracking, Repairs | Receive equipment, track assets, handle broken items and recycling |
| **A-3 Server Hardware Setup** | Testing, Imaging, Rack Install | Test servers, load software, and install servers in racks |
| **A-4 Networking Setup in Datacenter** | Cabling, Switch Setup, Port Testing | Lay cables, configure switches/routers, and verify all network links |

---

### Summary Table

| Team | Description |
|------|-------------|
| **A-1 Buying & Vendor Management** | Handles vendor relationships and purchasing for all datacenter equipment. |
| **A-2 Inventory & Warehousing** | Manages inventory rooms, tracks all equipment, and handles repairs or recycling. |
| **A-3 Server Hardware Setup** | Prepares servers with necessary software and installs them into datacenter racks. |
| **A-4 Networking Setup in Datacenter** | Sets up network cables and hardware to ensure everything is connected properly. |

---

### **A – Team Tree View**

```
1A - Facilities & Physical Infrastructure
│
├─ A-1 Buying & Vendor Management
│   ├─ Scope:
│   │   ├─ Vendor Relations
│   │   ├─ Budgeting
│   ├─ Tasks:
│   │   ├─ Talk to vendors
│   │   ├─ Create purchase orders
│   │   └─ Manage costs and budgets
│
├─ A-2 Inventory & Warehousing
│   ├─ Scope:
│   │   ├─ Incoming Equipment
│   │   ├─ Asset Records
│   │   ├─ Repairs & Disposal
│   ├─ Tasks:
│   │   ├─ Receive equipment
│   │   ├─ Track all devices in records
│   │   ├─ Handle damaged items
│   │   └─ Recycle or dispose items properly
│
├─ A-3 Server Hardware Setup
│   ├─ Scope:
│   │   ├─ Hardware Testing
│   │   ├─ Server Imaging
│   │   ├─ Rack Installation
│   ├─ Tasks:
│   │   ├─ Test memory, disks, power, etc.
│   │   ├─ Load OS images or firmware
│   │   └─ Install and label servers in racks
│
└─ A-4 Networking Setup in Datacenter
    ├─ Scope:
    │   ├─ Network Cabling
    │   ├─ Switch & Router Setup
    │   ├─ Port Testing
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

### What This Area Does

This area provides the basic compute, storage, and networking services for all products. They run Kubernetes clusters, manage storage systems, and take care of both internal and external network connectivity.

---

### 🔧 Team Details

| Team | Scope | What They Do |
|------|-------|--------------|
| **B-1 Compute Platform** | Kubernetes Clusters, Node Management, OS Updates | Run Kubernetes clusters, manage different types of nodes, and update Linux kernels |
| **B-2 Storage Services** | Object & Block Storage, Managed Databases | Provide storage for files and volumes, and run reliable MySQL database clusters |
| **B-3 Network, Edge & Service Connectivity** | Networking, DNS, API Gateway, Service Mesh | Set up datacenter networks, handle DNS and IPs, secure internal traffic, and manage feature rollouts |

---

### Summary Table

| Team | Description |
|------|-------------|
| **B-1 Compute Platform** | Manages Kubernetes and Linux systems for running applications. |
| **B-2 Storage Services** | Offers reliable storage and database services for stateful apps. |
| **B-3 Network, Edge & Service Connectivity** | Handles all networking needs, from data center cabling to global edge routing and secure service communication. |

---

### **B – Team Tree View**

```
1B - Core Cloud Infrastructure & Platform
│
├─ B-1 Compute Platform
│   ├─ Scope:
│   │   ├─ Cluster Setup
│   │   ├─ Node Management
│   │   ├─ Kernel Updates
│   ├─ Tasks:
│   │   ├─ Manage Kubernetes clusters
│   │   ├─ Configure node pools
│   │   └─ Patch and maintain OS kernels
│
├─ B-2 Storage Services
│   ├─ Scope:
│   │   ├─ Object Storage (Ceph-S3)
│   │   ├─ Block Storage (RBD)
│   │   ├─ DB-as-a-Service (Vitess)
│   ├─ Tasks:
│   │   ├─ Provide file and volume storage
│   │   ├─ Ensure high availability and backups
│   │   └─ Manage MySQL databases with Vitess
│
└─ B-3 Network, Edge & Service Connectivity
    ├─ Scope:
    │   ├─ Data Center Networking (Spine-Leaf)
    │   ├─ POP / CDN Routing
    │   ├─ DNS / IPAM Management
    │   ├─ Istio Service Mesh
    │   ├─ API Gateway
    │   ├─ Feature Flags / Canary Releases
    ├─ Tasks:
    │   ├─ Build and maintain networks
    │   ├─ Route edge traffic via CDN
    │   ├─ Manage DNS zones and IPs
    │   ├─ Secure traffic with mTLS mesh
    │   ├─ Operate API gateways
    │   └─ Roll out features gradually
```
---
# **C – Platform Engineering & Developer Experience**

```
1C - Platform Engineering & Developer Experience
│
├─ C-1 IDP Core & Self-Service
├─ C-2 CI/CD Platform
├─ C-4 Dev Environment Tooling
└─ C-5 Release Engineering
```

### What This Area Does

This team helps developers move from writing code to getting it running in production easily. They provide tools to start new projects, run builds, test code, deploy to environments, and safely release updates.

---

### 🔧 Team Details

| Team | Scope | What They Do |
|------|-------|--------------|
| **C-1 IDP Core & Self-Service** | Developer Portal, Start New Projects, Dev Namespaces | Help developers find existing apps, start new ones fast, and get temporary environments to test them |
| **C-2 CI/CD Platform** | Build Systems, Deploy Pipelines, Test Environments | Run build and deploy pipelines, sign container images, and automatically clean up test setups |
| **C-4 Dev Environment Tooling** | Local Dev Setup, Shared Clusters, Secrets | Provide local development tools, create shared clusters that feel like production, and manage temporary passwords and certificates |
| **C-5 Release Engineering** | Release Calendar, Change Logs, Rollbacks | Automate releases, publish signed updates, and let teams undo a release with one click |

---

### Summary Table

| Team | Description |
|------|-------------|
| **C-1 IDP Core & Self-Service** | Lets developers find and start apps easily and test in short-term environments. |
| **C-2 CI/CD Platform** | Automates building, testing, and deploying apps with built-in security and cleanup. |
| **C-4 Dev Environment Tooling** | Gives developers the tools and environments to code and test just like production. |
| **C-5 Release Engineering** | Makes releases predictable, verifiable, and easy to roll back if needed. |

---

### **C – Team Tree View**

```
1C - Platform Engineering & Developer Experience
│
├─ C-1 IDP Core & Self-Service
│   ├─ Scope:
│   │   ├─ Developer Portal
│   │   ├─ New Project Setup
│   │   ├─ Temporary Environments
│   ├─ Tasks:
│   │   ├─ Show list of all current apps
│   │   ├─ Create new project setups fast
│   │   └─ Give 3-day dev environments
│
├─ C-2 CI/CD Platform
│   ├─ Scope:
│   │   ├─ Build and Cache Farm
│   │   ├─ GitOps Control (Argo CD)
│   │   ├─ Temporary Test Environments
│   ├─ Tasks:
│   │   ├─ Run build and test pipelines
│   │   ├─ Sign all container images
│   │   └─ Auto-clean short-lived environments
│
├─ C-4 Dev Environment Tooling
│   ├─ Scope:
│   │   ├─ Local Development Kit
│   │   ├─ Dev Cluster Setup
│   │   ├─ Secrets and TLS Management
│   ├─ Tasks:
│   │   ├─ One-command dev setup
│   │   ├─ Keep dev clusters like production
│   │   └─ Give temporary passwords and certificates
│
└─ C-5 Release Engineering
    ├─ Scope:
    │   ├─ Versioning Policy
    │   ├─ Automated Release Process
    │   ├─ Rollback Tools
    ├─ Tasks:
    │   ├─ Follow bi-weekly release schedule
    │   ├─ Publish signed changelogs and SBOMs
    │   └─ Provide one-click rollbacks
```
---
# **D – Data & AI Infrastructure**

```
1D - Data & AI Infrastructure
│
├─ D-1 Data Platform
├─ D-2 Data Engineering (Lakehouse & First-Class Pipelines)
├─ D-3 ML & AI Platform
├─ D-4 Governance & Observability
└─ D-5 BI & Semantic Services
```

### What This Team Does

This team builds and runs everything needed for working with data and AI. They manage big data systems, run data pipelines, support machine learning, enforce privacy rules, and prepare data for reports and dashboards.

---

### 🔧 Team Details

| Team | Scope | What They Do |
|------|-------|--------------|
| **D-1 Data Platform** | Hadoop, Spark, Trino, Kafka | Run big data systems for storing, processing, and streaming data |
| **D-2 Data Engineering** | Lakehouse (Iceberg), First-Class Pipelines | Build core data pipelines that move and transform data in batch and real-time |
| **D-3 ML & AI Platform** | ML Training, Feature Store, Model Serving | Train models, manage features, and serve models into applications |
| **D-4 Governance & Observability** | Metadata, Lineage, Privacy Rules | Track data use, check data quality, and apply privacy protections |
| **D-5 BI & Semantic Services** | Data Warehouse, OLAP Tables, Dashboards | Manage data warehouse and OLAP wide tables, prepare data models and pipeline outputs for BI dashboards |

---

### Summary Table

| Team | Description |
|------|-------------|
| **D-1 Data Platform** | Runs big data clusters and tools for processing and streaming data. |
| **D-2 Data Engineering** | Creates first-class pipelines for moving and transforming information. |
| **D-3 ML & AI Platform** | Supports AI workflows from training to live model use. |
| **D-4 Governance & Observability** | Tracks and protects data, and checks its quality. |
| **D-5 BI & Semantic Services** | Prepares data through pipelines and wide tables for BI and OLAP dashboards. |

---

### **D – Team Tree View**

```
1D - Data & AI Infrastructure
│
├─ D-1 Data Platform
│   ├─ Scope:
│   │   ├─ Hadoop Cluster
│   │   ├─ Spark & Trino Engines
│   │   ├─ Kafka Streaming
│   ├─ Tasks:
│   │   ├─ Set up and upgrade clusters
│   │   ├─ Keep systems highly available
│   │   └─ Manage real-time data flow
│
├─ D-2 Data Engineering (Lakehouse & First-Class Pipelines)
│   ├─ Scope:
│   │   ├─ Iceberg Lakehouse
│   │   ├─ Batch Pipelines (dbt, PySpark)
│   │   ├─ Realtime Pipelines (Flink SQL)
│   ├─ Tasks:
│   │   ├─ Define and manage data schemas
│   │   ├─ Build and run core ETL jobs
│   │   └─ Handle real-time data streams
│
├─ D-3 ML & AI Platform
│   ├─ Scope:
│   │   ├─ Feature Store (Feast)
│   │   ├─ Training Systems (Kubeflow, Ray)
│   │   ├─ Model Deployment (MLflow, Seldon)
│   ├─ Tasks:
│   │   ├─ Run model training jobs
│   │   ├─ Manage and store features
│   │   └─ Deploy and serve models
│
├─ D-4 Governance & Observability
│   ├─ Scope:
│   │   ├─ Metadata Catalog (Atlas)
│   │   ├─ Data Lineage & Quality (OpenLineage, Soda)
│   │   ├─ Privacy Controls (Ranger, Masking)
│   ├─ Tasks:
│   │   ├─ Maintain metadata and track usage
│   │   ├─ Run checks to ensure clean data
│   │   └─ Apply privacy and masking rules
│
└─ D-5 BI & Semantic Services
    ├─ Scope:
    │   ├─ Data Modeling & Pipelines
    │   ├─ Wide Tables & Aggregations
    │   ├─ Metrics & Query Performance
    │   ├─ OLAP Dashboards
    ├─ Tasks:
    │   ├─ Build reusable data models
    │   ├─ Create snapshot tables
    │   ├─ Manage data warehouse and OLAP tables
    │   └─ Speed up BI dashboards
```
---
# **E – Security, Privacy & Compliance**

```
1E - Security, Privacy & Compliance
│
├─ E-1 Security Engineering
├─ E-2 IAM / Zero-Trust
├─ E-3 Privacy Engineering
└─ E-4 Compliance Operations
```

### What This Team Does

This team keeps systems secure, protects user data, and makes sure the company follows all the rules. They manage logins, secure communication, data privacy tools, and prepare for audits.

---

### 🔧 Team Details

| Team | Scope | What They Do |
|------|-------|--------------|
| **E-1 Security Engineering** | Threat Detection, Token Security | Find and test for security weaknesses, manage secure tokens and software scans |
| **E-2 IAM / Zero-Trust** | Logins, Access Control, Certs | Run login systems, enforce strict access rules, manage short-lived security certificates |
| **E-3 Privacy Engineering** | Data Privacy, Deletion | Build tools that protect user data and allow secure data deletion |
| **E-4 Compliance Operations** | Audit Checks, Documentation | Prepare audit reports and manage legal/compliance documents and workflows |

---

### Summary Table

| Team | Description |
|------|-------------|
| **E-1 Security Engineering** | Finds risks and builds secure systems to protect the infrastructure. |
| **E-2 IAM / Zero-Trust** | Handles user access and makes sure services trust only what they should. |
| **E-3 Privacy Engineering** | Makes sure user data is handled safely and can be deleted if needed. |
| **E-4 Compliance Operations** | Keeps the organization ready for audits and legal checks. |

---

### **E – Team Tree View**

```
1E - Security, Privacy & Compliance
│
├─ E-1 Security Engineering
│   ├─ Scope:
│   │   ├─ Red / Blue Team
│   │   ├─ Token & Certificate Management
│   ├─ Tasks:
│   │   ├─ Scan software components (SBOM)
│   │   └─ Issue secure tokens
│
├─ E-2 IAM / Zero-Trust
│   ├─ Scope:
│   │   ├─ Single Sign-On (SSO)
│   │   ├─ SPIFFE / SPIRE (identity management)
│   ├─ Tasks:
│   │   ├─ Rotate certs every 24h
│   │   └─ Enforce secure (mTLS) connections
│
├─ E-3 Privacy Engineering
│   ├─ Scope:
│   │   ├─ Differential Privacy
│   │   ├─ Right-to-Erase Workflows
│   ├─ Tasks:
│   │   └─ Automate row-level deletes using Iceberg
│
└─ E-4 Compliance Operations
    ├─ Scope:
    │   ├─ SOC-2 Evidence Gathering
    │   ├─ GDPR Documentation
    ├─ Tasks:
    │   └─ Apply audit checks during deployments (Argo-CD)
```
---
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

### What This Team Does

This team keeps systems running smoothly. They track system health, respond to problems, test how systems behave under failure, run performance tests, and automate reliability tasks.

---

### 🔧 Team Details

| Team | Scope | What They Do |
|------|-------|--------------|
| **F-1 Observability Platform** | Metrics, Logs, Traces | Collect system data to monitor health and performance with dashboards |
| **F-2 Incident Command & Response** | On-call, RCA, Escalations | Handle outages with on-call teams, root cause analysis, and training |
| **F-3 Chaos & Resilience Engineering** | Chaos Tests, GameDays | Simulate failures to see how systems react and improve their recovery ability |
| **F-4 Performance & Capacity Reliability** | Load Testing, SLOs | Run performance tests, model system growth, and manage performance limits |
| **F-5 Reliability Automation & Tooling** | Auto-Healing, Bots | Build tools that fix known issues automatically and reduce manual work |
| **F-6 Release & Availability Engineering** | Deployment Checks, Rollbacks | Block risky releases, run readiness checks, and enable fast rollbacks |

---

### Summary Table

| Team | Description |
|------|-------------|
| **F-1 Observability Platform** | Collects and displays system data to detect issues early. |
| **F-2 Incident Command & Response** | Keeps services available by responding fast and learning from incidents. |
| **F-3 Chaos & Resilience Engineering** | Tests system stability using planned failures and learning exercises. |
| **F-4 Performance & Capacity Reliability** | Ensures systems stay fast and scalable through testing and models. |
| **F-5 Reliability Automation & Tooling** | Makes reliability tasks easier and faster with automation. |
| **F-6 Release & Availability Engineering** | Protects system health during releases using checks and quick rollbacks. |

---

### **F – Team Tree View**

```
1F - Reliability & Observability (SRE Core)
│
├─ F-1 Observability Platform
│   ├─ Scope:
│   │   ├─ Metrics (Prometheus)
│   │   ├─ Logs (Loki)
│   │   ├─ Traces (Tempo)
│   ├─ Tasks:
│   │   ├─ Operate dashboards and exporters
│   │   └─ Store data in Thanos
│
├─ F-2 Incident Command & Response
│   ├─ Scope:
│   │   ├─ PagerDuty Alerts
│   │   ├─ RCA & Postmortems
│   ├─ Tasks:
│   │   ├─ Manage on-call schedules
│   │   ├─ Handle bridge calls
│   │   └─ Train incident leads
│
├─ F-3 Chaos & Resilience Engineering
│   ├─ Scope:
│   │   ├─ Fault Injection (Litmus)
│   │   ├─ GameDay Events
│   ├─ Tasks:
│   │   ├─ Run failure scenarios
│   │   └─ Improve system recovery
│
├─ F-4 Performance & Capacity Reliability
│   ├─ Scope:
│   │   ├─ Load Testing (k6, Locust)
│   │   ├─ Capacity Planning
│   ├─ Tasks:
│   │   ├─ Test under load
│   │   ├─ Manage performance limits
│   │   └─ Support scaling needs
│
├─ F-5 Reliability Automation & Tooling
│   ├─ Scope:
│   │   ├─ Self-Healing Controllers
│   │   ├─ ChatOps Bots
│   ├─ Tasks:
│   │   ├─ Fix recurring problems
│   │   └─ Use bots to run playbooks
│
└─ F-6 Release & Availability Engineering
    ├─ Scope:
    │   ├─ SLO Checks
    │   ├─ Release Readiness
    │   ├─ Rollback Tools
    ├─ Tasks:
    │   ├─ Block risky deployments
    │   ├─ Review PRR checklists
    │   └─ Allow quick rollback
```
---
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

