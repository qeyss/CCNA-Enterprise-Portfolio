# CCNA-Enterprise-Portfolio

This repository documents a rigorous, hands-on deployment track consisting of **50 sequential projects**. It bridges academic **Cisco CCNA (200-301)** concepts with real-world engineering requirements for Small and Medium-sized Enterprises (SMEs). All documentation, engineering logs, and topologies are written in English to match official industry standards.

---

## 🛠️ Active Phase: Core Infrastructure (Projects 1–11)

### 🧱 Module 1 — Network Fundamentals
* **[Project 01: Network Design under SME Constraints](./Module_01_Network_Fundamentals/Project_01_SME_Network_Design/)**
  * *Focus:* Physical/logical hierarchy, flow validation, Draw.io architectural blueprints.

### 🔌 Module 2 — Ethernet LAN Switching
* **[Project 02: Network Segmentation & VLANs](./Module_02_Ethernet_LAN_Switching/Project_02_Network_Segmentation_VLANs/)**
  * *Focus:* Broadcast domain isolation, 802.1Q encapsulation, Trunk links.
* **[Project 03: L2 Redundancy & STP Observation](./Module_02_Ethernet_LAN_Switching/Project_03_L2_Redundancy_STP/)**
  * *Focus:* Loop prevention, manual Root Bridge election, RSTP state changes.
* **[Project 04: Bandwidth Increase via EtherChannel](./Module_02_Ethernet_LAN_Switching/Project_04_Bandwidth_Aggregation_EtherChannel/)**
  * *Focus:* Link aggregation, LACP negotiation, cross-floor distribution links.

### 🌐 Module 3 — IP Connectivity
* **[Project 05: Structured IP Addressing Plan](./Module_03_IP_Connectivity/Project_05_Structured_IP_Addressing_Plan/)**
  * *Focus:* VLSM optimization, network/host division, explicit reservation ranges.
* **[Project 06: Network Printers Integration](./Module_03_IP_Connectivity/Project_06_Network_Printers_Integration/)**
  * *Focus:* Static IP targeting outside dynamic pools, local device staging.
* **[Project 07: Multiple Branches Static Routing](./Module_03_IP_Connectivity/Project_07_Multiple_Branches_Static_Routing/)**
  * *Focus:* Next-hop resolution, multi-hop route propagation, raw routing table analysis.
* **[Project 08: WAN Redundancy via Floating Static Routes](./Module_03_IP_Connectivity/Project_08_WAN_Redundancy_Floating_Static/)**
  * *Focus:* Administrative Distance manipulation, automated failover verification.
* **[Project 09: Inter-VLAN Routing via Router-on-a-stick](./Module_03_IP_Connectivity/Project_09_Inter_VLAN_Routing_ROAS/)**
  * *Focus:* Subinterface creation, dot1q termination, single-point gateway limits.
* **[Project 10: Inter-VLAN Routing via Layer 3 Switch](./Module_03_IP_Connectivity/Project_10_Inter_VLAN_Routing_L3_Switch/)**
  * *Focus:* Switched Virtual Interfaces (SVI), ASIC-wireline speed routing, routed ports.
* **[Project 11: Dynamic SME Routing via Single-Area OSPF](./Module_03_IP_Connectivity/Project_11_Dynamic_Routing_OSPF/)**
  * *Focus:* Link-state engine, neighbor states, LSDB sync, convergence timers.

---

## 💻 Verification Command Quick-Reference (Cheat Sheet)

| Layer | Verification Target | Primary Cisco IOS Command |
| :--- | :--- | :--- |
| **L2** | VLAN Database Layout | `show vlan brief` |
| **L2** | Operational Trunks | `show interfaces trunk` |
| **L2** | Spanning-Tree Topology | `show spanning-tree` / `show spanning-tree vlan <id>` |
| **L2** | EtherChannel State | `show etherchannel summary` |
| **L3** | IP Interfaces Brief | `show ip interface brief` |
| **L3** | Complete Routing Table | `show ip route` |
| **L3** | Active OSPF Adjacencies | `show ip ospf neighbor` |
