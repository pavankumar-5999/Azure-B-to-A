# **Day 6 – Azure Networking (VNet, VPN, ExpressRoute, Load Balancer, Application Gateway)**

---

# **1. Introduction to Azure Networking**

Azure networking enables **secure communication** between Azure resources, on-premises networks, and the internet.

### **Why Networking Is Important**

* Connect virtual machines and services
* Secure traffic flow
* Enable hybrid cloud scenarios
* Improve availability and performance

---

# **2. Azure Virtual Network (VNet)**

## **2.1 What is a Virtual Network (VNet)?**

An Azure Virtual Network (VNet) is a **private network** in Azure that allows Azure resources to communicate securely with each other and with external networks.

---

## **2.2 Key Components of VNet**

* **Address Space**: Private IP range (CIDR notation, e.g., 10.0.0.0/16)
* **Subnets**: Logical divisions within a VNet
* **Network Interfaces (NICs)**: Connect VMs to the VNet
* **Network Security Groups (NSGs)**: Control inbound/outbound traffic

---

## **2.3 VNet Use Cases**

* Isolate applications
* Host VMs securely
* Enable communication between Azure services

---

# **3. Azure VPN Gateway**

## **3.1 What is Azure VPN Gateway?**

Azure VPN Gateway allows **secure encrypted connectivity** between Azure VNets and:

* On-premises networks
* Other Azure VNets

---

## **3.2 Types of VPN Connections**

* **Site-to-Site (S2S)**: On-premises network ↔ Azure VNet
* **Point-to-Site (P2S)**: Individual client ↔ Azure VNet
* **VNet-to-VNet**: Azure VNet ↔ Azure VNet

---

## **3.3 When to Use VPN Gateway**

* Hybrid connectivity
* Low to moderate bandwidth needs
* Encrypted communication over the internet

---

# **4. Azure ExpressRoute**

## **4.1 What is ExpressRoute?**

Azure ExpressRoute provides a **private, dedicated connection** between on-premises networks and Azure, bypassing the public internet.

---

## **4.2 ExpressRoute vs VPN Gateway**

| Feature         | VPN Gateway   | ExpressRoute      |
| --------------- | ------------- | ----------------- |
| Connection Type | Over Internet | Private Dedicated |
| Security        | Encrypted     | Private & Secure  |
| Bandwidth       | Lower         | Higher            |
| Latency         | Higher        | Lower             |
| Cost            | Lower         | Higher            |

---

## **4.3 When to Use ExpressRoute**

* Mission-critical workloads
* High bandwidth requirements
* Low latency applications

---

# **5. Azure Load Balancer**

## **5.1 What is Azure Load Balancer?**

Azure Load Balancer distributes incoming network traffic across multiple backend resources, such as VMs, to ensure **high availability and reliability**.

---

## **5.2 Types of Azure Load Balancer**

* **Public Load Balancer**: Internet-facing traffic
* **Internal Load Balancer**: Traffic within Azure VNet

---

## **5.3 Key Features**

* Layer 4 (TCP/UDP) load balancing
* Health probes
* High availability

---

# **6. Azure Application Gateway**

## **6.1 What is Azure Application Gateway?**

Azure Application Gateway is a **Layer 7 (HTTP/HTTPS) load balancer** designed for web applications.

---

## **6.2 Key Features**

* URL-based routing
* SSL termination
* Web Application Firewall (WAF)
* Cookie-based session affinity

---

## **6.3 Application Gateway vs Load Balancer**

| Feature   | Load Balancer   | Application Gateway |
| --------- | --------------- | ------------------- |
| OSI Layer | Layer 4         | Layer 7             |
| Protocols | TCP/UDP         | HTTP/HTTPS          |
| Use Case  | General traffic | Web applications    |
| WAF       | No              | Yes                 |

---

# **Quick reference**

* VNet = private network in Azure
* VPN Gateway = encrypted internet-based connectivity
* ExpressRoute = private, dedicated connection
* Load Balancer = Layer 4 traffic distribution
* Application Gateway = Layer 7 web traffic + WAF

---

# **8. Interview Questions & Answers**

### **Q1: What is the difference between VNet and VPN Gateway?**

A VNet is a private network; VPN Gateway provides connectivity to it.

### **Q2: When would you use ExpressRoute instead of VPN?**

Use ExpressRoute for high bandwidth, low latency, and mission-critical workloads.

### **Q3: Difference between Load Balancer and Application Gateway?**

Load Balancer works at Layer 4; Application Gateway works at Layer 7 with WAF.

---

# **9. TL;DR (Quick Revision)**

* **VNet** = private Azure network
* **VPN Gateway** = encrypted internet connection
* **ExpressRoute** = private dedicated connection
* **Load Balancer** = Layer 4 traffic distribution
* **Application Gateway** = Layer 7 web routing + WAF

---
