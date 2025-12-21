# 🏫 Technical College Campus Network Design & Implementation

## 📌 Project Overview
This project presents the **design and implementation of a full technical college campus network** using **Cisco Packet Tracer**.  
The network simulates a **real-world enterprise/university environment** consisting of multiple buildings, departments, users, and services, with a strong focus on **scalability, security, and fault tolerance**.

---

## 🏢 Campus Structure
The campus consists of **four main buildings**:
- **Administration Building**
- **Engineering Building**
- **Computer Science Building**
- **Library**

Each building supports:
- Administrative staff  
- Students  
- Specialized computer labs  
- Wired and wireless connectivity  

---

## 🔢 Scale & Capacity
- **Total devices**: ~350+ end devices  
- **Supported users**:
  - Students: 250+ concurrent users  
  - Staff/Faculty: 75+ users  
- **Infrastructure**:
  - Routers: 6  
  - Multilayer switches: 8  
  - Access switches: 20+  
  - Wireless Access Points: 12+  
  - Servers: 6+  
  - IP Phones & network printers  

---

## 🌐 Network Architecture
### 🔹 Layered Design
- **Access Layer**: End devices, labs, wireless users  
- **Distribution Layer**: Multilayer switches, VLAN routing  
- **Core Layer**: High-speed routing between buildings  

### 🔹 Topology
- **Mesh topology** between core routers to avoid single points of failure  
- Redundant paths ensure high availability and fast recovery  

---

## 🧩 IP Addressing & VLAN Design
- Logical **IP addressing plan** with subnetting per department  
- **VLAN segmentation** to isolate traffic and improve security  

### VLANs Used:
| VLAN ID | Name |
|------|------|
| 10 | Admin-VLAN10 |
| 20 | Admin-VLAN20 |
| 30 | Admin-VLAN30 |
| 40 | Admin-VLAN40 |

Inter-VLAN routing is handled using **multilayer switches (SVIs)**.

---

## 🔁 Routing Protocols
### 🟢 OSPF (Internal Routing)
- Used for **intra-campus routing**
- Fast convergence and automatic failover
- Handles 50+ internal routes across buildings

### 🔵 BGP (External Routing)
- Implemented on the **central router**
- **AS Number: 5000**
- Used for secure and scalable external connectivity
- **OSPF routes are redistributed into BGP**
- Multiple BGP peers for redundancy and policy-based routing

👉 This hybrid design reflects **real enterprise and university networks**.

---

## 🔐 Security Implementation
### 🔹 Access Control Lists (ACLs)
- **Extended ACL 100**:
  - Restricts **SSH & Telnet access** to the **IT Department subnet (13.0.0.0/11) only**
- **Standard ACL 10**:
  - Permits authorized IT subnet traffic

This ensures secure management-plane access and controlled inter-subnet communication.

---

## 🖥️ Network Services
Configured servers provide:
- ✅ **DHCP** – Dynamic IP assignment for all VLANs  
- ✅ **DNS** – Internal name resolution  
- ✅ **Web Server** – Internal college portal  
- ✅ **Database Server** – Academic & system data  
- ✅ **Backup Servers (2)** – Redundancy & disaster recovery  
- ✅ **Print Services** – Network printer integration  

---

## 📊 Budget & Cost Planning
A **realistic budget and cost table** was created, covering:
- Network devices
- Servers
- Infrastructure components

This adds a **practical, real-world planning aspect** to the project.

---

## 🧪 Verification & Testing
The implementation was verified using:
- `show access-lists`
- `show vlan`
- `show ip route ospf`
- `show ip bgp`

These commands confirm correct routing, VLAN configuration, security policies, and protocol operation.

---

## 📜 License
This project is for **educational and academic purposes**.
