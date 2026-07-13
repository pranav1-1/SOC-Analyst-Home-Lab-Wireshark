# Lab 2 – ARP & ICMP Investigation

## Objective

To understand how devices discover each other on a local network using ARP and verify network connectivity using ICMP. This lab demonstrates how SOC analysts use Wireshark to investigate network communication and troubleshoot connectivity issues.

---

## Lab Environment

| Device | IP Address |
|----------|------------|
| Kali Linux | 192.168.1.5 |
| Ubuntu Server | 192.168.1.6 |
| Tool | Wireshark |

---

## Protocols Covered

- ARP (Address Resolution Protocol)
- ICMP (Internet Control Message Protocol)

---

## Tasks Performed

- Started packet capture in Wireshark.
- Generated ARP traffic between Kali and Ubuntu.
- Captured ARP Request and ARP Reply packets.
- Generated ICMP traffic using the `ping` command.
- Captured ICMP Echo Request and Echo Reply packets.
- Verified successful communication between both systems.
- Analyzed packet details using Wireshark.

---

## Wireshark Filters Used

```text
arp
```

```text
icmp
```

```text
ip.addr == 192.168.1.5 && ip.addr == 192.168.1.6
```

---

## Key Findings

- ARP successfully resolved the MAC address before communication.
- ICMP Echo Requests received corresponding Echo Replies.
- Network connectivity between Kali and Ubuntu was verified.
- No packet loss or abnormal network behavior was observed.

---

## Skills Learned

- ARP packet analysis
- ICMP packet analysis
- Packet filtering
- Network troubleshooting
- Protocol investigation using Wireshark

---

## Screenshots 
---

## Conclusion

This lab demonstrated how ARP resolves MAC addresses before communication and how ICMP verifies connectivity between hosts. These protocols are essential for SOC analysts when investigating connectivity issues, network reconnaissance, and suspicious network activity.
