# Day 19 — Zenmap Port Scan + IDS vs IPS

**Date:** <!-- insert date -->
**Platform:** Cisco NetAcad — Module 4.1.5 & 4.1.7
**Topics:** Port Scanning | Zenmap Hands-On | 
IDS vs IPS | Real Scan Results
**Note:** Nmap installation completed — pending 
practical from Day 17 now done ✅

---

## 💻 Hands-On Lab: Zenmap Intense Scan

### Scan Details

| Field | Value |
|-------|-------|
| **Target** | 10.182.194.10 |
| **Profile** | Intense Scan |
| **Command** | `nmap -T4 -A -v 10.182.194.10` |
| **Scan Duration** | 38.67 seconds |
| **Raw Packets Sent** | 1,030 (46.186KB) |
| **Raw Packets Received** | 1,021 (41.710KB) |

---

### Scan Results

```bash
nmap -T4 -A -v 10.182.194.10
```

| Port | State | Service | Version |
|------|-------|---------|---------|
| **53/tcp** | **OPEN** | domain (DNS) | dnsmasq 2.51 |
| 999 others | CLOSED | — | — |

### Device Profile Revealed

| Detail | Value |
|--------|-------|
| **Device Type** | Phone |
| **OS** | Google Android 9/10/11 (Linux 4.9–4.14) |
| **MAC Address** | 96:08:53:CD:7A:61 (Unknown vendor) |
| **Network Distance** | 1 hop |
| **Host Latency** | 0.0073s — active |
| **TCP Sequence Prediction** | Difficulty=260 |
| **Uptime Guess** | 13.748 days |

---

### Security Analysis of Results

**Port 53 — DNS service open on a phone:**
- `dnsmasq` is a lightweight DNS/DHCP server
- Finding a DNS service running on a mobile device
  is worth investigating — DNS on an endpoint
  rather than a router/server is unusual
- A SOC Analyst would flag this for further review

**999 closed ports:**
- Closed ports are visible but not accessible
- No services running — attack surface minimal
- Significantly better than open ports

**TCP Sequence Prediction — Difficulty=260:**
- Higher difficulty = harder to predict sequence numbers
- Makes TCP session hijacking significantly harder
- "Good luck!" — Nmap's own assessment of the difficulty

---

## 🛡️ IDS vs IPS — Cisco NetAcad 4.1.7

Both are security measures deployed on a network
to detect and prevent malicious activity.
Both scan traffic against a database of rules
and attack signatures.

| System | Position | Action on Detection | Network Impact |
|--------|----------|--------------------| ---------------|
| **IDS** (Intrusion Detection System) | Offline — data mirrored by switch | Log and alert only — no prevention | Minimal — separate from live traffic |
| **IPS** (Intrusion Prevention System) | Inline — sits in traffic path | Actively blocks malicious traffic | Can introduce latency |

### How IDS Works
- Can be a dedicated device, server tool, firewall
  component, or host OS feature
- Scans mirrored traffic against attack signature database
- On match: logs detection and creates alert for
  network administrator
- **Does not prevent** — detects, logs, reports only
- Placed offline to avoid network latency (slowing traffic)

### How IPS Works
- Sits inline between LAN and firewall
- Inspects all traffic in real time
- On match: **actively blocks** the malicious traffic
- Faster response — no human needed to act on alert
- Trade-off: inline position can introduce latency

### SOC Analyst Relevance

> Knowing which system is deployed changes
> how you respond to an alert entirely.
> An IDS alert requires human investigation and action.
> An IPS alert means the threat was already stopped —
> but still requires investigation to understand
> what attempted to get through and why.

---

## 📸 Screenshots

### 📘 Cisco — IDS & IPS (4.1.7)
![Cisco - IDS and IPS](../images/day-19/Cisco.JPG)

### 💻 Zenmap — Intense Scan Results
![Zenmap Scan - 10.182.194.10](../images/day-19/Zenmap.JPG)

### 📘 Cisco — Port Scanning Reference (4.1.5)
![Cisco - Port Scanning](../images/day-19/Port_Scanning.JPG)

---

## ✅ Summary
- Completed pending Nmap/Zenmap installation
  from Day 17 ✅
- Ran intense scan on `10.182.194.10` —
  identified Android phone with DNS service
  on port 53, 999 closed ports
- TCP Sequence Prediction Difficulty=260 —
  session hijacking significantly harder
- IDS: passive — detects, logs, reports only
- IPS: active — detects and blocks in real time
- IDS sits offline to avoid latency |
  IPS sits inline for real-time blocking

---

*[← Day 18](day-18.md) | [Day 20 →](day-20.md)*
