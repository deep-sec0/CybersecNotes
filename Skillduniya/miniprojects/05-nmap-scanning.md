# Mini Project 05: Scanning Kali & Windows 7 Systems Using Nmap

## Summary

Used **Nmap** to perform port scanning and network service enumeration on **Kali Linux** and **Windows 7** machines. This mini project demonstrates basic scanning techniques and insights obtained during the analysis.

---

## Objective

- Identify open and closed ports on both systems  
- Determine the services running on those ports  
- Understand privilege requirements and performance impact of different Nmap scans

---

## Target Systems

- **Kali Linux IP:** 10.0.2.15  
- **Windows 7 IP:** 103.127.108.11  

---

## Tool Used

- **Nmap** (Network Mapper)

---

## Scanning Observations

- Nmap can detect:
  - Open, closed, and filtered ports
  - Services bound to specific ports
  - OS fingerprinting (with elevated privileges)
  
- Nmap scans were conducted from the Kali system targeting both itself and the Windows 7 machine.

---

## Considerations

- **Performance:**  
  Scanning **all 65535 ports** takes time. Using targeted scans (e.g., top 1000 ports) improves speed.

- **Privileges:**  
  Some scan types like **SYN scan (-sS)** require **root privileges**.

- **Network Configuration:**  
  The attacker and target machines must be on the **same network segment** or **properly routed**. Misconfigured NAT/bridged adapters can lead to scan failure or false negatives.

---

## Conclusion

Nmap proved highly effective for analyzing both **Kali Linux** and **Windows 7** machines. It revealed the open/closed ports and associated services, helping simulate real-world reconnaissance. Understanding its scanning options and network dependencies is crucial for accurate results.

> “Port scanning is like knocking on every door of a building — you never know which one is unlocked... or loaded.” 🔍🔓

