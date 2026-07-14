# Lab 10 – DHCP Traffic Analysis Using Wireshark

## Overview

This lab demonstrates how the Dynamic Host Configuration Protocol (DHCP) automatically assigns IP addresses to devices on a network. Using Wireshark, DHCP packets were captured and analyzed to understand the complete IP address allocation process.

The packet capture includes the DHCP DORA process (Discover, Offer, Request, Acknowledgment), which is the standard method used by DHCP clients to obtain network configuration.

---

## Objectives

- Capture DHCP traffic using Wireshark.
- Understand the DHCP DORA process.
- Identify DHCP packet types.
- Analyze automatic IP address assignment.
- Learn how DHCP assists network administration.
- Practice identifying DHCP traffic from a SOC analyst's perspective.

---

## Lab Environment

| Component | Details |
|-----------|---------|
| Client | Kali Linux |
| DHCP Server | Router / Ubuntu DHCP Server |
| Protocol | DHCP |
| UDP Ports | 67, 68 |
| Tool | Wireshark |

---

## Scenario

A SOC analyst investigates whether a newly connected device successfully obtained an IP address from the DHCP server.

The objective is to verify:

- DHCP Discover packet
- DHCP Offer response
- DHCP Request packet
- DHCP Acknowledgment (ACK)
- Assigned IP address
- DHCP Server Identifier

---

## Wireshark Filter

```
dhcp
```

or

```
bootp
```

---

## DHCP DORA Process

1. DHCP Discover
2. DHCP Offer
3. DHCP Request
4. DHCP ACK

---

## Key Findings

- DHCP communication uses UDP ports 67 and 68.
- The client broadcasts a DHCP Discover message.
- The DHCP server offers an available IP address.
- The client requests the offered address.
- The server acknowledges the request and assigns the IP.

---

## Skills Practiced

- DHCP Analysis
- Network Troubleshooting
- IP Address Allocation Analysis
- Packet Inspection
- SOC Network Monitoring
- Wireshark Investigation

---

```

---

## Conclusion

This lab demonstrates the DHCP DORA process used to automatically assign IP addresses to network devices. Understanding DHCP traffic enables SOC analysts to troubleshoot IP assignment issues, detect rogue DHCP servers, and monitor network behavior effectively.
