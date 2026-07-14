# Lab 09 – SSH Traffic Analysis Using Wireshark

## Overview

This lab demonstrates how Secure Shell (SSH) traffic appears in Wireshark. Unlike FTP and HTTP, SSH encrypts authentication credentials and session data, making it a secure protocol for remote administration.

The packet capture includes the TCP connection establishment, SSH version exchange, key exchange process, and encrypted communication between a Kali Linux client and an Ubuntu server.

---

## Objectives

- Capture SSH traffic using Wireshark.
- Identify TCP three-way handshake.
- Analyze SSH version exchange.
- Observe SSH key exchange.
- Verify that credentials are encrypted.
- Understand why SSH is preferred over Telnet and FTP.

---

## Lab Environment

| Component | Details |
|-----------|---------|
| Attacker / Client | Kali Linux |
| Server | Ubuntu Server |
| Client IP | 192.168.1.6 |
| Server IP | 192.168.1.7 |
| Protocol | SSH (TCP Port 22) |
| Tool | Wireshark |

---

## Scenario

A SOC analyst receives an alert indicating that an administrator remotely logged into an internal Linux server using SSH.

The analyst captures network traffic to verify:

- Source and destination IP addresses
- SSH protocol version
- Successful key exchange
- Whether credentials are visible
- Whether encrypted communication is used

---

## Wireshark Filter

```
tcp.port == 22
```

---

## Key Findings

- SSH communication uses TCP Port 22.
- TCP three-way handshake completed successfully.
- SSH version exchange observed.
- Key exchange completed.
- Session becomes encrypted immediately after authentication.
- Username and password are not visible.

---

## Skills Practiced

- SSH Traffic Analysis
- Secure Remote Access Investigation
- TCP Analysis
- Protocol Identification
- Encrypted Traffic Analysis
- Wireshark Packet Investigation

---


```

---

## Conclusion

This lab demonstrates how SSH protects remote administrative sessions through encryption. Unlike insecure protocols such as FTP, SSH hides authentication credentials and transmitted data, making it the preferred protocol for secure remote management.
