Definitions  
  
##  A) CLOUD FUNDAMENTALS   
### 1. Cloud Computing  
 Delivery of computing services (VMs, storage, databases, networking) over the internet.  
### 2. Region  
A geographic area where Azure has multiple data centers.  
### 3. Datacenter  
A physical building filled with servers and networking equipment.  
### 4. Availability Zone  
Physically separate data centers within a region — protects against datacenter failures.  
### 5. Region Pair  
Two Azure regions linked together for disaster recovery and automatic redundancy.  
### 6. Scalability  
Ability to increase or decrease resources based on demand.  
### 7. Elasticity  
Automatic scaling up or down based on workload needs.  
### 8. Agility  
Ability to quickly build, deploy, and manage resources without long delays.  
### 9. Vertical Scaling  
Adding more power (CPU/RAM) to an existing machine.  
### 10. Horizontal Scaling  
## Adding more machines to handle more load.  B) CORE AZURE STRUCTURE (Start With These)  
  
### 11. Resource  
Anything you create in Azure — like a VM, storage account, network, or database.  
### 12. Resource Group  
A container that stores related Azure resources so you can manage them together.  
### 13. Subscription  
A billing and access boundary — all resource usage inside a subscription is billed together.  
### 14. Management Group  
A higher-level container that groups multiple subscriptions for centralised governance.  
### 15. Azure Resource Manager (ARM)  
The engine that creates, updates, and deletes Azure resources using templates, portal, CLI, or APIs.  
  
## C) CLOUD MODELS  
  
### 16. Public Cloud  
Cloud services available for anyone to use, owned and managed by the provider (Azure, AWS).  
### 17. Private Cloud  
Cloud infrastructure used only by one organisation, hosted in its own datacenter.  
### 18. Hybrid Cloud  
Combination of public + private cloud working together.  
##  D) CLOUD SERVICE TYPES  
  
### 19. IaaS (Infrastructure as a Service)  
You manage OS, apps, and data; provider manages hardware. Example: Virtual Machines.  
### 20. PaaS (Platform as a Service)  
Provider manages OS and runtime; you manage only apps and data. Example: App Service, Azure SQL.  
### 21. SaaS (Software as a Service)  
Fully ready-to-use applications delivered over the internet. Example: Office 365.  
  
## E) AVAILABILITY & RELIABILITY CONCEPTS  
  
### 22. Fault Domain  
Group of hardware that can fail together. Azure spreads VMs across fault domains for protection.  
### 23. Update Domain  
Group of resources updated together during maintenance to avoid simultaneous reboots.  
### 24. Availability Set  
A logical grouping to distribute VMs across fault + update domains.  
##  F) CORE AZURE SERVICES   
  
### 25. Virtual Machine (VM)  
A cloud-based computer you can configure with your own OS, software, and settings.  
### 26. Virtual Network (VNet)  
A private network in Azure where your resources (VMs, databases) securely communicate.  
### 27. Subnet  
A smaller segment inside a VNet used for organizing and controlling traffic.  
### 28. Network Security Group (NSG)  
A firewall that controls inbound and outbound traffic for VMs and subnets.  
### 29. Azure Storage Account  
A service to store files, blobs, disks, tables, and backups.  
### 30. Azure App Service  
A managed platform for hosting web applications and APIs without managing servers.  
### 31. Azure Functions  
A serverless compute service where you run small pieces of code on demand.  
### 32. Azure SQL Database  
A fully managed SQL Server database in the cloud.  
### 33. Azure Cosmos DB  
A globally distributed NoSQL database with fast performance.  
### 34. Azure Load Balancer  
Distributes traffic across multiple VMs to improve performance and availability.  
### 35. Virtual Machine Scale Sets (VMSS)  
Automatically increases or decreases VM instances based on load.  
### 36. Azure Key Vault  
Stores secrets, passwords, certificates, and encryption keys securely.  
### 37. Azure Monitor  
Tracks performance, logs, and alerts for all Azure resources.  
### 38. Azure Active Directory (Azure AD) - Entra ID  
Cloud identity service used for user login, authentication, and access control.  
  
  
  
