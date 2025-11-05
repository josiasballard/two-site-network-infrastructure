# Two-Site Network Infrastructure Lab

A full virtual environment simulating a small business network with **two connected sites** — Rapid City HQ and Dallas branch.  
Built on **Windows 11 Pro with Hyper-V**, this lab demonstrates enterprise-level IT design on a single workstation.

---

## 🧠 Purpose
To showcase real-world IT infrastructure skills across networking, system administration, and security:
- Active Directory, DNS, DHCP, and File Services
- VLAN segmentation and inter-site VPN
- VoIP network (PBX and extensions)
- Endpoint management with MDM / Intune
- Group Policy baselines and conditional access
- Documentation and network diagrams

---

## 🧩 Topology Summary
**Site 1 – HQ (Rapid City)**  
Primary AD DS / DNS / DHCP • File Server • Main PBX • Intune / MDM integration  

**Site 2 – Branch (Dallas)**  
Replica Domain Controller • DHCP failover • Local file cache • Remote VoIP extensions  

**VPN:** pfSense site-to-site (IPsec)  
**Subnets:**  
- HQ – 10.10.x.x/24 VLANs (Mgmt, Workstations, Servers, VoIP, Guest)  
- Branch – 10.20.x.x/24 VLANs (mirrored layout)

---

## 🧱 Core Components
| Role | Function |
|------|-----------|
| pfSense | Routing, VLANs, VPN, QoS |
| Windows Server 2022 | AD DS, DNS, DHCP, GPOs |
| File Server | NTFS permissions, DFS replication |
| FreePBX | SIP PBX to simulate Allworx-style VoIP |
| MDM Server | Intune trial + Flyve MDM demo |
| Clients | 6 Windows, 4 macOS (sim), 6 iOS, 4 Android |

---

## 📂 Repository Layout
two-site-network-infrastructure/
├── README.md
├── diagrams/
│   ├── topology.png
│   ├── rc_vlan_map.png
│   └── dallas_vlan_map.png
├── pfSense/
│   ├── rc_config.md
│   ├── dallas_config.md
│   └── vpn_tunnel_summary.txt
├── ad/
│   ├── ou_structure.txt
│   ├── gpo_reports/
│   └── replication_test.txt
├── dhcp_dns/
│   └── scope_exports.txt
├── voip/
│   └── pbx_setup.md
├── mdm/
│   ├── intune_notes.md
│   └── enrollment_screenshots/
├── inventory/
│   └── device_inventory.csv
├── scans/
│   └── site_scan.nmap
├── reports/
│   └── audit_summary.pdf
└── screenshots/
    ├── ad_replication.png
    ├── pfSense_vlans.png
    ├── freepbx_dashboard.png
    └── intune_devices.png




---

## 🧰 Tools & Technologies
Windows Server • Hyper-V • pfSense • FreePBX • Intune / Flyve • Azure AD / Entra ID • PowerShell • draw.io • nmap

---

## 🚀 Goals
1. Design a working dual-site network using VLANs and VPNs  
2. Implement AD replication and GPO baseline  
3. Configure VoIP extensions and QoS policies  
4. Demonstrate MDM device management  
5. Document everything for review on GitHub

---

> Built and documented by **Josias Ballard** – IT Specialist | A+ Certified | Net+/Sec+ in progress
