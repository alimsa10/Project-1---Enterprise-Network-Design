# Project Title: Enterprise Network Design for Construction Company

# 🎯 Project Overview:
This project simulates a complete network infrastructure for a multi-site construction company. It connects a Main HQ and a Branch site, supporting specific departments like Finance, IT, and a Data Center. The design focuses on high availability, redundancy, and efficient traffic management using Huawei eNSP.

# Technical Implementation
This project fulfills the following network requirements and configurations:

### 1. Network Topography & Design

- Multi-Site Architecture: Designed a comprehensive network connecting a Main Headquarters and a Branch Office using a simulated Private WAN.
- Departmental Segmentation: Created dedicated networks for specific departments:
   - Data Center: VLAN 100 (High availability zone)
   - Finance: VLAN 10
   - IT Department: VLAN 20
   - Administration: VLAN 30
   - Marketing: VLAN (120)

### 2. Switching Technologies (Layer 2)
- VLAN Configuration: Implemented VLANs to isolate broadcast domains and improve security.
- Trunking & Access: Configured 802.1Q trunks between switches and access ports for end devices.
- Core Switching: Deployed redundant Core Switches (S1 & S2) at the Main Site to handle inter-VLAN traffic and (S15 & S16) at Branch site.

### 3. Routing Technologies (Layer 3)
- OSPF (Open Shortest Path First): Configured dynamic routing to facilitate automatic route exchange between the Main Site and the Branch Office.
- Static Routing: Implemented default static routes for reliable upstream connectivity to the ISP.
- Inter-VLAN Routing: Enabled communication between different subnets using VLANIF interfaces on the Core Switches.

### 4. Network Services & Management
- DHCP Services: Configured a dedicated DHCP server (AC1 & AC2) to provide dynamic IP addressing to APs and their STA ,and DHCP server (S15) to provide dynamic IP addressing to end devices at Branch site.
- Gateway Redundancy: Utilized Virtual Gateway IPs on the Core layer to ensure continuous connectivity for endpoint devices.
- DNS (Domain Name System): Deployed a DNS server to resolve domain names for internal and external resources.
- SNMP (Simple Network Management Protocol): Enabled SNMP to facilitate network monitoring and management.

### 5. Security & Traffic Control
- NAT (Network Address Translation): Configured to allow internal private IP addresses to access the internet via the ISP.
- Access Control Lists (ACLs): Applied traffic filtering rules to restrict unauthorized access between sensitive departments and the Data Center.



