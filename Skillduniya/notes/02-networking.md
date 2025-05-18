# Part 2: Networking Basics for Cybersecurity

## Protocols  
Protocols are standardized rules that allow computers to communicate over networks. They define how data is formatted, transmitted, and received to ensure smooth and reliable communication. Common protocols include TCP (Transmission Control Protocol), UDP (User Datagram Protocol), HTTP (Hypertext Transfer Protocol), and FTP (File Transfer Protocol). Understanding these is essential for anyone diving into cybersecurity.

## IP Addresses  
An IP address is a unique identifier assigned to each device on a network. It works like a digital address, allowing devices to find and communicate with each other.

- **Public IP Address:** This is your device’s unique address on the internet, visible to the outside world.  
- **Private IP Address:** Used within local networks (like your home or office), these addresses aren’t visible externally but allow devices to communicate internally.

### Versions of IP  
- **IPv4:** The most widely used version, IPv4 uses 32-bit addresses (e.g., 192.168.1.1). It supports around 4 billion unique addresses but is running out due to the internet’s growth.  
- **IPv6:** Developed to solve IPv4’s limitations, IPv6 uses 128-bit addresses, allowing for a vast number of unique IPs. It’s becoming increasingly important as more devices connect to the internet.

## Ports: Physical and Virtual  
- **Physical Ports:** These are the actual hardware interfaces on your device, such as Ethernet ports or USB connectors, where cables plug in.  
- **Virtual Ports:** These are logical endpoints for network communication inside a device, represented by numbers from 1 to 65535. They allow multiple applications to use network connections simultaneously.

### Important Port Numbers and Their Services  
- **80:** HTTP (web browsing)  
- **443:** HTTPS (secure web browsing)  
- **21:** FTP (file transfers)  
- **22:** SSH (secure remote login)  
- **53:** DNS (domain name resolution)

## OSI Model Overview  
The OSI (Open Systems Interconnection) model is a conceptual framework that divides network communication into seven layers:

1. **Physical:** Transmission of raw bits over physical media.  
2. **Data Link:** Node-to-node data transfer and error detection.  
3. **Network:** Routing and forwarding of data packets (IP operates here).  
4. **Transport:** Reliable data transfer and flow control (TCP and UDP protocols).  
5. **Session:** Managing sessions between applications.  
6. **Presentation:** Data translation, encryption, and compression.  
7. **Application:** High-level APIs and user interfaces (e.g., browsers, email clients).

For beginners, focus mainly on the first four layers, as they form the foundation of network communication and security concepts.
