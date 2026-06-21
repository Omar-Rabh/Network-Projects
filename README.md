Enterprise Branch Connectivity & Security Architecture
 The Objective
This project addresses the critical need for a reliable, scalable, and secure network infrastructure connecting a headquarters branch (Cairo) to a remote branch (Alexandria). The core goal was to eliminate single points of failure while enforcing strict security policies to protect sensitive departmental data.

 Problem-Solving Approach (Why we did it)
Ensuring Non-stop Connectivity: Implemented HSRP (Hot Standby Router Protocol) to provide gateway redundancy. This ensures that if the primary router fails, the secondary one takes over instantly, keeping the business operational.

Optimizing Bandwidth & Reliability: Deployed EtherChannel to bundle physical links between switches, increasing bandwidth and providing link-level fault tolerance.

Efficient Traffic Routing: Utilized the OSPF dynamic routing protocol to allow the network to automatically adapt to topology changes and find the best path between branches.

Granular Security Implementation (The "Zero-Trust" Policy): Enforced specific access policies using Extended ACLs to protect the central data center:

Web Service Restriction: Explicitly blocked HTTP (port 80) traffic from sensitive departments (Sales VLAN 10, HR VLAN 30, and Directory VLAN 60) to the central server.

Diagnostic Lockdown: Enforced a network-wide policy to block ICMP (Ping) requests to the server, preventing unauthorized reconnaissance of the data center.

Selective Access: Enabled full connectivity for the Marketing department (VLAN 20) and permitted all other legitimate traffic.

Scalable WAN Design: Designed the WAN link as a secure point-to-point connection, simulating modern enterprise-grade tunneling to ensure inter-branch communication is both fast and logically separated.

🛠️ Technologies Used
Core Protocols: OSPF, HSRP.

Layer 2 Optimization: EtherChannel, VLAN Trunking (802.1Q).

Security: Extended Access Control Lists (ACLs).

Simulation: Cisco Packet Tracer.
