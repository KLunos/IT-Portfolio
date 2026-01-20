# pfSense Firewall and VLAN Segmentation

## Purpose
I built pfSense as an edge firewall and router for my home lab to practice real-world network segmentation, access control, and troubleshooting.

## What I Built
- WAN/LAN routing using pfSense as the gateway
- VLAN segmentation for isolated networks
- Separate DHCP scopes per network
- Firewall rules enforcing least privilege
- Logging and monitoring aligned with Security Onion goals

## Architecture Overview
pfSense sits between the WAN and my internal virtual networks, controlling traffic between segments and enforcing security policies.

## Key Configurations

### Interfaces
- WAN:vExternal
- LAN:vLabLAN
- VLANs:10.10.0.0/24

### DHCP
- Main LAN:10.10.0.120 - 10.10.0.199
- Guest/IoT:N/A

### Firewall Rules (Summary)
- Default deny between VLANs
- Allow only required services
- Management access from jump box only

## Screenshots

- [pfSense Web UI login (from Win11 Jump)](/pfSense/pfSense-WebUI-Login-from-jump.png)
- [pfSense console main menu](pfSense/pfSense-main-console.png)
- [Jump box IP config (vExternal + vLabLAN)](pfSense/pfSense-Interfaces-vExternal-vLabLAN.png)

### Console output (sanitized)
- [ifconfig (page 1)](pfSense/pfSenseifconfig1.png)
- [ifconfig (page 2)](pfSense/pfSenseifconfig2.png)
- [netstat -rn (page 1)](pfSense/pfSensenetstat1.png)
- [netstat -rn (page 2)](pfSense/pfSensenetstat2.png)

## Lessons Learned (Coming soon!)
