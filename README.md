# MyPortfolio-INTER-VLAN-ROUTING-PROJECT-02
project 02
# Project 02 — Router-on-a-Stick

## Scenario
- Three departments: Finance (VLAN 30), IT (VLAN 20), HR (VLAN 10)
- Need inter-VLAN communication using a single router interface

## VLANs
| VLAN ID | Name    | Hosts |
|---------|--------|-------|
| 10      | HR     | 10    |
| 20      | IT     | 20    |
| 30      | Finance| 30    |

## IP Addressing (VLSM)
- Finance (VLAN30): 192.168.10.1/27 → router subinterface 192.168.10.1  
- IT (VLAN20): 192.168.10.33/27 → router subinterface 192.168.10.33  
- HR (VLAN10): 192.168.10.65/27 → router subinterface 192.168.10.65  

## Switch Configuration
- VLANs created: 10, 20, 30  
- Ports assigned to VLANs (Fa0/1–6)  
- Trunk: Fa0/24 → Router Gig0/0

## Router Configuration
- Subinterfaces configured with 802.1Q encapsulation  
- No shutdown on Gig0/0  

## Verification
- Ping tests between PCs within the same VLAN → successful  
- Ping tests between PCs in different VLANs → successful

## Outcome
- All VLANs remain logically separated  
- Inter-VLAN routing works via Router-on-a-Stick
