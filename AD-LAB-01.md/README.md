# Active Directory (AD-LAB-01)

## Purpose
- Centralized identity/authentication for the lab
- Domain-join the Win11 Jump box
- Provide DNS for lab clients and servers
- Foundation for GPO, users/groups, and future security monitoring

  ## Virtual Machine Specifications (Hyper-V)
- The resources I allocated for this virtual machine to run well on the PC.
  - Name: AD-LAB-01
  - Storage (max/used): 3.11GB / 80GB
  - Memory: 4GB
  - vCPU: 2
- [AD-LAB-01](/AD/AD-specs.png)

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
  - Proof of the version of Windows Server.
- [Domain controller login](/AD/AD-login.png)
  - This is medirectly logging into the server using the credentials I log in with from the jump box.
- [Updates in progress](/AD/AD-updating.png)
  - The place to directly execute updates is different from normal Windows. Keeping up with them is high priority!
- [Main server dashboard](/AD/AD-server-dashbard.png)
  - Just a basic shot of the dashboard, showing that it exists.
- [Active Directory - users/groups](/AD/AD-groups-and-users.png)
  - One of my first times inside, messing around by creating random groups and users.

## Notes / Lessons Learned
- [Server error status?](/AD/AD-server-error.png)
- [I cleared it!](/AD/AD-server-fixed.png)
