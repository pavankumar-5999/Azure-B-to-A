# Day 1 – Cloud Basics, Benefits, Shared Responsibility

## 1. What is Cloud Computing?
Cloud computing delivers computing services—servers, storage, networking, databases, analytics, and software—over the internet.

### Key Points
- Access on-demand resources without managing hardware
- Reduces CAPEX, increases OPEX flexibility
- Pay-as-you-go pricing model

### Example
Deploy a website using **Azure App Service** instead of buying physical servers.

### Cloud vs On-Premises
| Feature | On-Premises | Cloud |
|--------|-------------|--------|
| Hardware Ownership | Organization | Cloud Provider |
| Upfront Cost | High (CAPEX) | Low (OPEX) |
| Scalability | Limited | Elastic & instant |
| Maintenance | Customer | Provider |

---

## 2. Cloud Service Models

### **A. Infrastructure as a Service (IaaS)**
You manage: OS, applications, data  
Provider manages: hardware, network

**Examples:** Azure VMs, Storage

### **B. Platform as a Service (PaaS)**
You manage: applications, data  
Provider manages: OS, runtime, infrastructure

**Examples:** Azure App Service, Azure SQL Database

### **C. Software as a Service (SaaS)**
Provider manages everything; user consumes the software.

**Examples:** Microsoft 365, Teams, Outlook

### Comparison Table
| Feature | IaaS | PaaS | SaaS |
|--------|------|------|------|
| Infrastructure | Provider | Provider | Provider |
| OS | Customer | Provider | Provider |
| Applications | Customer | Customer | Provider |
| Maintenance | High | Medium | Low |
| Examples | VMs, Storage | App Service, SQL DB | Office 365 |

---

## 3. Cloud Deployment Models
### Public Cloud
- Shared resources
- Examples: Azure, AWS, GCP

### Private Cloud
- Dedicated to one organization

### Hybrid Cloud
- Combines public + private
- Example: On-prem SQL + Azure Backup

### Multi-Cloud
- Using multiple cloud providers

---

## 4. Benefits of Cloud Computing
- **Cost Efficiency:** No upfront hardware, pay-as-you-go
- **Scalability:** Automatic scaling (VM Scale Sets)
- **Global Reach:** Deploy globally
- **High Availability:** SLAs + redundancy
- **Agility:** Quick deployment
- **Security:** Strong compliance
- **Innovation:** AI, ML, analytics

---

## 5. Shared Responsibility Model
Defines what the provider vs. customer manages.

### Responsibility Table
| Responsibility | IaaS | PaaS | SaaS |
|----------------|------|------|------|
| Physical Infrastructure | Provider | Provider | Provider |
| Network & Datacenter Security | Provider | Provider | Provider |
| OS & Patching | Customer | Provider | Provider |
| Applications | Customer | Customer | Provider |
| Data & Access | Customer | Customer | Customer |

### Summary
- **IaaS:** Customer manages the most
- **PaaS:** Customer focuses on apps & data
- **SaaS:** Provider handles almost everything
