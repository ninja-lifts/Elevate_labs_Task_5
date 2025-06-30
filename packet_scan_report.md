#  Network Traffic Analysis Report

This document summarizes the findings from the network traffic capture and highlights the types of protocols used .

---

## Protocols Identified ( I have  added a screenshot of all findings ) 
- Overall 42192 packets were identified including TCP , TLS/SSP , UDP , DNS , HTTP and others.

### Transport Layer Protocols

- **TCP (Transmission Control Protocol - 26440  packets found )**
  Most of the network traffic uses TCP for reliable, connection-oriented communication.

- **ICMPv6( 86 packets found )**  
  Observed in packets , used for IPv6 neighbor discovery.

---

### 💬 Application Layer Protocols

- **TLS/SSL (Transport Layer Security - 15125 packets / Secure Sockets Layer - 196 packets)**  
  Used extensively for encrypted web traffic. Versions found:
  - TLSv1.2 (most common)
  - TLSv1.3 (newer and more secure)
  - SSL (older and less secure)

- **DNS (Domain Name System - 457 packets found)**  
  Seen resolving domain names and reverse lookups.
  - Queries for Google domains and internal addresses.
  - Some IPv6 address queries included.
---

## Specific Protocol Behaviors

###  HTTPS Traffic - 6 Packets found (TLS over TCP Port 443)
- Multiple **TLS handshakes** observed.
- **Encrypted Application Data** exchange after handshake
- **Server Hello** messages confirmed.

### TCP Control Packets 
- **SYN / SYN-ACK / ACK**: used for standard connection establishment.
- **RST** packets observed indicating connection resets.

---

## Notable Observations

- Heavy use of **TLS 1.2**, which is still widely accepted.
- Presence of **TLS 1.3**:  Strong security posture.
- Multiple connections to **HTTPS (port 443)**.
- DNS traffic suggests **web browsing behavior**.
- Some **IPv6** traffic mixed with IPv4.
- TCP connections showed proper 3-way handshakes and terminations.

---

##  Potential Security Notes

- No obvious signs of **malicious activity**.
- TLS 1.3 adoption indicates **modern encryption usage**.
- A few "Ignored Unknown Record" messages.

---
