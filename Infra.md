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

### What This Team Does

This team manages the cost and growth of the infrastructure. They track cloud spending, manage budgets, plan future needs, and use automation to save money.

---

### 🔧 Team Details

| Team | Scope | What They Do |
|------|-------|--------------|
| **G-1 Cost Analytics** | Cloud Costs, Tagging Rules | Watch where money is spent, make sure deployments are tagged to track costs clearly |
| **G-2 Budget Governance** | Budgets, Reports, Slack Bots | Manage spending limits, build budget dashboards and reporting tools |
| **G-3 Capacity Modelling** | Forecasts, Spot Planning | Predict future infrastructure needs and plan spot instance usage |
| **G-4 Efficiency Engineering** | Autoscaling, Spot Pools | Build smart scaling tools to save money using automation and spot instances |

---

### Summary Table

| Team | Description |
|------|-------------|
| **G-1 Cost Analytics** | Tracks cloud costs and improves cost visibility using tagging tools. |
| **G-2 Budget Governance** | Manages budgets, sends updates via Slack, and automates cost tracking. |
| **G-3 Capacity Modelling** | Forecasts future needs and plans smart usage of cheaper compute resources. |
| **G-4 Efficiency Engineering** | Builds autoscalers and rightsizing tools to optimize usage and save cost. |

---

### **G – Team Tree View**

```
1G - FinOps & Capacity Engineering
│
├─ G-1 Cost Analytics
│   ├─ Scope:
│   │   ├─ Kubecost
│   │   ├─ CloudHealth
│   ├─ Tasks:
│   │   └─ Tag-before-Deploy enforcement in Argo-CD
│
├─ G-2 Budget Governance
│   ├─ Scope:
│   │   ├─ CapEx Planning
│   │   ├─ Cost API & Slack Bots
│   ├─ Tasks:
│   │   ├─ Manage budget via APIs
│   │   └─ Send reports using Slack
│
├─ G-3 Capacity Modelling
│   ├─ Scope:
│   │   ├─ Forecasting (Prophet)
│   │   ├─ Planning Scenarios
│   ├─ Tasks:
│   │   ├─ Plan 3-year capacity
│   │   └─ Use spot market data
│
└─ G-4 Efficiency Engineering
    ├─ Scope:
    │   ├─ Spot Pool Usage
    │   ├─ Autoscaling Strategies
    ├─ Tasks:
    │   ├─ Monitor spot usage
    │   └─ Automate instance rightsizing
```
---
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

### What This Team Does

This team connects products with users. They plan product features, test what works, set prices, improve user experience, and help customers succeed with training and support.

---

### 🔧 Team Details

| Team | Scope | What They Do |
|------|-------|--------------|
| **H-1 Product Strategy & Road-mapping** | Research, Planning | Talk to users, study the market, and create product plans every quarter |
| **H-2 Product-Ops & Analytics** | Metrics, Experiments | Track how products are used, run A/B tests, and measure what brings value |
| **H-3 Pricing, Packaging & GTM** | Pricing Plans, SLAs | Decide on pricing, manage contracts, and work with Sales and Finance |
| **H-4 UX Research & DevRel** | Usability, Docs, Advocacy | Improve how easy products are to use, write guides, and support developers |
| **H-5 Customer-Success & Support** | Onboarding, Support | Train users and solve issues through tickets and direct support |

---

### Summary Table

| Team | Description |
|------|-------------|
| **H-1 Product Strategy & Road-mapping** | Builds the product direction using user input and market analysis. |
| **H-2 Product-Ops & Analytics** | Tracks product usage and tests ideas for growth. |
| **H-3 Pricing, Packaging & GTM** | Sets prices and handles business contracts and revenue models. |
| **H-4 UX Research & DevRel** | Improves the product experience and supports developers with examples and guides. |
| **H-5 Customer-Success & Support** | Helps customers get started and solves their problems quickly. |

---

### **H – Team Tree View**

```
1H - Product, UX & Customer-Success Division
│
├─ H-1 Product Strategy & Road-mapping
│   ├─ Scope:
│   │   ├─ User Interviews
│   │   ├─ Market Analysis
│   │   ├─ Roadmap Creation
│   ├─ Tasks:
│   │   ├─ Talk to 8+ users per month
│   │   ├─ Analyze competitors
│   │   └─ Publish roadmap every 3 months
│
├─ H-2 Product-Ops & Analytics
│   ├─ Scope:
│   │   ├─ Product Metrics
│   │   ├─ A/B Testing
│   │   ├─ ROI Models
│   ├─ Tasks:
│   │   ├─ Track adoption and churn
│   │   ├─ Run growth experiments
│   │   └─ Measure feature value
│
├─ H-3 Pricing, Packaging & GTM
│   ├─ Scope:
│   │   ├─ Pricing Models
│   │   ├─ Contracts & SLAs
│   ├─ Tasks:
│   │   ├─ Define Free vs. Paid tiers
│   │   ├─ Work on legal SLAs
│   │   └─ Coordinate with sales/finance
│
├─ H-4 UX Research & DevRel
│   ├─ Scope:
│   │   ├─ Usability Testing
│   │   ├─ Docs and Tutorials
│   │   ├─ Developer Support
│   ├─ Tasks:
│   │   ├─ Test new features with users
│   │   ├─ Write sample code and articles
│   │   └─ Attend dev meetups
│
└─ H-5 Customer-Success & Support
    ├─ Scope:
    │   ├─ Onboarding Programs
    │   ├─ Support Tickets
    │   ├─ Training and Help
    ├─ Tasks:
    │   ├─ Respond to user tickets
    │   ├─ Deliver team training
    │   └─ Track response and resolution times
```
---
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

### What This Team Does

This team provides all the IT support employees need to do their work smoothly. They manage helpdesk tickets, laptops and devices, company networks, user logins (AD/SSO/MFA), voice services like phones and video calls, and IT equipment purchases.

---

### 🔧 Team Details

| Team | Scope | What They Do |
|------|-------|--------------|
| **IT-1 Service Desk & Endpoint Support** | Helpdesk, Devices, Patching | Respond to support tickets, set up and fix laptops, push updates |
| **IT-2 Enterprise Network Services** | LAN/Wi-Fi, Internet, Cabling | Run and fix office and WAN networks, monitor bandwidth, handle cabling |
| **IT-3 Systems & Identity Administration** | AD/SSO/MFA, Servers, Backup | Manage logins and access (AD, SSO, MFA), patch servers, run backups |
| **IT-4 Voice & Collaboration Services** | Phones, Zoom/Teams, Call Centers | Set up phones and video calls, manage call routing and call center tools |
| **IT-5 Asset & Procurement** | Buying, Inventory, Licenses | Order equipment, track devices, and handle software license records |

---

### Summary Table

| Team | Description |
|------|-------------|
| **IT-1 Service Desk & Endpoint Support** | Helps employees with devices and tickets, and keeps them patched. |
| **IT-2 Enterprise Network Services** | Runs the company network infrastructure, both wired and wireless. |
| **IT-3 Systems & Identity Administration** | Manages logins, server health, and safe storage and backups. |
| **IT-4 Voice & Collaboration Services** | Handles all calling tools and video communication services. |
| **IT-5 Asset & Procurement** | Tracks hardware and software and manages all IT purchases. |

---

### **I – Team Tree View**

```
1I - Corporate IT & End-User Services
│
├─ IT-1 Service Desk & Endpoint Support
│   ├─ Scope:
│   │   ├─ Ticket Support
│   │   ├─ Device Setup
│   │   ├─ Patch Management
│   ├─ Tasks:
│   │   ├─ Respond to IT tickets (L1/L2)
│   │   ├─ Set up and image devices
│   │   └─ Push patches and track RMA
│
├─ IT-2 Enterprise Network Services
│   ├─ Scope:
│   │   ├─ LAN & Wi-Fi Access
│   │   ├─ WAN & Internet Service
│   │   ├─ Network Cabling
│   ├─ Tasks:
│   │   ├─ Maintain switches and Wi-Fi
│   │   ├─ Monitor ISP usage
│   │   └─ Maintain physical network ports
│
├─ IT-3 Systems & Identity Administration
│   ├─ Scope:
│   │   ├─ Active Directory (AD)
│   │   ├─ Single Sign-On (SSO)
│   │   ├─ Multi-Factor Auth (MFA)
│   │   ├─ Server Patching
│   │   ├─ Storage & Backups
│   ├─ Tasks:
│   │   ├─ Apply login policies and MFA
│   │   ├─ Harden and patch servers
│   │   └─ Manage backups and restores
│
├─ IT-4 Voice & Collaboration Services
│   ├─ Scope:
│   │   ├─ VoIP Phones & PBX
│   │   ├─ Zoom/Teams Video
│   │   ├─ Call Center Tools
│   ├─ Tasks:
│   │   ├─ Set up voice menus and queues
│   │   ├─ Manage conferencing tools
│   │   └─ Track voice quality and usage
│
└─ IT-5 Asset & Procurement
    ├─ Scope:
    │   ├─ Procurement Workflow
    │   ├─ Hardware Inventory
    │   ├─ License Tracking
    ├─ Tasks:
    │   ├─ Order laptops and software
    │   ├─ Track assets with barcodes
    │   └─ Maintain software compliance
```
---
