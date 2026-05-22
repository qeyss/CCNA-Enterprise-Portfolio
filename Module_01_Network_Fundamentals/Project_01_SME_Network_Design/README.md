# Project 01: Network Design under SME Constraints

## 📝 Objective
Design a hierarchical, secure, and scalable physical network architecture for a Small and Medium-sized Enterprise (SME) spread across a 3-story building, using a standardized Cisco design model before any hardware configuration.

## 🏢 Business Constraints & Scenario
* **Physical Layout:** 3 floors with a dedicated server room located on the 3rd floor.
* **Hardware Availability:** 1 Edge Internet Router, 1 Core/Distribution Layer 3 Switch, and multiple Access Switches.
* **Traffic Flows:** Internals users must access the Server Room, and all departments require secure Internet access.

## 🗺️ Physical Topology Diagram
This blueprint uses a classic hierarchical design (Core/Distribution layer collapsed into a single backbone switch, connecting to distinct access switches per floor).

![SME Hierarchical Network Design](topology_sme.png)

## 🧠 Architectural Design Choices (Theory Cheat Sheet)

### 1. Hierarchical Layers Used:
* **Core / Distribution Layer (Collapsed Core):** Handled by a single high-performance Layer 3 Switch in the server room. It acts as the central backbone of the company, routing traffic between floors/departments and enforcing security policies.
* **Access Layer:** Handled by Layer 2 switches deployed on each floor. Their unique job is to provide network connectivity directly to end-user devices (PCs, laptops, printers).

### 2. Benefits of this Design:
* **Scalability:** If the company grows and adds a 4th floor, we simply add a new Access Switch and connect it directly to the Core Switch without disrupting the existing infrastructure.
* **Performance:** Local floor traffic stays on the local access switch. Cross-floor traffic goes directly to the Core at wire speed, preventing bottlenecks.
* **Security Isolation:** By separating floors physically, we prepare the infrastructure for logical segmentation (VLANs) in the next phase.

## 🔍 Validation & Review Checklist
- [ ] Verify that every Access Switch has a direct uplink to the Core Switch (Star Topology).
- [ ] Confirm the Edge Router is connected directly to the Core Switch to handle external Internet boundaries.
- [ ] Validate that all end-user endpoints terminate at the Access Layer, never directly on the Core Switch or Router.