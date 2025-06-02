# Capture-And-Analyze-Network-Traffic-Using-Wireshark
Task 5

# Network Traffic Analysis with Wireshark

Capture live network traffic using Wireshark and analyze protocols and traffic types. This project provides a `.pcapng` capture file and a summarized report of the network protocols observed.

---

## Tools Used:

- [Wireshark](https://www.wireshark.org/) – Free network protocol analyzer

---

## Steps Performed:

1. **Installed Wireshark** on the laptop.
2. **Started live capture** on the active network interface (Wi-Fi).
3. **Generated traffic** by:
   - Visiting `google.com`
   - Running `ping google.com` in the terminal
4. Captured packets for **1 minute**.
5. Applied protocol filters to analyze:
   - TCP
   - DNS
   - ICMPv6
6. **Saved capture** as: `network_packet_capture.pcapng`
7. Summarized findings below.
---
## Capture File:

- **Filename**: `network_packet_capture.pcapng`
---
## Packet Details:

### TCP Packet
- Source IP: 34.54.255.56
- Destination IP: 192.168.125.252
- Source Port: 443
- Destination Port: 52692
- Flags: ACK

### DNS Packet
- Query: Standard query
- Response: 0xb37a AAAA google.com AAAA 2404:6800:4009:805::200e
- Protocol: User Datagram Protocol, Source Port: 53, Destination Port: 55568

### ICMPv6 Packet
- Type: 135 (Neighbor Solicitation)
- Source IP: 2401:4900:1889:82e1:7862:1e49:66e7:c299
- Destination IP: 2404:6800:4009:805::200e
- Info: Who has 2401:4900:1889:82e1:7862:1e49:66e7:c299?

## Protocols Identified:

| Protocol | Description                     | Observations |
|----------|----------------------------------|--------------|
| **TCP** | Transmission Control Protocol      | Used for HTTP communication, observed 3-way handshake and data segments |
| **DNS**  | Domain Name System               | Standard queries for `google.com` |
| **ICMPv6** | Internet Control Message Protocol for IPv6 | `ping` command generated ICMPv6 Echo Requests and Replies |

---
