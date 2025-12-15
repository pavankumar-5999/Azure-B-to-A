# **Day 5 – Azure Storage Services and Redundancy**

These notes cover **Azure Storage services and data redundancy options** and are designed for:
---

# **1. Introduction to Azure Storage**

Azure Storage provides **durable, highly available, and scalable cloud storage** for a wide variety of data types, including objects, files, disks, and queues.

### **Why Azure Storage Matters**

* Persistent data storage for applications
* Backup and disaster recovery
* Scalable and pay-as-you-go pricing

---

# **2. Core Azure Storage Services**

| Service       | Type            | Description                                      | Use Case                                 |
| ------------- | --------------- | ------------------------------------------------ | ---------------------------------------- |
| Blob Storage  | Object Storage  | Stores unstructured data like text and binary    | Images, videos, logs, backups            |
| File Storage  | File Share      | Fully managed file shares accessible via SMB/NFS | Lift-and-shift legacy apps, shared files |
| Queue Storage | Messaging       | Stores messages for asynchronous communication   | Workflow processing, decoupling apps     |
| Table Storage | NoSQL Key-Value | Stores structured, non-relational data           | IoT telemetry, application metadata      |
| Disk Storage  | Block Storage   | Provides persistent disks for VMs                | VM storage, databases                    |

---

# **3. Azure Storage Redundancy Options**

Redundancy ensures **data durability** by replicating data across multiple locations.

## **3.1 Locally Redundant Storage (LRS)**

* Replicates data **3 times within a single datacenter** in a region
* Protects against **hardware failures** only
* **Cost-effective but less durable** than cross-region options

### **Use Case**

* Non-critical data
* Test and dev environments

<img width="808" height="226" alt="Screenshot 2025-12-15 at 20 35 45" src="https://github.com/user-attachments/assets/8f430383-77ba-4f48-b5ab-a7158dac70a3" />

---

## **3.2 Zone-Redundant Storage (ZRS)**

* Replicates data **synchronously across multiple Availability Zones** within the same region
* Protects against **datacenter failures**
* Higher durability and availability than LRS

### **Use Case**

* Production workloads requiring high availability
* Web applications and critical VMs
<img width="808" height="226" alt="Screenshot 2025-12-15 at 20 35 45" src="https://github.com/user-attachments/assets/0192cb11-6689-4a16-8d2a-58c3a2b27b26" />

---

## **3.3 Geo-Redundant Storage (GRS)**

* Replicates data **to a secondary region hundreds of miles away** in addition to LRS/ZRS in the primary region
* Protects against **regional disasters**
* Data is replicated asynchronously

### **Use Case**

* Business-critical applications
* Disaster recovery solutions
* Regulatory compliance requiring geo-replication

<img width="808" height="226" alt="Screenshot 2025-12-15 at 20 35 45" src="https://github.com/user-attachments/assets/8a6e4081-159d-4ef3-be1f-fec9e4b570f1" />

---

## **3.4 Read-Access Geo-Redundant Storage (RA-GRS)**

* Same as GRS but provides **read access to the secondary region**
* Allows **high availability even during primary region outage**

### **Use Case**

* Applications needing continuous read access during outages
* Global distribution of data for read-heavy apps

---
# **AZ-900 – Geo-Zone-Redundant Storage (GZRS)**

These notes explain **GZRS** in Azure and are useful for AZ-900 exam, interviews, and daily learning.

---

# ** What is GZRS?**

**GZRS (Geo-Zone-Redundant Storage)** combines the benefits of **ZRS (Zone-Redundant Storage)** and **GRS (Geo-Redundant Storage)**. It ensures:

* Data is **replicated across multiple Availability Zones** within the primary region (like ZRS).
* Data is **asynchronously replicated to a secondary region** (like GRS).
* Provides **high durability, high availability, and disaster recovery**.

---

# **2. Key Features**

* Combines **zone-level redundancy** with **geo-replication**.
* Protects against:

  * Datacenter failures in primary region
  * Regional disasters
* Data is **readable only from the primary region** by default.
* Can be paired with **RA-GZRS** for read access from secondary region.

---

# **3. Use Cases**

* Business-critical applications that need **high availability and disaster recovery**.
* Applications that require **zone-level fault tolerance** and **cross-region replication**.
* Compliance scenarios requiring **geographically separate copies** of data.

---

# **4. Comparison with Other Redundancy Options**

| Storage Type | Replication                         | Protection Level                                 |
| ------------ | ----------------------------------- | ------------------------------------------------ |
| LRS          | 3 copies in single datacenter       | Protects against hardware failure only           |
| ZRS          | 3 copies across zones in a region   | Protects against datacenter failure              |
| GRS          | LRS + replicate to secondary region | Protects against regional disaster               |
| **GZRS**     | ZRS + replicate to secondary region | Protects against datacenter & regional disasters |

---

# **5. AZ-900 Exam Tips**

* GZRS = **ZRS + GRS** combination
* Provides **maximum durability** for critical workloads
* Paired with **RA-GZRS** for read access from secondary region
* Choose GZRS when **cost is less critical** than **availability & disaster protection**

---

# **6. TL;DR**

* **GZRS** = Zone-redundant + Geo-redundant storage
* **Protects against datacenter and regional failures**
* Use for **business-critical, high-availability apps**
* Optional: **RA-GZRS** for read access from secondary region

---

<img width="808" height="226" alt="Screenshot 2025-12-15 at 20 35 45" src="https://github.com/user-attachments/assets/f50c77f9-cf76-4255-a038-0df6ce61a5be" />


# **4. Azure Storage Pricing Factors**

* Redundancy type (LRS < ZRS < GRS < RA-GRS)
* Data volume (GB/TB stored)
* Transaction operations (read/write requests)
* Data egress (transfer out of Azure)

---

# **5. Exam Tips (AZ-900 Focus)**

* **LRS** = 3 copies in single datacenter, cheapest
* **ZRS** = 3 copies across zones, high availability
* **GRS** = replicates to secondary region, disaster recovery
* **RA-GRS** = read access to secondary region
* Use **Blob storage** for unstructured data, **File storage** for SMB shares
* Always match storage redundancy to **business criticality and cost**

---

# **6. Interview Questions & Answers**

### **Q1: What is LRS and when would you use it?**

LRS replicates data 3 times within one datacenter. Use it for non-critical, cost-sensitive data.

### **Q2: What’s the difference between ZRS and GRS?**

ZRS replicates within a region across zones; GRS replicates across regions for disaster recovery.

### **Q3: When should you use RA-GRS?**

Use RA-GRS when your app needs continuous read access even if the primary region fails.

### **Q4: Which Azure storage service is best for unstructured data?**

Blob Storage is ideal for images, videos, logs, and backups.

### **Q5: Why is redundancy important in cloud storage?**

It ensures data durability and availability in case of hardware or regional failures.

---

# **7. TL;DR (Quick Revision)**

* **Blob Storage** = unstructured data
* **File Storage** = shared file systems
* **Queue Storage** = messaging
* **Disk Storage** = persistent VM disks
* **LRS** = 3 copies in 1 datacenter
* **ZRS** = across multiple zones in a region
* **GRS** = replicated to another region
* **RA-GRS** = read access from secondary region
* Choose redundancy based on **criticality & cost**

---
