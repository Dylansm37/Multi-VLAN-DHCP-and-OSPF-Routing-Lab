# Multi-VLAN DHCP and OSPF Routing Lab

## Overview

This lab demonstrates DHCP across multiple VLANs using Cisco routers, router-on-a-stick, DHCP relay, and OSPF dynamic routing.

## Objectives

- Configure VLANs 10, 20, 30, and 40.
- Configure router subinterfaces using 802.1Q encapsulation.
- Configure DHCP pools for multiple client networks.
- Configure `ip helper-address` to relay DHCP requests.
- Configure OSPF so routers learn routes to remote VLANs.
- Troubleshoot DHCP failures caused by missing return routes.

## IP Addressing

| VLAN | Network | Default Gateway |
|---|---|---|
| 10 | 192.168.10.0/24 | 192.168.10.1 |
| 20 | 192.168.20.0/24 | 192.168.20.1 |
| 30 | 192.168.30.0/24 | 192.168.30.1 |
| 40 | 192.168.40.0/24 | 192.168.40.1 |

## Technologies

- Cisco IOS
- DHCP and DHCP relay
- OSPF
- 802.1Q VLAN trunking
- Cisco Packet Tracer

## Verification

The following commands were used to verify interface status, OSPF neighbors, routing tables, and DHCP operation.

### Interface Status

```cisco
show ip interface brief
```

### OSPF Neighbors

```cisco
show ip ospf neighbor
```

### Routing Table

```cisco
show ip route
```

### DHCP Pools

```cisco
show ip dhcp pool
```

### DHCP Bindings

```cisco
show ip dhcp binding
```

### Running Configuration

```cisco
show running-config
```

## Files

- `lab.pkt` — Packet Tracer topology
- `configs/` — Router configuration files
- `topology.png` — Network topology diagram
- `troubleshooting.md` — Troubleshooting notes
