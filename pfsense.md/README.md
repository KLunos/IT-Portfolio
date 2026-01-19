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

## Screenshots (Coming soon!)

- [ ] pfSense dashboard
- [ ] Interfaces
- [ ] VLAN configuration
- [ ] DHCP scopes
- [ ] Firewall rules
- [ ] Logs

## Lessons Learned (Coming soon!)
