# Security Onion

## Purpose
- Network Security Monitoring  + threat detection
- Generate and inspect alerts, logs, and packet data
- Practice “SOC-style” workflows: triage → investigate → document findings

  ## Virtual Machine Specifications (Hyper-V)
 
- The resources I allocated for this virtual machine to run well on the PC.
  - Name: SEC-ONION-01
  - Storage (max/used): 28.14GB / 230GB
  - Memory: 32GB
  - vCPU: 6
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
  - For important files like this, its always a great idea to be careful and match the hash.
- [Security Onion - mid setup](/SecOnion/SO-initial-setup.png)
  - Security Onion takes a long time to set up, I had to get a couple of shots during it.
- [Layered updating](/SecOnion/SO-updating.png)
  - Properly updating Security Onion requires multiple 'sudo soup' commands. Don't forget extra portions of soup!
- [Web interface from Win11 Jump box](/SecOnion/SO-UI-from-Win11Jump.png)
  - Considering the issues I had with installation (an embarassing story I would gladly share), I was very happy to see this screen!
- [Security Onion - dashboard metrics](/SecOnion/SO-main-dashboard.png)
  - I can't pretend to completely understand all of this quite yet, but my intention is mastery.
- [Security Onion - ips and ports report](/SecOnion/SO-ips-and-ports.png)
  - More of the same dashboard. I do have a good grasp on ips and ports in general.

## Lessons / Notes

After initial installation, life kept me away from Security Onion for over a month. When I came back, I couldn't log into the web UI from the jump box. I could not pass MFA. It claimed my authenticator code was incorrect. It wasn't.
- [Not up to date, better fix!](/SecOnion/SO-outdated-error.png)
  - So to begin troubleshooting, I logged into Ubuntu via the Hyper-V console. I discovered it was missing updates.
- [Up to date now, confirmed!](/SecOnion/SO-up-to-date-confirmed.png)
  - After 3 helpings of 'sudo soup', I verified it was up to date. However, the problem persisted. After some investigation I noticed the time zone was incorrect.
- [Time sync is now fixed](/SecOnion/SO-timesync-fixed.png)
  - After manually changing the time in Ubuntu, I was able to log in from the jump box! A classic example of time sensitive MFA being out of sync.
