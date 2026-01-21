# Windows 11 Jump Box

## Purpose
This VM serves as a secure management workstation used to access and administer internal lab systems.

## What I Built
- Centralized admin access point
- RDP/SSH access to internal servers
- Browser-based management (pfSense, osTicket, Security Onion)
- Simulated help desk / IT admin workflow

## Architecture Overview
The Jump Box is the only machine allowed to directly manage sensitive infrastructure components, enforcing a least-privilege model.

## Key Configurations
- Domain-joined
- Admin tools installed
- Hardened access policies

## Screenshots

- [Windows version](/Win11Jump/Win11Jump-OS-Version.png)
- [Machine specs](/Win11Jump/Win11Jump-Specs.png)
- [Active Directory Admin credentials](/Win11Jump/Win11Jump-connected-to-AD.png)
- [Manually setting an IP temporarily](/Win11Jump/Win11Jump-manual-IP.png)

## Lessons / Notes (coming soon)

