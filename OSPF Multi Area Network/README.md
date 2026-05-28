# OSPF Multi-Area Network

Built a multi-area OSPF network in Cisco Packet Tracer across 3 routers 
and 3 OSPF areas, demonstrating dynamic routing, inter-area route 
propagation, and OSPF reconvergence after a simulated link failure.

## Technologies Used
- OSPFv2 (Open Shortest Path First)
- Multi-area OSPF (Area 0, Area 1, Area 2)
- Area Border Router (ABR)
- Cisco 2911 Routers
- Inter-area route summarisation

## Network Design
- R1 — internal router in Area 1 (10.0.1.0/24)
- R2 — Area Border Router connecting Area 1 and Area 0 backbone
- R3 — internal router in Area 2 (10.0.3.0/24)
- /30 subnets used for point-to-point router links

## IP Addressing
| Network | Subnet | Purpose |
|---------|--------|---------|
| 10.0.1.0/24 | 255.255.255.0 | R1 LAN — Area 1 |
| 10.0.3.0/24 | 255.255.255.0 | R3 LAN — Area 2 |
| 10.0.12.0/30 | 255.255.255.252 | R1 to R2 link |
| 10.0.23.0/30 | 255.255.255.252 | R2 to R3 link |

## Verification
- Confirmed OSPF neighbor adjacencies in FULL state on all routers
- Verified O IA (inter-area) routes appearing in R1 routing table
- Confirmed end-to-end connectivity with cross-area ping from PC-A to PC-B
- Simulated link failure on R2 Gi0/1 and observed OSPF reconvergence
- Verified route removal and re-advertisement after interface restored

## Key Concepts Demonstrated
- OSPF hello packets and neighbor discovery
- Area Border Router role in multi-area OSPF
- Inter-area route propagation (O IA routes)
- OSPF reconvergence after topology change
- /30 subnetting for point-to-point links
