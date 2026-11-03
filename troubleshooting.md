## Troubleshooting

Initially, DHCP clients were unable to obtain IP addresses. The DHCP pools were configured correctly, and the DHCP server was reachable over its directly connected link.

Inspection of the DHCP server router's routing table revealed that it was missing routes to the client VLANs.

**Resolution:** Configured OSPF on the DHCP server router so it could dynamically learn the remote client networks and route DHCP replies back to the clients.
