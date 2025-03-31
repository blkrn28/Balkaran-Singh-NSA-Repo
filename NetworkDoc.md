# Home Network Documentation

## Introduction
This document serves as comprehensive documentation for the home network, detailing both physical and logical topologies, addressing schemes, device configurations, and security practices. Proper documentation helps in troubleshooting, network expansion, and security reinforcement.

---

## Physical and Logical Topologies

### Physical Topology
The physical topology outlines the layout of all network devices, their physical placement, and how they are connected.
![Physical Tology](https://github.com/user-attachments/assets/6d569f1f-2ef1-454a-a841-63dd96730343)

#### Network Layout and Device Placement:
- **Room**
  - **PC0**: Desktop computer connected via wired Ethernet (FastEthernet 0)
  - **Smartphone0**: Connected wirelessly to the router
- **Living Room**
  - **PC1**: Wired connection using FastEthernet 0
  - **Laptop0**: Connected via wired Ethernet (FastEthernet 0)
- **Bathroom**
  - **Router**: Central networking device with wired and wireless connections
- **Kitchen**
  - No direct network devices, but Wi-Fi coverage is ensured

#### Router Connections:
- **Ethernet 0/0** → Connected to the Cloud (ISP) for internet access
- **Ethernet 0/1** → PC0 (Wired - Room)
- **Ethernet 0/2** → PC1 (Wired - Living Room)
- **Ethernet 0/3 (Wireless)** → Smartphone0, Smartphone1, and other wireless devices

---

## Logical Topology
The logical topology represents how data flows within the network, IP addressing, and segmentation.
![logical topology](https://github.com/user-attachments/assets/34ca2013-ecf0-491e-a7ae-33f80b7c5ef5)

- **Subnet**: `192.168.1.0/24`
- **Default Gateway**: `192.168.1.1` (Router’s LAN interface)
- **Device Addressing:**
  - **PC0** → `192.168.1.10` (Static IP)
  - **PC1** → `192.168.1.11` (Static IP)
  - **Laptop0** → `192.168.1.12` (Static IP)
  - **Smartphone0** → `192.168.1.20` (DHCP-assigned)
  - **Smartphone1** → `192.168.1.21` (DHCP-assigned)

---

## Addressing Documentation

| Device       | Interface      | IP Address     | Connection Type |
|-------------|--------------|---------------|----------------|
| Router      | Ethernet 0/0  | Dynamic (ISP) | WAN            |
| Router      | Ethernet 0/1  | 192.168.1.1   | LAN            |
| PC0         | FastEthernet 0 | 192.168.1.10  | Wired          |
| PC1         | FastEthernet 0 | 192.168.1.11  | Wired          |
| Laptop0     | FastEthernet 0 | 192.168.1.12  | Wired          |
| Smartphone0 | Wireless 0/3  | 192.168.1.20  | Wireless       |
| Smartphone1 | Wireless 0/3  | 192.168.1.21  | Wireless       |

---

## Detailed Device Information

| Device       | Type          | Model               | OS/Software Version |
|-------------|--------------|---------------------|---------------------|
| Router      | Router       | Cisco Router-PT-AC | Firmware v1.2       |
| PC0         | Desktop      | Custom Build       | Windows 10 Pro      |
| PC1         | Desktop      | Dell Optiplex      | Windows 11 Pro      |
| Laptop0     | Laptop       | HP EliteBook       | Windows 11 Pro      |
| Smartphone0 | Smartphone   | iPhone 12         | iOS 17              |
| Smartphone1 | Smartphone   | Samsung Galaxy S22 | Android 14          |

---

## Configuration Maintenance
To ensure network stability and recoverability, configurations are periodically backed up.

- **Router Configuration:**
  - Configuration is stored in `startup-config` and backed up weekly to external storage.
  - Firmware updates are checked monthly.
- **PC and Laptop Configurations:**
  - System restore points are created weekly.
  - Automated backups to cloud storage (OneDrive, Google Drive) are enabled.
- **Mobile Device Configurations:**
  - Encrypted cloud backups (iCloud, Google Backup) are used.

---

## Secure Storage of Login Credentials
To protect sensitive credentials, the following methods are used:

1. **Password Manager:** Securely stores router and device login information in an encrypted vault.
2. **Multi-Factor Authentication (MFA):** Enabled on all applicable accounts and devices.
3. **Offline Storage:** A hardcopy of critical credentials is securely stored in a locked location.

---

## Network Security Measures
Security is a top priority for the home network. Implemented measures include:

- **Firewall Configuration:** Configured on the router to filter traffic and prevent unauthorized access.
- **MAC Address Filtering:** Restricts access to known devices.
- **Wireless Security:**
  - WPA3 encryption for secure Wi-Fi connections.
  - Hidden SSID to prevent unauthorized visibility.
- **Regular Security Audits:**
  - Monthly check on connected devices.
  - Network scanning for vulnerabilities using Nmap and Wireshark.

---

## Conclusion
This document provides a detailed overview of the home network, ensuring that all aspects of network documentation are covered. Regular updates to this document are recommended to keep it relevant and useful for future network expansions and troubleshooting.
