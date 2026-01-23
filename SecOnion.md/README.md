# Security Onion

## Purpose
- Network Security Monitoring  + threat detection
- Generate and inspect alerts, logs, and packet data
- Practice “SOC-style” workflows: triage → investigate → document findings

  ## Virtual Machine Specifications (Hyper-V)
 
- The resources I allocated for this virtual machine to run well on the PC.
  - Name:
  - Storage (max/used):
  - Memory:
  - vCPU:
- [Security Onion](/SecOnion/SecOnion-specs.png)

## Lab Context
- **VM Name:** SEC-ONION-01
- **OS:** Security Onion (Oracle Linux-based)
- **Deployment Type:** Standalone
- **Management Interface:** pfSense LAN (10.10.0.0/24)
- **Mgmt IP:** 10.10.0.101
- **Sensor Interface(s):** vSniffer / monitor NIC(s)
- **Traffic Source:** Port mirror/SPAN (virtual switch mirror) or TAP-style feed

## Data Sources / What It Sees
- **Network telemetry:** Zeek
- **IDS alerts:** Suricata
- **Packet capture:** PCAP
- **Logs/search:** Elastic/OpenSearch
- **Analyst UI:** SOC dashboards + Hunt/Query tools

## High-Level Build Steps
1. Create VM in Hyper-V (CPU/RAM/Disk + storage considerations)
2. Add NICs:
   - NIC1 = Management (LAN)
   - NIC2 = Monitor (vSwitch mirror / vSniffer)
3. Install Security Onion + choose **Standalone**
4. Assign mgmt IP + DNS/gateway (pfSense)
5. Configure sensor interface(s) for monitoring (no IP)
6. Confirm services healthy (SO status checks)
7. Configure traffic mirroring in Hyper-V/vSwitch
8. Generate test traffic from Win11 Jump / other VM
9. Validate: alerts/logs/PCAP visibility in the UI

## Screenshots
- [Security Onion - installation file checksum](/SecOnion/SO-hash.png)
- [Security Onion - mid setup](/SecOnion/SO-initial-setup.png)
- [Layered updating](/SecOnion/SO-updating.png)
- [Web interface from Win11 Jump box](/SecOnion/SO-UI-from-Win11Jump.png)
- [Security Onion - dashboard metrics](/SecOnion/SO-main-dashboard.png)
- [Security Onion - ips and ports report](/SecOnion/SO-ips-and-ports.png)

## Lessons / Notes

- [Not up to date, better fix!](/SecOnion/SO-outdated-error.png)
- [Up to date now, confirmed!](/SecOnion/SO-up-to-date-confirmed.png)
- [Time sync is now fixed](/SecOnion/SO-timesync-fixed.png)
