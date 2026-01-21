## Kev's IT Portfolio

This project was born on October 17th, 2025, and will continue to improve in detail and evolve as I discover more of my own interests in the world of IT. I have worked with computers in some capacity my entire life, beginning with the Atari ST and Commodore Amiga. Being a gamer my whole life, maybe its only natural that I feel a pull towards IT Security as a long term career. But this is just the beginning, so I have immersed myself in the world of ticketing systems, network troubleshooting, and documentation.
I am CompTIA A+, Network+, and Security+ certified. Obtaining these self credentials and creating this home lab from scratch proves that I am well prepared for work in the IT field.

## Overview

  Using a hypervisor on my laptop, I simulate a real-world business environment where users connect through a firewall to internal services via a Windows jump box. This provides access to an Ubuntu Apache server running osTicket, a Windows server running an Active Directory domain, and a full Security Onion monitoring stack. This portfolio is designed to document what I built, how I built it, why I built it, what issues I ran into along the way, and how I fixed them. Included are many screenshots designed to prove that what I claim I built exists, and works. This includes the connections involved in my networking maps. They also tell the story of mistakes made along the way, and how I learned from them.

### Hardware
Laptop: Lenovo ThinkPad, Ryzen 7 7735HS, 64 GB RAM, 1 TB SSD

### Software
The host runs on Windows 11 Pro. The virtual machines are run in Hyper-V and are comprised of: pfSense, Windows 11 Pro, Windows Server 2022, Ubuntu 24.04.3 LTS, Security Onion 2.4.201,

## Network Topology (Physical and Logical)
This visually documents the physical layout and logical segmentation of my home network, along with the VLANs, firewall, boundaries, and routing paths of my home lab.

- [Host Windows version](/HostWinVer.png)
- [Host specs](/HostSpecs.png)
- [Proof of life!](/HomeLabRunning.png)
  - This shows Hyper-V, with all five virtual machines running.

### Physical Topology
- [Physical Network Map](Physical-Topology.png)

*This diagram shows the actual physical layout of my home network, including the ISP demarc, firewall/router, switches, access points, and where my home lab resides within the network. This demonstrates my understanding of hardware placement, cabling, and how choices affect performance, reliability, and scalability.*

### Logical Topology
- [Logical Network Map](Logical-Topology.png)

*This diagram shows the logical structure of my home network, highlighting traffic flow through my virtual lab. It documents DHCP scopes and VLAN segmentation via pfSense, and multiple lab servers all monitored by Security Onion. This demonstrates my ability to design, secure, and document enterprise style network environments.*

# [pfSense (Firewall and VLAN Segmentation)](pfsense.md)
# [Windows 11 Jump Box](jumpbox.md)
# [osTicket (Ubuntu Server)](osTicket.md)
# [Active Directory](AD-LAB-01.md)
# [Security Onion](SecOnion.md)
