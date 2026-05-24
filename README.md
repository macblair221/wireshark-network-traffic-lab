# Local Network Traffic Analysis with Wireshark

This mini-project documents a beginner network traffic analysis lab using Wireshark. The goal was to build hands-on familiarity with packet capture, display filters, and common protocols seen on a local network.

All network testing and packet capturing performed for this project were conducted strictly on my own local machine and controlled testing environments. No external networks, unauthorized devices, or third-party traffic were monitored, intercepted, or analyzed.

## Goals

- Capture and inspect network packets using Wireshark
- Identify my host IP address, default gateway, and DNS server
- Observe DNS queries and responses
- Recognize HTTPS traffic over TCP/UDP port 443
- Identify local discovery protocols such as SSDP, mDNS, and LLMNR
- Recognize IPv6 network discovery and maintenance traffic
- Demonstrate how HTTP form submissions can expose cleartext data in packet captures when encryption is not used

## Tools Used

- Wireshark
- Windows Command Prompt
- `ipconfig`
- `nslookup`
- Web browser traffic
- Intentionally vulnerable HTTP test site
- Dummy credentials for controlled testing


## Packet Metadata Analysis with Python

After capturing traffic in Wireshark, I exported packet metadata as a CSV and used Python/Pandas to summarize basic traffic patterns.

The analysis included:

- Packet counts by protocol
- Top source and destination addresses
- Packet length summary statistics
- Packet volume over time
- Comparison of normal encrypted web traffic and controlled HTTP cleartext form submission traffic

This helped connect packet-level inspection in Wireshark with basic data analysis techniques.
