# Security Onion (SO-01)

## Purpose
- Network Security Monitoring (NSM) + detection lab
- Generate and inspect alerts, logs, and packet data
- Practice “SOC-style” workflows: triage → investigate → document findings

## Lab Context
- **VM Name:** SO-01 (or your actual VM name)
- **OS:** Security Onion (Oracle Linux-based)
- **Deployment Type:** Standalone (most common for home labs)
- **Management Interface:** pfSense LAN (10.10.0.0/24)
- **Mgmt IP:** 10.10.0.X
- **Sensor Interface(s):** vSniffer / monitor NIC(s) (no IP)
- **Traffic Source:** Port mirror/SPAN (virtual switch mirror) or TAP-style feed

## Data Sources / What It Sees
- **Network telemetry:** Zeek
- **IDS alerts:** Suricata
- **Packet capture:** PCAP
- **Logs/search:** Elastic/OpenSearch (depends on your SO version)
- **Analyst UI:** SOC dashboards + Hunt/Query tools

## High-Level Build Steps (Skeleton)
1. Create VM in Hyper-V (CPU/RAM/Disk + storage considerations)
2. Add NICs:
   - NIC1 = Management (LAN)
   - NIC2 = Monitor (vSwitch mirror / vSniffer)
3. Install Security Onion + choose **Standalone**
4. Assign mgmt IP + DNS/gateway (pfSense)
5. Configure sensor interface(s) for monitoring (no IP)
6. Confirm services healthy (SO status checks)
7. Configure traffic mirroring in Hyper-V/vSwitch (if applicable)
8. Generate test traffic from Win11 Jump / other VM
9. Validate: alerts/logs/PCAP visibility in the UI

## Validation / Evidence (Screenshots Later)
- SO console showing interfaces + IP config
- Web UI login page + main dashboard
- Zeek data visible (connections/http/dns depending on traffic)
- Suricata alerts appearing (even basic test alerts)
- Hunt/Query example (search by src/dst IP, DNS query, HTTP host)
- PCAP drilldown example for one event

## Demo Scenarios (Add Later)
- Basic port scan detection (from Jump box)
- Suspicious DNS / blocked domain example
- HTTP download + PCAP follow-stream investigation
- “SOC Note” style writeup: what happened + evidence + conclusion

## Notes / Lessons Learned (Optional)
- Resource tuning (RAM/CPU/storage) and performance observations
- Anything tricky about vSwitch mirroring / vSniffer NIC setup
- What you’d improve next (more sensors, VLAN visibility, Sysmon/endpoint logs, etc.)
