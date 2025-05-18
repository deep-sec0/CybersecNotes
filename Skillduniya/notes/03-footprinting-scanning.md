# Part 3: Footprinting and Scanning

## Footprinting  
Footprinting is the first step in the information gathering phase of ethical hacking and cybersecurity. It involves collecting as much data as possible about a target system or network to identify potential vulnerabilities. The goal is to create a detailed profile of the target by gathering publicly available information.

### Common Footprinting Tools  
Most footprinting tools are online websites or services that help gather data about domains, IPs, and network infrastructure:

- **nslookup:** Retrieves DNS records to find domain-related information like IP addresses.  
- **tracert (traceroute):** Maps the path data packets take to reach a target, showing intermediary routers.  
- **whois:** Provides registration details of domain names and IP blocks, such as owner info and contact.  
- **Netcraft:** Offers detailed information about web servers and hosting details.  
- **Shodan:** A search engine for internet-connected devices, helping find exposed systems and vulnerabilities.  
- **dnsdumpster:** Maps DNS records and related domains to help understand the attack surface.

## Scanning  
Scanning is the next phase, where specific probes are sent to the target to identify open ports, services, and vulnerabilities. It helps in mapping out the target’s network and understanding which entry points can be exploited.

### Types of Scanning  
- **Network Scanning:** Identifies live hosts, devices, and network infrastructure on the target network.  
- **Port Scanning:** Detects open ports and services running on those ports to assess potential vulnerabilities.

### Scanning Tools  
Scanning tools are typically desktop applications downloaded from official websites:

- **Nmap:** A powerful port scanning tool used to discover open ports, running services, and OS detection.  
- **Advanced IP Scanner:** A user-friendly network scanning tool that quickly identifies devices on the local network.

---

Footprinting mainly relies on publicly available online tools, while scanning involves active probing with downloadable applications to gather more in-depth data about the target.
