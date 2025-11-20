# Steven Nielsen – IT Support & Systems Administration Portfolio

**IT Support Technician | WGU BSIT (Accelerated) | Windows • AD • Networking • Virtualization • Cloud Identity**

Welcome to my hands-on IT portfolio.  
These labs demonstrate real-world skills in Windows Server, Active Directory, networking, VPN, ticketing, and cloud identity that I use to transition into full-time IT Support / Junior SysAdmin roles.

---

## 🔧 Lab 1 – Windows Server 2019 + Active Directory Domain Deployment

**Goal:** Deploy a Windows Server 2019 VM, promote it to a domain controller, and build a working AD environment.

**Skills:**  
Windows Server • Active Directory • DNS • Virtualization • User & OU management

**Highlights:**

- Created a VirtualBox VM (`DC01`) with Windows Server 2019.
- Configured static IP and DNS to prepare for domain services.
- Installed **AD DS** and **DNS**, created a new forest `lab.local`.
- Built OUs for **IT, HR, Finance, StandardUsers**.
- Created multiple test users and a delegated admin account.
- Joined a Windows 10 client to the domain and verified login.

📄 **Documentation:** `Lab1-WindowsServer_AD/Lab1-AD-Lab-Writeup.pdf`  
📸 **Screenshots:** `Lab1-WindowsServer_AD/screenshots/`

---

## 🌐 Lab 2 – DNS, DHCP & Group Policy Management

**Goal:** Configure DHCP and DNS and apply Group Policy settings for domain clients.

**Skills:**  
DHCP • DNS • Group Policy • Network troubleshooting

**Highlights:**

- Configured a DHCP scope for domain clients (IP, gateway, DNS).
- Verified DHCP leases and name resolution from a Windows 10 VM.
- Created a GPO enforcing password complexity and screen-lock timeout.
- Simulated DNS/DHCP issues (wrong DNS, duplicate IP) and resolved them.
- Documented troubleshooting steps and final configuration.

📄 `Lab2-DNS_DHCP_GPO/Lab2-DNS-DHCP-GPO-Writeup.pdf`  

---

## 🎫 Lab 3 – IT Ticketing & Troubleshooting Workflow

**Goal:** Practice structured troubleshooting and documentation using a ticketing system.

**Skills:**  
Ticketing systems • Documentation • Customer communication • Root cause analysis

**Highlights:**

- Created a small help desk project in **Jira / Freshdesk**.
- Logged sample tickets:
  - *User cannot log in – account locked*
  - *VPN disconnects intermittently*
  - *Computer is slow*
- Wrote clear, step-by-step resolution notes for each incident.
- Used priorities, categories, and status transitions like a real help desk.
- Exported tickets and notes as portfolio evidence.

📄 `Lab3-Ticketing/Lab3-Ticketing-Portfolio.pdf`  

---

## 🔐 Lab 4 – VPN & Network Connectivity Troubleshooting

**Goal:** Configure a simple VPN and diagnose network connectivity problems.

**Skills:**  
VPN • Routing • DNS • Firewall rules • Network troubleshooting

**Highlights:**

- Deployed an **OpenVPN / WireGuard** server in the lab environment.
- Installed VPN client on a Windows 10 VM and verified access to internal resources.
- Broke connectivity on purpose (ports blocked, DNS misconfigured, routes removed).
- Used `ipconfig`, `ping`, `tracert`, and firewall checks to isolate issues.
- Documented each failure scenario and fix.

📄 `Lab4-VPN_Network/Lab4-VPN-Network-Lab-Writeup.pdf`  

---

## ☁️ Lab 5 – SaaS / Cloud Identity & MFA Support (Microsoft 365)

**Goal:** Show cloud identity administration and user support around MFA and access.

**Skills:**  
Entra ID / Azure AD • MFA • Conditional Access • User account management • SaaS troubleshooting

**Highlights:**

- Provisioned a **Microsoft 365 Developer** tenant and created test accounts.
- Enabled **MFA** and Conditional Access policies for selected users.
- Simulated common issues: lost MFA device, disabled account, bad password.
- Resolved issues via the admin center, including password resets and MFA resets.
- Used sign-in logs and audit logs to confirm behavior and document root causes.

📄 `Lab5-CloudIdentity_MFA/Lab5-CloudIdentity-MFA-Writeup.pdf`  

---

## 📥 Downloadable PDF Portfolio

For a recruiter-friendly overview of these labs, download:

**[Steven Nielsen – IT Portfolio (PDF)](IT_Portfolio_Full.pdf)**

---

## 📫 Contact

- **Location:** Vancouver, WA (open to Portland metro & remote)
- **Email:** steven.nielsen226@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/steven-nielsen-33806919b/

If you’d like more detail on any lab or want to discuss how this experience maps to your environment, I’d be happy to walk through it live.
