# High-Availability Enterprise Network Infrastructure 🚀
**A resilient multi-department network simulation featuring Cisco HSRP, Inter-VLAN routing, and DHCP services.**

## 📌 Overview
This project simulates a robust corporate network environment designed for 100% uptime. By implementing **HSRP (Hot Standby Router Protocol)**, the infrastructure ensures seamless gateway redundancy across 15 distinct VLANs, preventing any single point of failure.

> **Status:** Fully Verified & Documented ✅

## 🛠️ Tech Stack & Protocols
- **Tool:** Cisco Packet Tracer
- **Redundancy:** HSRP (Hot Standby Router Protocol)
- **Routing:** Inter-VLAN Routing (Router-on-a-Stick)
- **Switching:** VTP, STP, 802.1Q Trunking
- **Services:** DHCP Server (IPv4 Pools per VLAN), ICMP (Verification)

## 📐 Network Architecture
The design follows a hierarchical model (Core, Distribution, Access) to ensure scalability and manageability.

### [Insira aqui a imagem: 01_Network_Topology_Overview.png]
*Full view of the 15 departments (Management, HR, Sales, Marketing, etc.) segmenting the broadcast domains.*

## ⚙️ Core Configurations

### 1. Gateway Redundancy (HSRP)
I configured a dual-router setup (Active/Standby). If the primary router (R1-CORE-A) fails, the secondary (R2-CORE-B) takes over the virtual IP (VIP) instantly.

**Active Router State (R1):**
### [Insira aqui a imagem: 02_R1_HSRP_Active_State_Brief.png]

**Standby Router State (R2):**
### [Insira aqui a imagem: 03_R2_HSRP_Active_State_Brief.png]

### 2. VLAN & DHCP Services
Each department has a dedicated DHCP pool configured directly on the Core routers to automate IP assignment.

### [Insira aqui a imagem: 06_DHCP_Pool_Configuration_CLI.png]
*Example of the DHCP pools for VLANs 10 through 150.*

## 🧪 Verification & Failover Tests

### Connectivity Test (Inter-VLAN)
Ping tests confirm that traffic flows correctly between different departments through the HSRP virtual gateway.
### [Insira aqui a imagem: 08_InterVLAN_Ping_Test_Success.png]

### Failover Simulation
A critical test was performed by disabling the primary link. The simulation logs confirm that HSRP traffic migrated to the backup router in seconds without user intervention.
### [Insira aqui a imagem: 09_HSRP_Failover_Simulation_Verified.png]

## 📁 Repository Structure
- `/topology`: Contains the `.pkt` (Cisco Packet Tracer) source file.
- `/documentation`: High-resolution screenshots of CLI configurations and verification tests.
- `README.md`: Project summary and technical details.

---
**Developed by:** Eduardo Almeida  
**Date:** January 2026  
*Connect with me for Network Infrastructure and Support projects.*
