# Day 14 — Firewall Types & NotebookLM Active Testing

**Date:** <!-- 04/05/2026 -->
**Platform:** Cisco NetAcad — Module 4 | NotebookLM
**Topics:** Firewall Types | Proxy Servers | NAT | 
Host-Based Firewall | NotebookLM Quiz & Flashcards

---

## 🛡️ Firewall Types — Full Breakdown

A firewall is not a single tool. It is a category of
defence with distinct types operating at different
layers of the network stack.

| Firewall Type | OSI Layer | How It Filters |
|---------------|-----------|----------------|
| **Network Layer** | Layer 3 | Source/destination IP addresses |
| **Transport Layer** | Layer 4 | TCP/UDP ports and connection states |
| **Application Layer** | Layer 7 | Actual content and application identity |
| **Context-Aware** | Multiple | User, app, location, behaviour, session context |
| **Host-Based** | Device level | Installed on individual endpoint |

---

### Network Layer Firewall
- Filters traffic based on source and destination IP addresses
- Fast and efficient — operates at packet level
- First line of defence at the network perimeter

### Transport Layer Firewall
- Operates at TCP/UDP level
- Filters based on port numbers and connection states:

| State | Meaning |
|-------|---------|
| NEW | First packet of a new connection |
| ESTABLISHED | Part of an ongoing connection |
| RELATED | Related to an existing connection |

### Application Layer Firewall
- Inspects the actual content of traffic — not just headers
- Can identify and block specific applications regardless
  of which port they use
- Essential for detecting application-layer attacks

### Context-Aware Firewall
- Most intelligent firewall type
- Decisions based on full session context:
  user identity, application, location, behaviour
- Goes beyond packet inspection to behavioural analysis

### Proxy Server
- Acts as intermediary between user and internet
- User never connects directly to external resources
- Adds anonymity, content filtering, and access control

### Reverse Proxy Server
- Sits in front of internal servers
- Handles incoming requests on behalf of those servers
- Protects server identity | Enables load balancing

### Network Address Translation (NAT)
- Maps internal private IP addresses to a single
  public IP address
- Internal device IPs are invisible to the outside world
- Adds a layer of obscurity to internal network structure

### Host-Based Firewall
- Installed directly on an individual endpoint device
- Last line of defence after all network-level controls
- Critical for protecting devices on untrusted networks

---

## 📓 NotebookLM — Active Testing Session

### Quiz Results

**Score: 24/30 — 80%**

| Result | Count |
|--------|-------|
| ✅ Correct | 24 |
| ❌ Wrong | 6 |

**Topics Covered:**
- Wi-Fi Security Protocols
- Password Standards and NIST Guidelines
- Data Persistence and Deletion
- SOC Analyst Career Foundations
- Ethical Decision Making in Business

> 6 questions wrong — all identified for targeted review.
> A score is only useful if the gaps are understood.

---

### Flashcards

**50 flashcards generated from 9 sources**
covering the full week's content.

**Example card reviewed:**
> *True or False: The KRACKs attack targets
> vulnerabilities in specific hardware devices
> rather than the protocol itself.*
>
> **False** — KRACKs targets the WPA2 protocol
> itself. Every device implementing WPA2 is
> potentially affected regardless of manufacturer.

---

### Why Active Testing Matters

| Method | What It Builds |
|--------|---------------|
| Passive reading | Familiarity |
| Active recall (quiz/flashcards) | Retained knowledge |

> Passive reading builds familiarity.
> Active recall builds knowledge.
> One performs under pressure. The other does not.

---

## 📸 Screenshots

### 📘 Cisco — Port Scanning (Module 4.1.5)
![Cisco - Port Scanning](../images/day-14/Cisco.JPG)

### 📓 NotebookLM — Cybersecurity Quiz (24/30 — 80%)
![NotebookLM Quiz Results](../images/day-14/NotebookLM.JPG)

### 📓 NotebookLM — Cybersecurity Flashcards
![NotebookLM Flashcards](../images/day-14/NotebookLM2.JPG)

---

## ✅ Summary
- 7 distinct firewall types — each operating at
  a different layer with a different purpose
- Network/Transport/Application/Context-Aware
  firewalls form layered network defence
- Proxy and Reverse Proxy protect identity
  on both the user and server side
- NAT conceals internal IP structure from
  external networks
- Host-based firewall is the last line of
  defence at the endpoint level
- NotebookLM quiz: 80% — 6 gaps identified
- 50 flashcards across 9 sources — active
  recall now part of the daily study system

---

*[← Day 13](day-13.md) | [Day 15 →](day-15.md)*
