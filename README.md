# CMPG325 - Network Design Portfolio
**Client:** CLI-110 (Tlhabane Materials Testing Laboratory)

## Project Overview
This repository contains the network design and Cisco Packet Tracer simulation to address the networking needs of the Tlhabane Materials Testing Laboratory.The completed network permits successful data exchange between appropriate nodes and fulfills the following assigned project parameters

* **Addressing Block:** The core IP addressing plan is based on the assigned 192.168.49.0/24 network block.
* **Design Constraint:** The addressing plan is explicitly designed to accommodate a new branch office that may open within 18 months.
* **Networking Challenge:** The implementation demonstrates a foundational Wireless LAN configuration, focusing on access point (AP) integration and coverage across the network. 
* **Change Request (CR2):** The final topology incorporates network coverage for an additional floor and area of the building that the client recently took over.

## Milestone 1: Network Design & IP Addressing
This section contains the foundational design documentation, topologies, and IP allocations required to build the network.

### Deliverables
* [1. Client Requirements](docs/client_requirements.md)
* [2. Physical Topology](diagrams/physical_topology.png)
* [3. Logical Topology](diagrams/logical_topology.png) / [downloadable packet](packet-tracer/logical_topology.pkt)
* [4. IP Addressing Plan ](docs/ip_addressing_plan.md)

## Milestone 2 
This section contains an active working packet tracer and configurations backed by testing evidence.


### Deliverables

#### [1.Working Packet Tracer](packet-tracer/logical_topology_pt2.pkt)

Contains and demonstrates the following:
* Logical Topology: The fully assembled network with all devices (Main-Router, Core-Switch, Access Switches, PCs, and Access Points) connected and active.
* Active Configurations: This includes the Router-on-a-Stick sub-interfaces, the trunking on the switches, and the VLAN access ports.



#### [2.Ping tests](tests/ping_test)
Contain screenshots of the command prompt windows from end-devices executing the standard ICMP ping command against IP addresses in different subnets

* Inter-VLAN Routing Success: Proves that traffic can successfully leave a device on one VLAN , travel up the trunk to the Main-Router, get routed to a different subnet, and successfully reach a device on another VLAN.
* Network Convergence: The 100% success rate which is the replies received without packet loss proves that all switches have updated their MAC address tables, the router's routing table is accurate, and the network is fully operational.
* End-to-End Connectivity: Validates that the entire physical and logical path from the PC, through the access switch, across the core switch, up to the router, and back down to the destination is free of configuration errors and Spanning Tree Protocol (STP) blocks.
  

#### [3.Device configurations](https://github.com/cliffor-18/CMPG325-2026-110-Tlhabane-Network/tree/afc4fec63d31ada1430fdc3de98ca2564ed1f54f/configs) 

Contains scripts used to build and operate the network.
* Router: The implementation of Inter-VLAN routing, including the creation of logical sub-interfaces, 802.1Q VLAN encapsulation, specific VLSM IP address assignments, and the dynamic DHCP pool setup.
* Core-Switch: The setup of the Layer 2 distribution layer, detailing the global VLAN database creation and the enforcement of 802.1Q trunking on the router uplink and switch downlinks.
* Access Switches(Switch1-F1 & Switch2-F2): The assignments of specific physical access ports to designated VLANs and the confguration of Layer 3 management IPs and default gateways.
  

