#  Networking Cheatsheet

A quick-reference guide to essential networking concepts.

---

##  Network Models

### OSI Model (7 Layers)
| Layer | Name             | Function                         | Example Protocols      |
|-------|------------------|----------------------------------|------------------------|
| 7     | Application      | User interface                   | HTTP, FTP, DNS         |
| 6     | Presentation     | Data format/Encryption           | SSL/TLS, JPEG          |
| 5     | Session          | Connection management            | NetBIOS, PPTP          |
| 4     | Transport        | Reliable delivery                | TCP, UDP               |
| 3     | Network          | Routing, IP addressing           | IP, ICMP               |
| 2     | Data Link        | MAC addressing, switching        | Ethernet, ARP          |
| 1     | Physical         | Cables, radio, and signals       | Ethernet cables, Wi-Fi |

---

##  Common Protocols & Ports

| Port | Protocol | Description            |
|------|----------|------------------------|
| 21   | FTP      | File Transfer Protocol |
| 22   | SSH      | Secure Shell           |
| 23   | Telnet   | Remote access (insecure)|
| 25   | SMTP     | Email Sending          |
| 53   | DNS      | Domain Name Resolution |
| 80   | HTTP     | Web Traffic            |
| 110  | POP3     | Email Retrieval        |
| 143  | IMAP     | Email Retrieval        |
| 443  | HTTPS    | Secure Web Traffic     |
| 3389 | RDP      | Remote Desktop         |

---

##  TCP vs UDP

| Feature             | TCP                         | UDP                        |
|---------------------|-----------------------------|----------------------------|
| Connection Type     | Connection-oriented         | Connectionless             |
| Reliability         | Reliable, guaranteed        | Unreliable, best-effort    |
| Speed               | Slower due to overhead      | Faster, lightweight        |
| Use Cases           | Web, Email, File Transfer   | Streaming, DNS, VoIP       |

---

##  Subnetting Quick Guide

- Class A: `1.0.0.0 – 126.0.0.0` /8  
- Class B: `128.0.0.0 – 191.255.0.0` /16  
- Class C: `192.0.0.0 – 223.255.255.0` /24  
- Private IP ranges:
  - `10.0.0.0/8`
  - `172.16.0.0/12`
  - `192.168.0.0/16`

---

##  Nmap Cheat Sheet

```bash
nmap -sV -T4 -Pn 10.10.10.10     # Version scan
nmap -sC -sV -oN scan.txt TARGET # Default scripts & versions
nmap -p- -T4 TARGET              # Scan all 65535 ports
```
## Wireshark filters
```bash
ip.addr == 192.168.1.5
tcp.port == 80
http.request
dns
tcp.flags.syn == 1 and tcp.flags.ack == 0  # TCP SYN packets
