# Enterprise Network Lab using Cisco Packet Tracer

This project demonstrates the design and configuration of an enterprise-style network using:
- VLAN segmentation
- Inter-VLAN routing (Router-on-a-Stick)
- DHCP automation
- ACL security
- SSH remote management
- Static routing
- NAT for WAN access

All configurations were implemented and tested in Cisco Packet Tracer.

## Network Topology

The following diagram represents the full network topology, including VLAN segments, trunk links, routers, switches, and the WAN connection.

![Network Diagram](Network-Diagram.png)

## Device Configurations
### Switch100 Configuration

This switch acts as the core switch for the left-side network segment.
It handles VLAN segmentation for VLAN 10 and VLAN 99, and it also provides the uplink to the router.
	•	Connects directly to Router100 for inter-VLAN routing
	•	Provides a trunk connection to Switch200
	•	Carries VLANs 10, 20, and 99 over the trunk link
  
![Switch100 Configuration](Switch100-conf.png)

### Switch200 Configuration

This access switch serves VLAN 20 on the left-side network segment.

- Receives a trunk link from Switch100 on Fa0/1 (VLANs 10, 20, and 99 allowed).
- Provides access ports for PCs in VLAN 20 (PC3 and PC4).
- Extends the same VLAN segmentation from the core switch to the edge devices.

![Switch200 Configuration](Switch200-conf.png)

