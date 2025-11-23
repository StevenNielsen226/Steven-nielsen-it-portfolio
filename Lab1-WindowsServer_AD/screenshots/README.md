# Lab 1 – Active Directory Domain Controller Deployment (Windows Server 2022)

## 🎯 Overview
This lab demonstrates the deployment of a fully functional **Active Directory Domain Services (AD DS)** environment using **Windows Server 2022**. Tasks include:

- Installing AD DS
- Promoting the server to a Domain Controller
- Configuring DNS
- Creating Organizational Units (OUs)
- Creating Users & Security Groups
- Assigning group membership
- Verifying domain structure

Domain used in this lab: **lab.local**

---

# 🖥️ Step 1 — Install Active Directory Domain Services (AD DS)

### 📌 Server Selection
Choosing the server from the pool to install AD DS.

![Server Selection](images/ad-install-server-selection.png)

---

### 📌 Select AD DS Role

![Select AD DS Role](images/ad-install-role-selection.png)

---

### 📌 Add Required Features
Windows automatically selects additional tools needed for AD DS (RSAT, GPMC, etc.)

![Required Features](images/ad-install-features.png)

---

# 🏰 Step 2 — Promote Server to Domain Controller

### 📌 Deployment Configuration
Creating a **new forest** with domain: `lab.local`

![Deployment Configuration](images/ad-deployment-configuration.png)

---

### 📌 Domain Controller Options
Setting DSRM password, configuring DNS, GC, and forest functional level.

![Domain Controller Options](images/ad-domain-controller-options.png)

---

### 📌 Prerequisite Check
All checks passed → Ready to install.

![Prerequisite Check](images/ad-prereq-check.png)

---

# 🗂️ Step 3 — Create Organizational Units (OUs)

The following OUs were created:

- **HR**
- **IT**
- **Sales**
- **Temp**

![OU Structure](images/aduc-ou-structure.png)

---

# 👥 Step 4 — Create Security Groups & Users

### 📌 HR Department
- HR Group
- HR User1
- HR User2

![HR Users](images/aduc-hr-users.png)

![HR Group](images/aduc-hr-group.png)

---

### 📌 IT Department
- IT Group
- IT Admin
- IT Admin2

![IT Group](images/aduc-it-group-users.png)

---

# 🔐 Step 5 — Verify Group Membership

Example: HR Group containing HR User1 and HR User2.

![HR Group Members](images/aduc-hr-group-members.png)

---

# ✅ Lab 1 Complete

This lab demonstrates core enterprise sysadmin skills:

- Server role installation  
- DNS & domain configuration  
- AD forest deployment  
- OU planning  
- User & group provisioning  
- Administrative structure design  

This environment will be used in later labs (Group Policy, DNS/DHCP, VPN, Cloud Identity).

---
