Define  
  
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
Adding more machines to handle more load.  
  
## B) CORE AZURE STRUCTURE   
  
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
  
###    
### What is a VNet?  
 A Virtual Network (VNet) is a logically isolated network in Azure where you can deploy your Azure resources like VMs, databases, and web apps. It’s like your own private network in the cloud.  
  
### Purpose:  
* Provides isolation and segmentation.  
* Enables secure communication between Azure resources.  
* Supports hybrid connections with on-premises networks.  
  
### Example:  
You can create a VNet VNet1 with an address space 10.0.0.0/16 to host multiple VMs and Azure services that need to communicate privately.  
  
### What are Subnets, and Why do we need them?  
 A Subnet is a range of IP addresses within a VNet. It helps divide the network into smaller, manageable segments.  
  
### Purpose  
* Organizes resources logically.  
* Implements security boundaries with NSGs.  
* Efficient IP address management.  
  
### Example  
* In VNet1 (10.0.0.0/16)  
* Subnet1: 10.0.1.0/24 for web servers  
* Subnet2: 10.0.2.0/24 for database servers  
  
### What is Network Security Group (NSG)? When do you use it?  
 A Network Security Group (NSG) is a firewall that controls inbound and outbound traffic to resources in a subnet or network interface.  
  
### Purpose  
* Restricts unauthorized access.  
* Applies rules at subnet or VM level.  
  
### When to use NSG:  
* When you want to allow only specific traffic (like HTTP/HTTPS to web servers).  
* To block unwanted inbound or outbound connections.  
  
### Example  
- NSG WebNSG allows inbound 80/443 and denies all other inbound traffic for a web server subnet.  
  
### What is Application Security Group (ASG)? When do you prefer ASG?  
 An Application Security Group (ASG) allows grouping of VMs with similar workloads to simplify NSG rules.  
  
### Purpose  
* Makes NSG rules dynamic and easier to manage.  
* Allows you to apply security policies based on application role rather than IP addresses.  
  
### When to use ASG  
* In large deployments where VMs frequently scale or change.  
* When you want rules like "allow traffic from Web-ASG to DB-ASG".  
  
### Example  
* Web-ASG → all web servers  
* DB-ASG → all database servers NSG rule: Allow traffic from Web-ASG to DB-ASG on port 1433.  
  
### What is VNet Peering?  
VNet Peering connects two VNets privately in Azure, allowing resources in each VNet to communicate without using public IPs.  
  
### Purpose  
* Enables seamless cross-VNet communication.  
* Low latency, high bandwidth connection.  
  
### Example  
- VNet VNet1 (10.0.0.0/16) peered with VNet2 (10.1.0.0/16) allows a VM in VNet1 to access a database in VNet2 privately.  
  
### What is Public IP?  
 A **Public IP** is an IP address accessible from the internet.  
  
### Purpose  
* Makes Azure resources (VMs, Load Balancers, etc.) reachable from outside.  
  
### Example  
- A web server VM with public IP 52.172.12.34 can be accessed from a browser.  
  
### What is Private IP?  
 A Private IP is an IP address used for internal communication within a VNet or between VNets.  
  
### Purpose  
* Ensures internal resources communicate privately.  
* Not accessible directly from the internet.  
  
### Example  
- VM1 in Subnet1 has private IP 10.0.1.4 and VM2 in the same VNet can access it via this IP.  
  
### What are Outbound Rules?  
 Outbound rules define how traffic leaves a resource, subnet, or network interface to external destinations.  
  
### Purpose:  
* Control which destinations a VM or subnet can connect to.  
* Implement security for outbound traffic.  
  
### Example:  
* NSG outbound rule: Allow traffic from Subnet1 to 0.0.0.0/0 on port 443 (HTTPS).  
* Restrict all other outbound traffic.  
  
### Bastion 
Azure Bastion is a fully managed service that provides secure and seamless RDP/SSH connectivity to virtual machines directly through the Azure portal without exposing public IP addresses.  
  
### Purpose:  
* Securely access VMs without exposing them to the internet.  
* Protect against brute-force attacks and reduce the risk of public exposure.  
* Simplifies connectivity management since no VPN or public IP is needed.  
  
### Example:  
* VM WebServer01 has only a private IP 10.0.1.5.  
* Using Azure Bastion, you can connect to this VM from your browser via the Azure portal without assigning a public IP to the VM.  
  
### Key Point  
- Bastion acts like a **jump server** but fully managed and more secure.  
  
### NAT Gateway  
 Azure NAT (Network Address Translation) Gateway is a service that provides outbound internet connectivity for resources in a VNet or subnet while keeping them private.  
  
### Purpose  
* Provides a **static public IP** for outbound traffic from private VMs.  
* Enables secure, consistent outbound connections without exposing VMs with public IPs.  
* Handles large-scale outbound connections efficiently.  
  
### Example  
* VMs in Subnet1 (private IPs 10.0.1.4 - 10.0.1.20) need to download updates from the internet.  
* NAT Gateway assigns a public IP 52.174.56.10 for all outbound traffic.  
* All VMs use this single public IP for outbound, but remain unreachable from the internet.  
  
### Key Point  
- NAT Gateway is for **outbound-only connectivity**, while Bastion is for **inbound secure access**.  
  
### Azure Pricing Calculator  
 The Azure Pricing Calculator is a web-based tool provided by Microsoft Azure that helps estimate the cost of using Azure services based on your specific configurations and usage patterns. It allows you to plan budgets before deploying resources.  
  
### Real-Time Purpose  
* Helps organizations **estimate cloud costs** before deployment.  
* Allows comparison between different service configurations (e.g., VM sizes, storage types).  
* Helps in **budgeting and cost optimization** by simulating real-time usage scenarios.  
* Provides detailed cost breakdowns including region-specific pricing, reserved instances, and storage tiers.  
  
### Example  
* You plan to deploy:  
    * 2 Standard DS3 v2 VMs for 1 month  
    * 500 GB of Standard SSD Storage  
    * Azure SQL Database for 1 year  
* Using Azure Pricing Calculator, you select each service, configure specs, and it shows the **estimated monthly cost** (e.g., $450/month).  
  
### Key Points  
* It is **free to use** and does **not require Azure subscription**.  
* Helps **plan and optimize cloud expenses** before deploying resources.  
* Can export the estimate as **Excel or PDF** for budget approvals.   
### What is ExpressRoute?  
Azure ExpressRoute is a service that provides a private, dedicated, high-bandwidth connection between your on-premises data center and Azure—not over the public internet.  
  
### When do we use ExpressRoute?  
  
We use ExpressRoute when we need:  
* **Private and secure connectivity** (avoiding internet).  
* **High reliability** and **low latency** for mission-critical systems.  
* Large data transfers between on-prem and Azure.  
* Compliance requirements that restrict internet-based connections.  
  
### Example:  
* A bank wants to connect its on-prem data center to Azure with a private 10 Gbps connection for hosting core banking applications. They use ExpressRoute for secure and predictable performance.   
### What is VPN Gateway?  
  
Azure VPN Gateway is a networking service that connects your on-premises network to Azure using encrypted tunnels over the public internet (IPsec/IKE VPN).  
  
### When do we use VPN Gateway?  
We typically use it when:  
* A simple and **cost-effective hybrid connection** is needed.  
* Internet-based secure connectivity is acceptable.  
* ExpressRoute is not required or too expensive.  
* You need site-to-site, point-to-site, or VNet-to-VNet connections.  
  
### Example  
A small company wants to extend its on-prem environment to Azure for hosting test servers. They set up a **Site-to-Site VPN Gateway** to create a secure encrypted tunnel to Azure.  
  
### What is Azure Arc?  
Azure Arc is a service that extends Azure management and governance capabilities to on-premises servers, virtual machines, Kubernetes clusters, and other clouds (AWS, GCP).  
  
### When do we use Azure Arc?  
Use Azure Arc when you need to:  
* Manage on-prem, multi-cloud, and edge servers **from Azure Portal**.  
* Apply **Azure Policies**, **RBAC**, **monitoring**, and **security controls** to non-Azure resources.  
* Use **Azure services** like Azure SQL Managed Instance or Kubernetes management on your own hardware.  
* Maintain a **single control plane** for hybrid or multi-cloud environments.  
  
### Example:  
A company runs servers across AWS, on-prem VMware, and Azure. They use **Azure Arc** to:  
* View all these servers in Azure Portal  
* Apply Azure Policy  
* Monitor them using Azure Monitor  
* Use Azure Defender for security  
  
  
  
  
##    
  
