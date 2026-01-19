# Active Directory (AD-LAB-01)

## Purpose
- Centralized identity/authentication for the lab
- Domain-join the Win11 Jump box
- Provide DNS for lab clients and servers
- Foundation for GPO, users/groups, and future security monitoring

## Lab Context
- **VM Name:** AD-LAB-01
- **OS:** Windows Server 2022
- **Role(s):** AD DS, DNS
- **Domain:** LAB.LOCAL
- **Network:** pfSense LAN (10.10.0.0/24)
- **Static IP:** 10.10.0.X
- **DNS:** 127.0.0.1 (preferred) / 10.10.0.X (alternate)

## High-Level Build Steps (Skeleton)
1. Create VM in Hyper-V (CPU/RAM/Disk)
2. Set static IP + correct DNS settings
3. Rename server to **AD-LAB-01**
4. Install **Active Directory Domain Services**
5. Promote to Domain Controller
6. Install/verify **DNS**
7. Create baseline OUs, users, and groups
8. Join Win11 Jump box to domain

## Validation / Evidence (Screenshots coming soon!)
- Server name + IP config
- AD DS installed + DC promotion success
- DNS console showing forward lookup zone
- Domain Users/Computers or custom OU structure
- Win11 Jump box successfully domain-joined

## Notes / Lessons Learned (Coming soon!)
- DHCP vs DNS split decisions (pfSense vs AD)
