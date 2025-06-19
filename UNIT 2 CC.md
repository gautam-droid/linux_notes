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
