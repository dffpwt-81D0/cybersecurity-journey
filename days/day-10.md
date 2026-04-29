# Day 10 — Wi-Fi Security, Passwords, Encryption & Data Privacy

**Date:** <!-- 29/04/2026 -->
**Platform:** Cisco NetAcad — Module 3: Protecting Your Data and Privacy
**Topics:** Wi-Fi Encryption | SSID | KRACKs | Bluetooth | 
Passphrases | NIST SP 800-63 | Deleted Files

---

## 📡 Wi-Fi Security

### SSID & Encryption
- **SSID** — the name that identifies a Wi-Fi network
- Wi-Fi networks are protected by encryption protocols 
  such as WPA2 to secure transmitted data

### KRACKs — Key Reinstallation Attacks
Discovered by Mathy Vanhoef, KU Leuven, 2017.

| Detail | Description |
|--------|-------------|
| **Method** | Forces nonce reuse in WPA2 handshake |
| **Impact** | Decrypts traffic assumed to be safely encrypted |
| **Scope** | Every device supporting Wi-Fi — Android, Linux, Apple, Windows |
| **Risk** | Steal credentials, inject ransomware or malware |

> The weakness is in the Wi-Fi standard itself —
> not individual products or implementations.
> If your device supports Wi-Fi, it is most likely affected.

### Wireshark Demonstration
A captured session showed a user opening a browser and 
attempting to create an account. The username and password 
typed appeared in **plain text** within the captured traffic.
The user had no indication their credentials were visible.

### Bluetooth
Attackers can exploit Bluetooth connections to access 
devices — physical proximity is the only requirement.

---

## 🔑 Passwords & Passphrases

### Passphrase Advantage
Using special characters within a passphrase significantly 
increases resistance to brute force and dictionary attacks 
compared to conventional short passwords.

### NIST Digital Identity Guidelines — SP 800-63
The federal standard governing password creation, 
management, and enforcement at an organisational level.

| Document | Title |
|----------|-------|
| SP 800-63-3 | Digital Identity Guidelines |
| SP 800-63A | Enrollment and Identity Proofing |
| SP 800-63B | Authentication and Lifecycle Management |
| SP 800-63C | Federation and Assertions |

> Note: SP 800-63-3 has been superseded by 
> NIST SP 800-63-4 as of August 1, 2025.

---

## 🗑️ Deleted Files — A Hidden Vulnerability

When a file is permanently deleted from a system:
- It is **removed from the operating system's index**
- It **remains physically on the hard disk**
- It is inaccessible through normal means but 
  **fully recoverable with the right tools**

| Deletion Method | Data Actually Gone? |
|----------------|-------------------|
| Empty Recycle Bin | ❌ No — still on disk |
| Shift + Delete | ❌ No — still on disk |
| Format drive | ❌ No — largely recoverable |
| **Physical destruction** | ✅ Yes — only guaranteed method |

> Any device that has stored sensitive data carries 
> this risk until the hardware is physically destroyed.

---

## 📸 Screenshots

### 📡 KRACKs — Key Reinstallation Attacks
![KRACKs Introduction](../images/day-10/KRACKs.JPG)
![KRACKs Wireshark Demo](../images/day-10/KRACKs2.JPG)

### 📘 Cisco NetAcad — Module 3.3 Terms of Service
![Cisco Module 3 - Who Owns Your Data](../images/day-10/Cisco.JPG)

### 🔑 NIST Password Regulations
![NIST Digital Identity Guidelines SP 800-63](../images/day-10/NIST_Password_Regulations.JPG)

### 📡 FCC — Wi-Fi Access Security Tips
![FCC Wireless Connections Security](../images/day-10/Wi-Fi_Access.JPG)

---

## ✅ Summary
- KRACKs breaks WPA2 by forcing nonce reuse — 
  affects every Wi-Fi capable device globally
- Wireshark can capture credentials in plain text 
  on unprotected or compromised networks
- Bluetooth is an active attack surface — 
  proximity is the only barrier
- NIST SP 800-63 governs password standards 
  at a federal and organisational level
- Permanently deleted files remain on hard disk 
  until physical destruction of the hardware

---

*[← Day 9](day-09.md) | [Day 11 →](day-11.md)*
