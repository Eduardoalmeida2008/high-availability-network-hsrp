# High-Availability Enterprise Network Infrastructure 🚀
**A resilient multi-department network infrastructure featuring Cisco HSRP, VLAN segmentation, and automated services.**

## 📌 Overview
This project simulates a robust corporate network environment designed for 100% uptime. By implementing **HSRP (Hot Standby Router Protocol)**, the infrastructure ensures seamless gateway redundancy across 15 distinct VLANs, preventing any single point of failure.

> **Status:** Fully Verified & Documented ✅

## 📐 Network Topology
![Network Topology Overview](./print/01_Network_Topology_Overview.png)
*Full view of the 15 departments segmenting the broadcast domains.*

## 🛠️ Tech Stack & Protocols
- **Tool:** Cisco Packet Tracer
- **Redundancy:** HSRP (Hot Standby Router Protocol)
- **Routing:** Inter-VLAN Routing (Router-on-a-Stick)
- **Switching:** VTP, STP, 802.1Q Trunking
- **Services:** DHCP Server (IPv4 Pools per VLAN)

## ⚙️ Core Configurations & Redundancy

### 1. Gateway Redundancy (HSRP)
I configured a dual-router setup (Active/Standby). If the primary router fails, the secondary takes over the virtual IP (VIP) instantly.

| Active Router State (R1) | Standby Router State (R2) |
|---|---|
| ![R1 Active State](./print/02_R1_HSRP_Active_State_Brief.png) | ![R2 Standby State](./print/03_R2_HSRP_Active_State_Brief.png) |

### 2. DHCP Infrastructure
Automated IP assignment for all 15 VLANs configured directly on the Core.
![DHCP Pool Configuration](./print/06_DHCP_Pool_Configuration_CLI.png)

## 🧪 Verification & Failover Tests

### Connectivity Test (Inter-VLAN)
Ping tests confirm that traffic flows correctly between different departments through the HSRP virtual gateway.
![InterVLAN Ping Test](./print/08_InterVLAN_Ping_Test_Success.png)

### Failover Simulation
Critical test performed by disabling the primary link. HSRP traffic migrated to the backup router in seconds.
![HSRP Failover Simulation](./print/09_HSRP_Failover_Simulation_Verified.png)

---
**Developed by:** Eduardo Almeida  
**Date:** January 2026  
*Connect with me for Network Infrastructure and Support projects.*
