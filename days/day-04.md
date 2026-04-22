# Day 4 — Hardware Vulnerabilities, Ports, Protocols & DNS

**Date:** <!-- insert date -->
**Platform:** Cisco NetAcad — Module 2.3 | Gemini Cybersecurity Teacher Gem
**Topics:** Hardware Vulnerabilities | Ports & Protocols | DNS | netstat Lab

---

## 🔩 Hardware Vulnerabilities

| Vulnerability | Method | Impact |
|---------------|--------|--------|
| **Rowhammer** | Hammers RAM rows to cause electrical interference | Corrupts neighbouring memory data |
| **Meltdown** | Side-channel attack on CPU | Reads all memory from a given system |
| **Spectre** | Side-channel attack on CPU | Reads data across applications |

> Meltdown & Spectre affect virtually every CPU since 1995 —
> desktops, servers, smartphones, and cloud infrastructure.

---

## 🚪 Ports & Protocols
- **Port** — a virtual door on a device where network traffic 
  enters and exits. 65,535 possible ports per device.
- **Protocol** — the rules governing how communication happens 
  through that port (e.g. HTTPS on port 443)
- SOC Analysts must recognise standard port/protocol pairs — 
  unexpected port usage is an immediate indicator of suspicious activity.

---

## 📖 DNS — Domain Name System
Translates human-readable domain names into IP addresses.

**Why it matters for security:**
- **DNS Poisoning** — corrupts DNS cache to redirect users
- **DNS Hijacking** — redirects queries to malicious servers  
- **DNS Tunnelling** — uses DNS traffic to exfiltrate data covertly

---

## 💻 Hands-On Lab: netstat

```bash
netstat -an
```

| State | Meaning |
|-------|---------|
| **LISTENING** | Port open, awaiting connection |
| **ESTABLISHED** | Active connection in progress |
| **TIME_WAIT** | Connection closing, ensuring all packets delivered |

**Observed:** Multiple ESTABLISHED connections to external IPs 
over port 443 (HTTPS) — real traffic on a real system.
First time all week's theory became directly observable 
in a single command output.

---

## 📸 Screenshots
![Cisco - Hardware Vulnerabilities](../images/day-04/Cisco.jpg)
![CMD - netstat output](../images/day-04/cmd.jpg)
![Gemini - DNS](../images/day-04/Gemini1.jpg)
![NotebookLM 6-months Roadmap](../images/day-04/NotebookLM.jpg)

---

## ✅ Summary
- Rowhammer, Meltdown & Spectre — hardware-level attack vectors
- Ports = network doors | Protocols = communication rules
- DNS translates domains to IPs and is actively exploited by attackers
- `netstat -an` reveals live TCP connections, ports, and states

---
*[← Day 3](day-03.md) | [Day 5 →](day-05.md)*
