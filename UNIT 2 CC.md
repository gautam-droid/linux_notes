### **Cloud Service Models**: service levels, user-managed vs provider-managed, SaaS, PaaS, IaaS

---

### **1. Software as a Service (SaaS)**

**Definition**: ready-to-use software over the internet, hosted & managed by provider

**Key Characteristics**

- No local installation
    
- Web access from any location
    
- Subscription/pay-as-you-go
    
- Automatic updates
    
- Multi-tenant architecture
    

**User Responsibility**: data, user settings  
**Provider Responsibility**: infrastructure, runtime, middleware, app, security

**Examples**

- Google Workspace (Gmail, Docs, Sheets)
    
- Microsoft Office 365
    
- Salesforce (CRM)
    
- Dropbox (cloud file storage)
    

---

### **2. Platform as a Service (PaaS)**

**Definition**: platform for developers to build, deploy, and manage applications without handling infrastructure

**Key Characteristics**

- No infrastructure management
    
- Provides tools, frameworks, databases, middleware
    
- Supports multiple languages
    
- Fast development & deployment
    
- Auto-scaling
    

**User Responsibility**: application code, data  
**Provider Responsibility**: infrastructure, OS, runtime, middleware, security

**Examples**

- Google App Engine
    
- Microsoft Azure App Service
    
- Heroku
    
- AWS Elastic Beanstalk
    

---

### **3. Infrastructure as a Service (IaaS)**

**Definition**: virtualized computing resources (VMs, storage, network) delivered over the internet

**Key Characteristics**

- Raw infrastructure access
    
- Full OS and software control
    
- On-demand scaling
    
- Pay-as-you-go
    
- User manages OS, middleware, runtime
    

**User Responsibility**: OS, applications, middleware, data, runtime  
**Provider Responsibility**: physical hardware, storage, networking, virtualization

**Examples**

- Amazon EC2
    
- Google Compute Engine
    
- Microsoft Azure Virtual Machines
    
- IBM Cloud Infrastructure
    

---

---

### **Service-Oriented Architecture (SOA)**: modular services, loose coupling, interoperability, cloud integration

---

#### **What is SOA?**

- Design approach: service-based
    
- Communication: network protocols
    
- Characteristics: loosely coupled, reusable, discoverable
    
- Performs: specific business functions
    

#### **Key Concepts**

- **Service**: unit of functionality (e.g., customer data, payments)
    
- **Loose Coupling**: minimal dependency
    
- **Interoperability**: standard protocols
    
- **Discoverability**: services in a registry
    
- **Reusability**: reusable across apps/processes
    

#### **Core Components of SOA**

- **Service Provider**: creates, publishes services
    
- **Service Consumer**: consumes services
    
- **Service Registry**: directory of services
    
- **Service Contract**: defines interfaces/protocols
    

---

#### **How SOA Works**

- Breaks complex apps into smaller services
    
- Independent development & deployment
    
- Communicates via: web services (SOAP, REST), messaging
    

---

### **SOA in Cloud Computing**

#### **1. SOA as Foundation for Cloud Design**

- **Modularity & Reusability**: storage, databases, authentication
    
- **Loose Coupling**: independent evolution, scalability
    
- **Standardized Communication**: HTTP, REST, SOAP, messaging queues
    

#### **2. SOA in Cloud Implementation**

- **Service Composition**: combining services (auth, payment, processing)
    
- **Multi-Tenancy**: shared services for many users
    
- **Elasticity & Dynamic Binding**: dynamic service allocation
    
- **Integration**: hybrid cloud, service interfaces
    

---

### **Conceptual Cloud Model**: abstraction of cloud services, layer-based delivery, infrastructure to end-user

---

#### **Three Core Layers of Cloud Model**

- **IaaS (Infrastructure as a Service)**
    
    - Provides: VMs, storage, network
        
    - User Responsibility: OS, middleware, apps
        
    - Examples: Amazon EC2, Azure VMs
        
- **PaaS (Platform as a Service)**
    
    - Provides: dev platforms, tools, databases
        
    - User Responsibility: app code, deployment
        
    - Examples: Google App Engine, Heroku
        
- **SaaS (Software as a Service)**
    
    - Provides: ready-made apps
        
    - User Responsibility: app usage, managing user data
        
    - Examples: Gmail, Office 365, Salesforce
        

---

#### **Additional Layers (optional in some models)**

- **BPaaS**: Business Process as a Service
    
- **SECaaS**: Security as a Service
    

---

#### **How the Layers Work Together**

- **IaaS**: foundation infrastructure
    
- **PaaS**: built on IaaS, adds dev tools
    
- **SaaS**: uses PaaS & IaaS to deliver apps
    

---

---

### **Cloud Stack**: layered technologies, cloud infrastructure, build-deploy-operate, foundation of cloud services

---

### **What is a Cloud Stack?**

- Technology stack for cloud computing
    
- Combines hardware, software, virtualization
    
- Enables cloud functionalities: storage, compute, networking, applications
    

---

### **Components of a Cloud Stack**

#### **1. Hardware Layer (Physical Infrastructure)**

- Physical servers
    
- Storage devices
    
- Networking equipment: switches, routers
    
- Data centers
    
- Power & rack systems
    

#### **2. Virtualization Layer**

- Abstracts hardware into virtual machines
    
- Enables resource pooling & efficiency
    
- Tools: VMware ESXi, Microsoft Hyper-V, KVM
    

#### **3. Infrastructure Layer (IaaS)**

- Provides virtual compute, storage, and network
    
- User-managed provisioning
    
- Examples: Amazon EC2, OpenStack, Azure VMs
    

#### **4. Platform Layer (PaaS)**

- OS, middleware, runtime environments
    
- App development support
    
- Hides infrastructure complexity
    
- Examples: Google App Engine, Heroku, Azure App Services
    

#### **5. Application Layer (SaaS)**

- Full-featured software over the internet
    
- No infrastructure or platform management by user
    
- Examples: Gmail, Salesforce, Dropbox
    

#### **6. Management and Orchestration Layer**

- Automation tools
    
- Deployment & resource monitoring
    
- Billing, performance, security
    
- Examples: Kubernetes, OpenStack Horizon, CloudStack
    

---

### **Significance of Cloud Stack in Cloud Computing**

- **End-to-End Solution**: full system from hardware to application
    
- **Resource Abstraction & Efficiency**: virtualization, pooling, orchestration
    
- **Modularity & Scalability**: independent scalable layers
    
- **Service Delivery Models**: enables IaaS, PaaS, SaaS
    
- **Simplified Management**: automated provisioning, scaling, security
    
- **Interoperability**: standard APIs, hybrid cloud compatibility
    

---

Here’s the **keyword extraction** for both topics: **Computing on Demand** and **Information Lifecycle Management (ILM)**, organized by headings and key points.

---

## **Computing on Demand**

**Definition**: Real-time provisioning of computing resources (e.g., CPU, storage, bandwidth) over the internet based on user needs, without upfront investment.

---

### **Key Characteristics**

- **Dynamic Resource Allocation** – provision resources as needed
    
- **Pay-per-use Model** – only pay for what is used
    
- **Elasticity** – auto-scale up or down based on workload
    
- **Self-Service** – users provision via web or API
    
- **Rapid Provisioning** – near-instant access to resources
    

---

### **Benefits for Cloud Users**

|**Benefit**|**Explanation**|
|---|---|
|**Cost Efficiency**|No upfront hardware costs; pay only for usage|
|**Scalability & Flexibility**|Adjust to workload changes dynamically|
|**Improved Resource Utilization**|Reduces waste; better efficiency|
|**Faster Time to Market**|Quick resource setup speeds up app deployment|
|**Focus on Core Business**|Less infrastructure management; more time for core tasks|
|**Global Accessibility**|Access resources anytime, anywhere|
|**Reliability & Availability**|Cloud redundancy ensures uptime|

---

### **Example**

**E-commerce site**:

- Auto-scales during sales
    
- Shrinks resources post-sale
    
- Saves costs and maintains user experience
    

---

## **Information Lifecycle Management (ILM)**

**Definition**: A strategy for managing data from creation to secure disposal, optimizing storage, access, and compliance.

---

### **Phases of the Information Lifecycle**

1. **Creation / Capture**
    
    - Data generation from users, sensors, or apps
        
2. **Storage**
    
    - Data stored based on frequency and performance needs
        
    - Examples: hot vs. cold storage
        
3. **Usage**
    
    - Data accessed for operations, decision-making
        
4. **Retention**
    
    - Keep data per legal/business rules
        
5. **Archiving**
    
    - Infrequently accessed data stored long-term (e.g., for compliance)
        
6. **Deletion / Disposal**
    
    - Secure destruction of obsolete or redundant data
        

---

### **Importance in Cloud Storage**

- Efficient data handling
    
- Cost-optimized storage allocation
    
- Data lifecycle control
    
- Compliance with data regulations
    
- Enhances data governance and security
    

---

