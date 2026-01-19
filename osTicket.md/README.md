# osTicket (Ubuntu Server)

## Purpose
- Simulate real help desk ticket workflow in a home lab
- Create tickets, manage SLAs, assign agents, and document resolution steps
- Tie into AD users to show identity + support process together (advanced steps for later)

## Lab Context
- **VM Name:** Ubuntu-osTicket
- **OS:** Ubuntu Server 24.04.3 LTS (Noble Numbat)
- **App:** osTicket 
- **Web Stack:** Apache/Nginx + PHP + MariaDB/MySQL
- **Network:** pfSense LAN (10.10.0.0/24)
- **Static IP:** 10.10.0.X

## High-Level Build Steps (Skeleton)
1. Create Ubuntu VM in Hyper-V (CPU/RAM/Disk)
2. Update/upgrade packages
3. Set static IP + DNS
4. Install web stack (Apache/Nginx, PHP modules)
5. Install database (MariaDB/MySQL) + create osTicket DB/user
6. Download/Deploy osTicket files + permissions
7. Configure virtual host + finish web installer
8. Harden basics (updates, firewall rules, remove setup dir)
9. Create admin + agents + departments/teams
10. Configure email piping/inbound + outbound SMTP

## Validation / Evidence (Screenshots coming soon!)
- System info / OS version + IP config
- Web UI accessible from Win11 Jump (screenshot)
- Admin panel showing:
  - Departments/Teams
  - Agents
  - SLAs / Help Topics
- Demo workflow:
  1. Create a ticket
  2. Assign to an agent
  3. Update status/notes
  4. Resolve/close ticket

## Lessons Learned (Coming soon!)
