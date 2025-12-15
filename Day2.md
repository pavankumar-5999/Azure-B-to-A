# **Day 2 – IaaS, PaaS, SaaS & Public, Private, Hybrid Cloud**
---

# **1. Cloud Service Models (IaaS, PaaS, SaaS)**

Cloud services are divided based on **how much you manage** vs. how much the **cloud provider manages**.

---

## **1.1 IaaS – Infrastructure as a Service**

**Definition:** Cloud provider delivers fundamental infrastructure resources like **virtual machines, storage, networks**, and you manage the OS, applications, and configurations.

### **Key Characteristics**

* Most flexible cloud model
* Full control over OS, middleware, and runtime
* Similar to renting a physical server, but in the cloud

### **Customer Manages:**

* Operating system updates
* Application installation & configuration
* Data & access security

### **Provider Manages:**

* Physical hardware
* Virtualization
* Networking

### **Common Azure IaaS Services:**

* **Azure Virtual Machines**
* **Virtual Networks (VNet)**
* **Azure Storage (Blob, Disk)**
* **Network Security Groups (NSG)**

### **Use Cases:**

* Lift-and-shift migrations
* Running custom applications
* Testing and development environments

---


## **1.2 PaaS – Platform as a Service**

**Definition:** Provider delivers **runtime environment, OS, middleware, and tools**. You only deploy and manage your application.

### **Key Characteristics**

* Developer-focused
* No server management
* Automatic scaling and updates

### **Customer Manages:**

* Application code
* Application data

### **Provider Manages:**

* OS and runtime
* Security patches
* Infrastructure scaling

### **Common Azure PaaS Services:**

* **Azure App Service**
* **Azure Functions** (Serverless)
* **Azure SQL Database** (Managed SQL)
* **Azure Kubernetes Service (AKS)**

### **Use Cases:**

* Web and mobile app hosting
* APIs
* Microservices
* Automated workflows

---

## **1.3 SaaS – Software as a Service**

**Definition:** Fully managed applications delivered over the internet. You only use the software.

### **Key Characteristics**

* No installation
* No maintenance
* Subscription-based

### **Customer Manages:**

* Only data & user access

### **Provider Manages:**

* Applications
* Infrastructure
* Security

### **Common Azure SaaS Examples:**

* **Microsoft 365**
* **Dynamics 365**
* **Power BI**

### **Use Cases:**

* Email
* CRM/ERP systems
* Productivity applications

---

# **2. Public, Private, and Hybrid Cloud**

These describe where infrastructure is hosted and how resources are accessed.

---

## **2.1 Public Cloud**

**Definition:** Cloud resources hosted on shared hardware by a third-party provider like Azure.

### **Key Characteristics**

* Pay-as-you-go
* No hardware maintenance
* High scalability
* Accessible over the internet

### **Examples:**

* Azure
* AWS
* Google Cloud

### **Use Cases:**

* Startups
* Web applications
* Data analytics

---

## **2.2 Private Cloud**

**Definition:** Cloud environment dedicated to a single organization.

### **Key Characteristics**

* Highest control and security
* Can be on-premises or hosted
* Expensive to manage

### **Examples:**

* On-prem VMware cloud
* Azure Stack deployments

### **Use Cases:**

* Large enterprises
* Organizations with strict compliance (banks, government)

---

## **2.3 Hybrid Cloud**

**Definition:** A mix of on-premises infrastructure and public cloud.

### **Key Characteristics**

* Flexibility between on-prem and cloud
* Seamless workload movement
* Cost optimization

### **Examples:**

* On-prem datacenter + Azure

### **Use Cases:**

* Gradual cloud migration
* Backup and disaster recovery
* Legacy apps needing on-prem connectivity

---

# **3. Comparison Tables**

## **3.1 Service Model Comparison**

| Feature     | IaaS      | PaaS            | SaaS               |
| ----------- | --------- | --------------- | ------------------ |
| Control     | High      | Medium          | Low                |
| Cost        | Medium    | Medium-Low      | Low                |
| Maintenance | Customer  | Shared          | Provider           |
| Use Case    | Migration | App development | Productivity tools |

---

## **3.2 Deployment Model Comparison**

| Model   | Who Owns It    | Access           | Cost   | Use Case           |
| ------- | -------------- | ---------------- | ------ | ------------------ |
| Public  | Cloud provider | Public internet  | Low    | Startups, web apps |
| Private | Single org     | Private networks | High   | Banking, security  |
| Hybrid  | Both           | Combined         | Medium | Migration, DR      |

---

# **4. Exam Tips (AZ-900 Focus)**

* **IaaS → You manage OS/applications**
* **PaaS → You manage only application code**
* **SaaS → You manage nothing except data and access**
* Public cloud is **scalable and inexpensive**, private cloud is **secure and expensive**, hybrid is **flexible**.
* PaaS services like Azure App Service reduce management overhead.
* SaaS includes Microsoft 365 and Dynamics 365.

---

# **5. Interview Tips & Answers**

### **Q: What is IaaS?**

IaaS provides virtualized computing resources like VMs and storage. It offers maximum flexibility because you manage the OS and applications.

### **Q: When would you use PaaS?**

Use PaaS when you want to focus on app development without worrying about servers, OS patching, or scaling.

### **Q: Explain SaaS with an example.**

SaaS provides fully managed applications like Outlook (Microsoft 365), where the provider handles everything.

### **Q: What is the difference between public and private cloud?**

Public cloud is shared, cost-effective, and internet-based, while private cloud is dedicated to one org, more secure, and often used for compliance.

### **Q: Why use hybrid cloud?**

Hybrid cloud provides flexibility to keep sensitive data on-prem while using cloud scalability for modern workloads.

---
