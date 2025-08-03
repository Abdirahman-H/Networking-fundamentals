# Networking Fundamentals

This document summarises the key networking concepts I have learned, covering everything from LAN/WAN to DNS, routing, and subnetting.

---

## 1. LAN and WAN
- **LAN (Local Area Network)**:  
  - A network within a small area like a house, office, or building.  
  - Devices are close to each other and can communicate using private IPs.

- **WAN (Wide Area Network)**:  
  - A network spanning large geographical areas, like the Internet.  
  - Connects multiple LANs together using public IP addresses.

---

## 2. OSI Model
The **OSI Model** has 7 layers to explain how data travels between devices:

1. **Physical Layer (Layer 1)** – Transmits raw bits (cables, Wi-Fi, fiber).  
2. **Data Link Layer (Layer 2)** – Uses **MAC addresses** to locate devices locally.  
3. **Network Layer (Layer 3)** – Uses **IP addresses** to route data to the correct network/device.  
4. **Transport Layer (Layer 4)** – Uses **TCP and UDP** to deliver data correctly:  
   - **TCP**: Reliable, checks delivery (websites, emails).  
   - **UDP**: Faster, no confirmation (gaming, streaming).  
5. **Session Layer (Layer 5)** – Maintains active connections between devices.  
6. **Presentation Layer (Layer 6)** – Translates and encrypts data so applications understand it.  
7. **Application Layer (Layer 7)** – What the user interacts with (web browsers, apps).

---

## 3. Ports and Protocols
- **Port**: Like a "door" that directs data to the correct application on a device.  
  - Example: **HTTP → Port 80**, **HTTPS → Port 443**.
- **Protocol**: Rules for how data is communicated and understood.  
  - Examples: **HTTP, HTTPS, FTP, SMTP**.

---

## 4. DNS (Domain Name System)
- **Purpose**: Translates domain names (like `google.com`) into IP addresses.  
- **Name Servers**: Store **DNS records** for domains.  
- **DNS Records**: Provide information about the domain:  
  - **A Record** → Domain → IPv4 Address  
  - **AAAA Record** → Domain → IPv6 Address  
  - **CNAME** → Alias to another domain  
- **Local Host File (/etc/hosts)**: Can resolve names locally before querying DNS.

---

## 5. Routing
- **Routing** decides how data moves from one network to another.  
- **Types of Routing**:  
  1. **Static Routing** – Manually configured paths; does not change automatically.  
  2. **Dynamic Routing** – Routers learn and update paths automatically using protocols.

- **Routing Protocols**:  
  - **OSPF** – Finds the fastest route.  
  - **BGP** – Routes data between ISPs and across the Internet.  

---

## 6. Subnetting and CIDR
- **Subnetting**: Splits a network into smaller sections to improve efficiency.  
- **CIDR (Classless Inter-Domain Routing)**:  
  - Helps allocate IPs efficiently and prevent waste.  
  - Example: `192.168.1.0/24` → 256 addresses in that subnet.

---

## 7. NAT (Network Address Translation)
- Converts **private IPs** (local devices) into a **public IP** (router) so devices can communicate with the Internet.  
- Example: Your phone 192.168.1.10 → Router Public IP → Google.

---

## 8. Networking Tools Learned
- **Ping** – Tests connectivity and packet loss.  
- **Traceroute (tracert)** – Shows the path data takes to reach its destination.  
- **nslookup / dig** – Checks DNS records and IP addresses of domains.

---

## Summary
Through this journey, I’ve learned how data travels:
1. My device sends a request → Router → Public IP → Internet.  
2. DNS translates the domain to an IP.  
3. Data travels through the fastest route using routing protocols.  
4. Ports and protocols ensure it reaches the **right app**, in the **right format**, on the **right device**.

This foundational knowledge is essential for cloud computing, server management, and AWS networking.