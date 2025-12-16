# **Day 7 – Identity, Security & Governance**

This document covers **Azure identity, access, and security services** for:

---

# **1. Azure Active Directory (Azure AD / Microsoft Entra ID)**

## **What is Azure AD?**

Azure AD is a **cloud-based identity and access management (IAM)** service.

### **Key Functions**

* User authentication
* Single Sign-On (SSO)
* Identity management for cloud apps

### **Used For**

* Logging into Azure Portal
* Accessing Microsoft 365
* Managing users, groups, devices

---

# **2. Role-Based Access Control (RBAC)**

## **What is RBAC?**

RBAC controls **who can do what** on Azure resources.

### **RBAC Components**

* **Security Principal** – user, group, or app
* **Role Definition** – permissions (Reader, Contributor, Owner)
* **Scope** – subscription, resource group, resource

### **Key Principle**

* Least privilege access
---

# **3. Azure Key Vault**

## **What is Key Vault?**

Secure storage for **secrets, keys, and certificates**.

### **Stores**

* Passwords
* API keys
* Certificates

### **Benefits**

* Centralized secret management
* Secure access via Azure AD

---

# **4. Microsoft Defender for Cloud**

## **What is Defender for Cloud?**

Security posture management and threat protection service.

### **Capabilities**

* Security recommendations
* Threat detection
* Compliance monitoring

---

# **5. Zero Trust Model**

### **Core Principles**

* Never trust, always verify
* Least privilege access
* Assume breach

---

# **6. Azure Policy**

## **What is Azure Policy?**

Service to **enforce organizational standards**.

### **Examples**

* Enforce allowed VM sizes
* Require tags
* Block public IP creation

---

# **Exam TL;DR**

* Azure AD = identity
* RBAC = permissions
* Key Vault = secrets
* Defender = security posture
* Policy = governance
# **Interview Questions & Answers (Day 7)**

### **Q1: What is Azure Active Directory?**

Azure AD is a cloud-based identity and access management service used for authentication, authorization, and Single Sign-On.

### **Q2: What is the difference between RBAC and Azure Policy?**

RBAC controls who can access Azure resources, while Azure Policy controls what configurations are allowed.

### **Q3: Why do we use Azure Key Vault?**

Azure Key Vault securely stores secrets, keys, and certificates and controls access using Azure AD.

### **Q4: What is Microsoft Defender for Cloud?**

It helps improve security posture, provides recommendations, and protects against threats.

### **Q5: Explain Zero Trust in simple terms.**

Never trust by default, always verify identity, and grant least-privilege access.

### **Q6: What does Azure Policy do?**

Azure Policy enforces organizational standards and compliance rules.

---

# **Quick Reference (Day 7)**

* Azure AD → Identity & authentication
* RBAC → Permissions & access control
* Key Vault → Secrets & certificates
* Defender for Cloud → Security posture & threats
* Zero Trust → Verify always, least privilege
* Azure Policy → Governance & compliance
---
