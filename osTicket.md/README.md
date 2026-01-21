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

## High-Level Build Steps
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

## Screenshots
- [Ubuntu - version](/osTicket/osTicket-all-versions.png)
- [Ubuntu - file checksum]()
- [Ubuntu - mid update]()
- [Ubuntu - freshly updated]()
- [osTicket - client screen from Jump box]()
- [osTicket - Admin panel]()

## Lessons Learned

- [Mistakes in bash, oops!]()
- [osTicket admin login DENIED, nooo!]()
- [Maybe resetting the password will work?]()
