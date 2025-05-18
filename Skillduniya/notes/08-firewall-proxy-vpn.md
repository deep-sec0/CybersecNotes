# 08 - Firewall, Proxy & VPN

## 🔥 Firewall

### What is a Firewall?
A **firewall** is a security system that monitors and controls **incoming and outgoing network traffic** based on predefined rules. It acts as a barrier between trusted internal networks and untrusted external networks (like the internet).

### Architecture:
- Can be hardware-based, software-based, or a combination of both.
- Positioned at the **network perimeter** to control access.

### Types of Firewalls:
- **Packet Filtering Firewall**: Filters traffic based on IP addresses, port numbers, protocols.
- **Circuit-Level Gateway**: Monitors TCP handshakes to ensure valid sessions.
- **Application-Level Gateway (Proxy Firewall)**: Filters traffic at the application layer (e.g., HTTP, FTP).
- **Stateful Multi-Level Inspection Firewall**: Tracks active connections and makes decisions based on state, port, and protocol.

### IDS – Intrusion Detection System:
- Works alongside firewalls.
- Detects suspicious activity and alerts admins but doesn’t block it (unlike IPS).
- Think of it as a **motion detector** for your network.

---

## 🛡️ Proxy & VPN

### What is a Proxy?
A **proxy server** is an intermediary between the user and the internet. It hides your IP address and can filter, log, or cache requests.
- Great for **anonymity**, **content control**, and **performance improvement**.

### What is a VPN (Virtual Private Network)?
A **VPN** encrypts your internet connection and routes it through a secure server, hiding your activity and location.
- Secures data on **public Wi-Fi**.
- Bypasses geo-restrictions and censorship.
- Shields your identity.

### Popular VPN Software:
- **CyberGhost**
- **NordVPN**
- **ProtonVPN**
- **ExpressVPN**

> 🧠 Fun fact: If a firewall is the bouncer, VPN is the disguise, and proxy is your shady friend who knows a backdoor.

