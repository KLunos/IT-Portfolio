# Active Directory (AD-LAB-01)

## Purpose
- Centralized identity/authentication for the lab
- Domain-join the Win11 Jump box
- Provide DNS for lab clients and servers
- Foundation for GPO, users/groups, and future security monitoring

## Lab Context
- **VM Name:** AD-LAB-01
- **OS:** Windows Server (version TBD)
- **Role(s):** AD DS, DNS (DHCP optional if used)
- **Domain:** LAB.LOCAL (or your chosen domain)
- **Network:** pfSense LAN (10.10.0.0/24)
- **Static IP:** 10.10.0.X
- **DNS:** 127.0.0.1 (preferred) / 10.10.0.X (alternate)

## High-Level Build Steps (Skeleton)
1. Create VM in Hyper-V (CPU/RAM/Disk)
2. Set static IP + correct DNS settings
3. Rename server to **AD-LAB-01**
4. Install **Active Directory Domain Services**
5. Promote to Domain Controller (create new forest)
6. Install/verify **DNS**
7. (Optional) Configure DHCP (or leave DHCP on pfSense)
8. Create baseline OUs, users, and groups
9. Join Win11 Jump box to domain

## Validation / Evidence (Screenshots Later)
- Server name + IP config
- AD DS installed + DC promotion success
- DNS console showing forward lookup zone
- Domain Users/Computers or custom OU structure
- Win11 Jump box successfully domain-joined
- (Optional) GPO example applied to a test user/computer

## Notes / Lessons Learned (Optional)
- DHCP vs DNS split decisions (pfSense vs AD)
- Anything you changed after first attempt
