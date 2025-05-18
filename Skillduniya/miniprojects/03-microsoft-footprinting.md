# Mini Project 03: Microsoft Footprinting (Passive & Active Recon)

## Summary

Conducted passive and active reconnaissance on **Microsoft Corporation** using common OSINT tools to gather domain, server, DNS, and network-level information. This mini project reflects practical use of footprinting techniques learned during the internship.

---

## Objectives

- Identify publicly available information about Microsoft  
- Gather domain, network, and system-level details  
- Analyze security posture using open-source intelligence (OSINT)  
- Understand the exposure and infrastructure of a global tech company  

---

## Tools Used

- `WHOIS`  
- `Netcraft`  
- `Shodan`  
- `DNSDumpster`

---

## Findings

### 🔍 WHOIS Lookup

- **Domain:** microsoft.com  
- **Registrar:** MarkMonitor, Inc.  
- **Created:** May 2, 1991  
- **Expires:** May 3, 2026  
- **Registrant:** Microsoft Corp, One Microsoft Way, Redmond, WA, US  
- **Name Servers:** Azure DNS - `ns1-39.azure-dns.com`, etc.  
- **Status:** Locked for update/transfer/delete (strong security posture)

---

### 🌐 Netcraft Results

**General Info**  
- Hosting: Microsoft Corporation (US)  
- IPs:  
  - IPv4: `13.107.246.59`  
  - IPv6: `2603:1010:3:3::5b`

**SSL/TLS Security**  
- TLS 1.3 (strong encryption)  
- Issued by Microsoft Azure CA  
- OCSP Stapling: Active  
- No SSLv3 or Heartbleed risks

**Email Security**  
- SPF and DMARC policies strictly enforced  
- DMARC set to "reject"  

**Web Technologies**  
- Backend: ASP.NET (hosted on Azure)  
- Client-side: JavaScript, jQuery  
- Security Headers: HSTS enabled  
- Trackers: Microsoft CDN

---

### 🔎 Shodan Intelligence

**Top Countries (Microsoft infra presence):**  
- US, China, Hong Kong, Germany, Netherlands  

**Top Ports:**  
- 80 (HTTP), 443 (HTTPS), 5985 (WinRM), 135 (RPC), 5357  

**Top Operating Systems:**  
- Windows 10+, Server 2012/2016/2019/2022  

---

### 🧠 DNSDumpster Insights

**Detected Server Technologies:**  
- AkamaiGHost (CDN)  
- Apache  
- Nginx/Ubuntu (test/staging)

**Subdomains & Services:**  
- Akamai-hosted: `a131.ms.a.microsoft.com`  
- Azure-hosted: `publisher-aircapi.1pp.microsoft.com`  
- SMTP: `064-smtp-in-2a.microsoft.com`  
- Ad Services: `adcenter.microsoft.com`  
- Testing: `qa2.acumen.microsoft.com`

**DNS Records:**  
- MX: Outlook.com  
- NS: Azure DNS  
- TXT: SPF, domain verifications (Google, Facebook), marketing tags

---

## Conclusion

Microsoft showcases a **strong external security posture** with modern encryption, strict domain protection, and layered DNS infrastructure. No immediate vulnerabilities were found using passive tools, but due to its high-profile nature, continuous monitoring and professional red teaming are recommended.
