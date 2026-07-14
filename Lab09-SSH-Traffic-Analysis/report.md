# Investigation Report

## Lab Title

SSH Traffic Analysis Using Wireshark

---

## Investigation Summary

A packet capture containing SSH traffic was analyzed to verify secure remote administration between a Kali Linux client and an Ubuntu server.

The investigation focused on identifying the SSH handshake, version negotiation, key exchange, and encrypted communication.

---

## Network Information

| Item | Value |
|------|-------|
| Source IP | 192.168.1.6 |
| Destination IP | 192.168.1.7 |
| Protocol | SSH |
| TCP Port | 22 |

---

## Evidence Collected

### 1. TCP Connection

A standard TCP three-way handshake was observed before SSH communication began.

Evidence:

- SYN
- SYN-ACK
- ACK

---

### 2. SSH Version Exchange

The client advertised:

```
SSH-2.0-OpenSSH_10.3p1 Debian-5
```

The server responded with:

```
SSH-2.0-OpenSSH_10.2p1 Ubuntu
```

This confirms protocol compatibility before authentication.

---

### 3. Key Exchange

The following packets were identified:

- Key Exchange Init
- Server Key Exchange
- New Keys

These packets establish encrypted communication.

---

### 4. Encrypted Session

Following key exchange, packets appeared as:

```
Encrypted packet
```

Application data is encrypted.

---

## Security Analysis

### Positive Findings

✔ Secure protocol in use

✔ Credentials are encrypted

✔ Session protected using SSH encryption

✔ No plaintext authentication observed

---

### Risks if SSH Were Misconfigured

- Weak passwords
- Password brute-force attacks
- Outdated SSH versions
- Exposed SSH service

---

## SOC Analyst Observations

The remote login followed the expected SSH authentication process.

No plaintext credentials were observed.

Traffic appears consistent with legitimate administrative access.

---

## Conclusion

The investigation confirms that the SSH session was securely established over TCP port 22.

Unlike FTP or Telnet, SSH encrypts authentication and communication, protecting sensitive information from interception.

No suspicious activity was identified during this analysis.
