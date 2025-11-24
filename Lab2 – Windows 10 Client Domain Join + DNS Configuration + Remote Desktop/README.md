# Lab 2 – Windows 10 Domain Client, DNS, and Remote Desktop

**Server VM:** `Server-2022-DC-Portfolio`  
**Client VM:** `Win10-Client`  
**Domain:** `lab.local`

This lab builds on **Lab 1**. You already have a Windows Server 2022 domain controller at `10.0.0.124`.  
In this lab you:

- Build a Windows 10 client VM  
- Join it to the `lab.local` domain  
- Point the client DNS to the domain controller  
- Verify name resolution and connectivity  
- Enable Remote Desktop and test an RDP session

All screenshots for this lab are stored in:  
`Lab2-DNS_DHCP_GPO/Images`

---

## 1. Create the Windows 10 Client VM

1. In **VirtualBox**, create a new VM named **Win10-Client** (50 GB disk, 4 GB RAM).
2. Attach the Windows 10 ISO to the VM.

   ![Windows Setup language screen](./Images/Lab2_ClientSetup_03_WindowsSetup_LanguageScreen.png)

3. Install Windows 10 with default options.
4. After installation, sign in with the **localadmin** account and verify the desktop loads.

   ![Client desktop after install](./Images/Lab2_ClientSetup_08_DesktopLoaded.png)

5. Confirm the virtual disk layout looks correct in VirtualBox.

   ![VirtualBox storage layout](./Images/Lab2_ClientSetup_StorageLayout_Correct.png)

---

## 2. Verify Server and Client Network Settings

Before joining the domain, confirm both machines are on the same network and that the server has a stable IP.

1. On the **Server 2022** VM, run:

   ```powershell
   ipconfig
