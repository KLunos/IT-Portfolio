# Active Directory (AD-LAB-01)

## Purpose
- Centralized identity/authentication for the lab
- Domain-join the Win11 Jump box
- Provide DNS for lab clients and servers
- Foundation for GPO, users/groups, and future security monitoring

  ## Virtual Machine Specifications (Hyper-V)
- The resources I allocated for this virtual machine to run well on the PC.
  - Name:
  - Storage (max/used):
  - Memory:
  - vCPU:
  - [AD-LAB-01](/pfSense/pfSense-specs.png)

## Lab Context
- **VM Name:** AD-LAB-01
- **OS:** Windows Server 2022
- **Role(s):** AD DS, DNS
- **Domain:** LAB.LOCAL
- **Network:** pfSense LAN (10.10.0.0/24)
- **Static IP:** 10.10.0.X
- **DNS:** default gateway (preferred) / 8.8.8.8 (alternate)

## High-Level Build Steps
1. Create VM in Hyper-V (CPU/RAM/Disk)
2. Set static IP + correct DNS settings
3. Rename server to **AD-LAB-01**
4. Install Active Directory Domain Services
5. Promote to Domain Controller
6. Install/verify **DNS**
7. Create some OUs, users, and groups
8. Join Win11 Jump box to domain

## Screenshots
- [Windows Server version](/AD/AD-server-version.png)
- [Domain controller login](/AD/AD-login.png)
- [Updates in progress](/AD/AD-updating.png)
- [Main server dashboard](/AD/AD-server-dashbard.png)
- [Active Directory - users/groups](/AD/AD-groups-and-users.png)

## Notes / Lessons Learned
- [Server error status?](/AD/AD-server-error.png)
- [I cleared it!](/AD/AD-server-fixed.png)
