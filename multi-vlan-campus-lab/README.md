# Multi-VLAN Campus Network

Built a 3-tier campus topology in Cisco Packet Tracer with 4 VLANs, 
802.1Q trunking, router-on-a-stick inter-VLAN routing, and STP root 
bridge configuration.

## Technologies Used
- VLANs (10, 20, 30, 40)
- 802.1Q Trunking
- Router-on-a-stick
- Spanning Tree Protocol
- Cisco 2911 Router
- Cisco 2960 Switches

## Network Design
- R1 (2911 router) handles inter-VLAN routing via sub-interfaces
- SW-DIST (2960) acts as distribution switch and STP root bridge
- SW-ACCESS-1 and SW-ACCESS-2 connect end devices
- 4 departments separated into individual VLANs

## IP Addressing
| VLAN | Department | Network | Gateway |
|------|------------|---------|---------|
| 10 | Sales | 10.0.10.0/24 | 10.0.10.1 |
| 20 | HR | 10.0.20.0/24 | 10.0.20.1 |
| 30 | IT | 10.0.30.0/24 | 10.0.30.1 |
| 40 | Management | 10.0.40.0/24 | 10.0.40.1 |

## Verification
- Confirmed inter-VLAN routing with cross-VLAN pings
- Verified trunk links with show interfaces trunk
- Verified STP root bridge election on SW-DIST
- Verified sub-interfaces with show ip interface brief
