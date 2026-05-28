# NAT/PAT — Network Address Translation

Configured NAT overload (PAT) on a Cisco 2911 router to translate 
multiple private hosts through a single public IP address, simulating 
how home and enterprise routers connect private networks to the internet.

## Technologies Used
- NAT overload (PAT)
- Standard ACL for NAT traffic selection
- Inside/outside interface designation
- Cisco 2911 Router · Cisco 2960 Switch

## Network Design
- Private LAN: 192.168.1.0/24 (3 PCs)
- Public network: 203.0.113.0/24 (simulated internet)
- R1 performs PAT — all private hosts share 203.0.113.1

## IP Addressing
| Device | IP Address | Network |
|--------|-----------|---------|
| PC1 | 192.168.1.10 | Private |
| PC2 | 192.168.1.20 | Private |
| PC3 | 192.168.1.30 | Private |
| R1 inside | 192.168.1.1 | Private |
| R1 outside | 203.0.113.1 | Public |
| Web server | 203.0.113.10 | Public |

## Verification
- Confirmed PAT translations with show ip nat translations
- Verified all three private hosts share one public IP
- Confirmed private IPs hidden from outside network
- Tested connectivity from all PCs to public web server
