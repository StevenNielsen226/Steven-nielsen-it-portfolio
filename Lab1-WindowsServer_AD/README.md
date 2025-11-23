# Lab 1 – Active Directory Domain Deployment

**Goal:** Deploy a new Active Directory forest and domain from scratch, design a basic OU structure, and provision users and security groups.

---

## Lab Overview

In this lab I:

- Installed the **Active Directory Domain Services (AD DS)** role on Windows Server.
- Promoted the server to a **domain controller** for the new domain `lab.local`.
- Designed and created an **OU structure** for HR, IT, Sales, and Temp users.
- Created **security groups** and **user accounts** for each department.
- Verified group membership and domain health.

This lab demonstrates skills in **Windows Server administration, AD DS, OU design, and user/group management.**

---

## Environment

- **Domain Controller:** Windows Server 2022 Standard Evaluation  
- **Domain Name:** `lab.local`  
- **Management Tools:** Server Manager, Active Directory Users and Computers (ADUC)  
- **Client OS (for future labs):** Windows 10/11 domain-joined workstation

---

## Topology (Logical)

- **Forest:** `lab.local`
- **Domain:** `lab.local`
- **Organizational Units:**
  - `HR`
  - `IT`
  - `Sales`
  - `Temp`
- **Groups:**
  - `HR Group` (Security group)
  - `IT` (Security group)
- **Sample Users:**
  - `HR User1`, `HR User2`
  - `IT Admin`, `IT Admin2`

---

## Step 1 – Install AD DS Role

1. Open **Server Manager** → **Add roles and features**.
2. Select the local server as the destination.
3. On **Server Roles**, check **Active Directory Domain Services**.
4. Accept required features and complete the wizard.

**Screenshots**

- Role/feature selection  
  ![Select AD DS Role](.images/ad-install-role-selection.png)

- Required management tools  
  ![Add Features for AD DS](.images/ad-install-features.png)

- Destination server selection  
  ![Select Destination Server](.images/ad-install-server-selection.png)

---

## Step 2 – Promote the Server to a Domain Controller

1. In **Server Manager**, click the flag notification and choose  
   **Promote this server to a domain controller**.
2. Select **Add a new forest** and set the root domain name to `lab.local`.

   ![Deployment Configuration](.images/ad-deployment-configuration.png)

3. On **Domain Controller Options**, keep defaults:
   - Forest functional level: *Windows Server 2016*
   - Domain functional level: *Windows Server 2016*
   - DNS server + Global Catalog checked
   - Set the **DSRM password**.

   ![Domain Controller Options](.images/ad-domain-controller-options.png)

4. Continue through the wizard and review the **Prerequisites Check**.
5. Once all checks pass, start the installation and allow the server to reboot.

   ![Prerequisites Check](.images/ad-prereq-check.png)

---

## Step 3 – Design OU Structure

1. Open **Active Directory Users and Computers** (ADUC).
2. Right-click the domain `lab.local` → **New → Organizational Unit**.
3. Create the following OUs:
   - `HR`
   - `IT`
   - `Sales`
   - `Temp`

**Screenshots**

- Final OU structure  
  ![OU Structure](.images/aduc-ou-structure.png)

- Alternate OU view  
  ![OU Structure (Alternative View)](.images/aduc-ou-alt.png)

---

## Step 4 – Create Security Groups

1. In ADUC, right-click the **HR** OU → **New → Group**.
2. Create `HR Group` as a **Security** group (Global scope).
3. Repeat for the **IT** OU, creating the `IT` security group.

**Screenshots**

- HR security group in HR OU  
  ![HR Group](.images/aduc-hr-group.png)

---

## Step 5 – Create Users and Assign to Groups

1. In the **HR** OU:
   - Right-click **HR** → **New → User**.
   - Create `HR User1` and `HR User2`.
2. In the **IT** OU:
   - Create `IT Admin` and `IT Admin2`.

3. Open **HR Group Properties → Members**.
4. Add `HR User1` and `HR User2` as group members.
5. For the **IT** group, add `IT Admin` and `IT Admin2`.

**Screenshots**

- HR users in HR OU  
  ![HR Users](.images/aduc-hr-users.png)

- HR Group membership  
  ![HR Group Members](..images/aduc-hr-group-members.png)

- IT users and group in IT OU  
  ![IT Admin & Group](..images/aduc-it-group-users.png)

---

## Verification

- **Domain:** `lab.local` successfully created and domain controller is operational.
- **OUs:** HR, IT, Sales, and Temp exist under `lab.local`.
- **Groups:** `HR Group` and `IT` created as security groups.
- **Users:** HR and IT users created in the correct OUs.
- **Membership:** HR users are members of `HR Group`; IT admins are members of `IT` group.

---

## Lab Artifacts

- **Lab Report PDF:** [`lab1-report.pdf`](lab1-report.pdf)  
  Contains the full step-by-step narrative of this lab, with screenshots and commentary.

---

## Skills Demonstrated

- Windows Server 2022 installation & role configuration  
- Active Directory Domain Services deployment  
- DNS integration during domain controller promotion  
- Organizational Unit design for business departments  
- User and security group provisioning  
- Basic identity and access management planning
