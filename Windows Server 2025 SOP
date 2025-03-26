# Standard operating Procedure
## MITT
130 Henlow Bay, Winnipeg, MB
R3Y 1G4
413 XXX XXXX

#00000001
Written by: Balkaran Singh

Approved by: Filex
Date: 03-26-2025

---

## Purpose
This SOP provides a step-by-step guide for installing and configuring Windows Server 2025.

---

## Application
Applies to system administrators responsible for Windows Server 2025 deployment.

---

## Definitions
- **ISO** – Disk image file format for operating system installation.
- **DHCP** – Dynamic Host Configuration Protocol assigns IP addresses.
- **DNS** – Domain Name System.

---

## Procedure Steps

### **Step 1: Obtain Windows Server 2025 Installation Media**
1. Go to the [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2025) and download the Windows Server 2025 ISO file.  
2. Use a tool like [Rufus](https://rufus.ie/) to create a bootable USB drive from the ISO file.  

---

### **Step 2: Verify System Requirements**
Ensure the server meets the following minimum requirements:

| Component | Requirement |
|-----------|-------------|
| **Processor** | 1.4 GHz 64-bit processor compatible with x64 instruction set |
| **RAM** | 512 MB (2 GB for Server with Desktop Experience) |
| **Disk Space** | 32 GB minimum |
| **Network Adapter** | Ethernet adapter capable of at least gigabit throughput |

[Reference: Microsoft Documentation](https://learn.microsoft.com/en-us/windows-server/get-started/hardware-requirements)  

---

### **Step 3: Install Windows Server 2025**
1. Insert the bootable USB drive into the server.  
2. Restart the server and boot from the USB drive.  
3. Select **language**, **time**, and **keyboard** settings.  
4. Click **Install Now**.  
5. Choose between:  
   - **Server Core** – Minimal interface for better performance.  
   - **Server with Desktop Experience** – Full GUI experience.  
6. Select the installation disk and format it if needed.  
7. Complete the installation and allow the server to restart.  

[Reference: Microsoft Documentation](https://learn.microsoft.com/en-us/windows-server/get-started/install-windows-server)  

---

### **Step 4: Perform Initial Configuration**
1. **Set Administrator Password**  
   - Upon first login, create a strong administrator password.  

2. **Configure Network Settings**  
   - Go to **Settings → Network & Internet → Ethernet**.  
   - Assign a static IP address, subnet mask, gateway, and DNS.  

3. **Rename the Server**  
   - Go to **Control Panel → System → Rename Computer**.  
   - Set to `DC01` (if it's a domain controller).  

4. **Activate Windows**  
   - Open **Settings → Update & Security → Activation**.  
   - Enter a valid product key.  

---

### **Step 5: Install Roles and Features**
1. Open **Server Manager**.  
2. Go to **Manage → Add Roles and Features**.  
3. Install the following roles:  
   - **Active Directory Domain Services (AD DS)**  
   - **DHCP Server**  
   - **DNS Server**  
   - **File and Storage Services**  
   - **Windows Backup**  
4. Complete the installation.  

---

### **Step 6: Configure Security Baselines**
1. Download the latest security baselines from the [Microsoft Security Compliance Toolkit](https://www.microsoft.com/en-us/download/details.aspx?id=55319).  
2. Use **Group Policy Management Console (GPMC)** to apply security policies.  
3. Ensure the server meets security standards.  

[Reference: Microsoft Documentation](https://learn.microsoft.com/en-us/windows-server/security/osconfig/osconfig-how-to-configure-security-baselines)  

---

### **Step 7: Update the Server**
1. Open **Settings → Update & Security → Windows Update**.  
2. Click **Check for updates**.  
3. Install the latest patches and security updates.  

---

### **Step 8: Backup Configuration**
1. Open **Server Manager → Add Roles and Features**.  
2. Under **Features**, select **Windows Server Backup**.  
3. Open **Windows Server Backup** from the **Tools** menu.  
4. Configure a backup schedule to back up critical data and system state.

---

## Resources
- **Windows Server 2025 ISO** – [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2025)  
- **VMware Workstation** – [VMware](https://www.vmware.com)  
- **Rufus (Bootable USB Creation)** – [Rufus](https://rufus.ie/)  
- **Microsoft Documentation** – [https://learn.microsoft.com](https://learn.microsoft.com)  
- **Microsoft Security Compliance Toolkit** – [Security Baselines](https://www.microsoft.com/en-us/download/details.aspx?id=55319)  
