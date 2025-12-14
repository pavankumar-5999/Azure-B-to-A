# **Day 4 – Azure Compute Services**

# **1. What are Azure Compute Services?**

Azure Compute services provide **on-demand computing resources** such as virtual machines, containers, and serverless platforms to run applications and workloads.

### **Why Compute Services Matter**

* Run applications and services
* Scale workloads based on demand
* Reduce infrastructure management
* Pay only for what you use

---

# **2. Azure Virtual Machines (VMs)**

## **2.1 What is an Azure Virtual Machine?**

An Azure Virtual Machine (VM) is an **Infrastructure as a Service (IaaS)** offering that lets you run a virtualized operating system in the cloud.

You have full control over:

* Operating system
* Software
* Patching
* Configuration

---

## **2.2 Key Features of Azure VMs**

* Supports **Windows and Linux**
* Full administrative access (RDP/SSH)
* Can be scaled vertically (resize VM)
* Can be scaled horizontally (VM Scale Sets)
* Integrates with Availability Sets and Availability Zones

---

## **2.3 Common VM Use Cases**

* Lift-and-shift on-premises workloads
* Hosting enterprise applications
* Running custom software
* Dev/Test environments

---

## **2.4 VM Pricing Model**

* Pay for compute time (per second)
* Additional cost for storage and networking
* Can save costs using:

  * Reserved Instances
  * Azure Hybrid Benefit

---

# **3. Azure App Service**

## **3.1 What is Azure App Service?**

Azure App Service is a **Platform as a Service (PaaS)** offering for hosting web applications, REST APIs, and mobile backends.

Azure manages:

* Operating system
* Patching
* Scaling
* Infrastructure

You focus on:

* Application code

---

## **3.2 Supported Application Types**

* Web Apps (HTML, Java, .NET, Node.js, Python, PHP)
* REST APIs
* Mobile backend services

---

## **3.3 Key Features of App Service**

* Built-in auto-scaling
* High availability
* CI/CD integration (GitHub, Azure DevOps)
* Custom domains and SSL
* Deployment slots (staging, production)

---

## **3.4 When to Use App Service**

* Hosting web applications
* When you don’t want to manage servers
* Rapid application development

---

# **4. Azure Functions**

## **4.1 What is Azure Functions?**

Azure Functions is a **serverless compute service** that allows you to run small pieces of code (functions) in response to events.

You do NOT manage:

* Servers
* Infrastructure
* OS

---

## **4.2 How Azure Functions Work**

Functions are triggered by events such as:

* HTTP requests
* Timer schedules
* Messages from queues
* Blob storage changes

---

## **4.3 Key Benefits of Azure Functions**

* Event-driven execution
* Automatic scaling
* Pay only when code runs
* Ideal for microservices and automation

---

## **4.4 Common Use Cases**

* Data processing
* Automation tasks
* Real-time file processing
* API backends

---

# **5. Azure Kubernetes Service (AKS)**

## **5.1 What is AKS?**

Azure Kubernetes Service (AKS) is a **managed container orchestration service** for deploying, scaling, and managing containerized applications using Kubernetes.

---

## **5.2 Key Features of AKS**

* Managed Kubernetes control plane
* Automatic scaling of nodes and pods
* Integrated security and monitoring
* Supports Docker containers

---

## **5.3 When to Use AKS**

* Running containerized microservices
* Large-scale distributed applications
* When Kubernetes expertise is available

---

# **6. Comparison Table (Exam Focus)**

| Service          | Type       | Best For               | Management Level         |
| ---------------- | ---------- | ---------------------- | ------------------------ |
| Virtual Machines | IaaS       | Full control workloads | Customer manages OS      |
| App Service      | PaaS       | Web & API apps         | Azure manages infra      |
| Azure Functions  | Serverless | Event-driven tasks     | Azure manages everything |
| AKS              | Containers | Microservices at scale | Shared responsibility    |

---

# **7. IaaS vs PaaS vs Serverless (Quick View)**

| Model      | You Manage       | Azure Manages      |
| ---------- | ---------------- | ------------------ |
| IaaS       | OS, apps, data   | Hardware, network  |
| PaaS       | Application code | OS, runtime, infra |
| Serverless | Function code    | Everything else    |

---

# **8. AZ-900 Exam Tips**

* VMs provide the **most control** but require the most management.
* App Service is best for **web apps** without managing servers.
* Azure Functions are **event-driven** and billed per execution.
* AKS is for **container orchestration**, not simple apps.
* Serverless = no infrastructure management.

---

# **9. Interview Questions & Answers**

### **Q1: When would you use a Virtual Machine instead of App Service?**

Use VMs when you need full OS control or to migrate legacy applications.

### **Q2: What is serverless computing?**

Serverless allows you to run code without managing servers and pay only when code executes.

### **Q3: What is the difference between App Service and Azure Functions?**

App Service hosts long-running web apps, while Functions run event-driven code.

### **Q4: What problem does AKS solve?**

AKS simplifies deployment and management of containerized applications using Kubernetes.

---

# **10. TL;DR (Quick Revision)**

* Azure VMs = IaaS with full control
* App Service = PaaS for web apps
* Azure Functions = Serverless, event-based
* AKS = Managed Kubernetes for containers
* Choose service based on control vs management needs

---
