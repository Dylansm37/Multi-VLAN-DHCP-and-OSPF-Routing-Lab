Multi-VLAN DHCP and OSPF Routing Lab
Overview
This lab demonstrates DHCP across multiple VLANs using Cisco routers, router-on-a-stick, DHCP relay, and OSPF dynamic routing.
Objectives
Configure VLANs 10, 20, 30, and 40.
Configure router subinterfaces using 802.1Q encapsulation.
Configure DHCP pools for multiple client networks.
Configure ip helper-address to relay DHCP requests.
Configure OSPF so routers learn routes to remote VLANs.
Troubleshoot DHCP failures caused by missing return routes.
IP Addressing
VLAN
Network
Default Gateway
10
192.168.10.0/24
192.168.10.1
20
192.168.20.0/24
192.168.20.1
30
192.168.30.0/24
192.168.30.1
40
192.168.40.0/24
192.168.40.1

Technologies
Cisco IOS
DHCP and DHCP relay
OSPF
802.1Q VLAN trunking
Packet Tracer
Troubleshooting
Initially, DHCP clients were unable to obtain IP addresses. The DHCP pools were configured, and the DHCP server was reachable over its directly connected link.
Inspection of the DHCP server's routing table revealed that it lacked routes to the client VLANs. OSPF was configured on the DHCP server router so it could learn the remote networks and return DHCP replies to the clients.
Verification
Commands used:
show ip interface brief
show ip ospf neighbor
show ip route
show ip dhcp pool
show ip dhcp binding
show running-config
Files
lab.pkt: Packet Tracer topology
configs/: Router configuration files
topology.png: Network topology
troubleshooting.md: Troubleshooting notes
