# Local Network Traffic Analysis with Wireshark

This mini-project documents a beginner network traffic analysis lab using Wireshark. The goal was to build hands-on familiarity with packet capture, display filters, common network protocols, and privacy-aware handling of network data.

All testing was performed on my own machine using controlled traffic and dummy credentials. No unauthorized devices, external networks, or third-party traffic were monitored or analyzed.

## Goals

- Capture and inspect packets using Wireshark
- Identify host, gateway, and DNS traffic
- Observe DNS queries and responses
- Recognize HTTPS traffic over TCP/UDP port 443
- Identify local discovery protocols such as SSDP, mDNS, and LLMNR
- Observe IPv6 network discovery traffic
- Demonstrate how HTTP form submissions can expose cleartext data when encryption is not used
- Export packet metadata and summarize basic traffic patterns with Python/Pandas

## Tools Used

- Wireshark
- Windows Command Prompt
- Python/Pandas
- `ipconfig`
- `nslookup`
- Web browser traffic
- Intentionally vulnerable HTTP test site using dummy credentials

## Packet Metadata Analysis

After capturing traffic in Wireshark, I exported packet metadata as a CSV and used Python/Pandas to summarize basic traffic patterns, including protocol counts, packet lengths, top source/destination labels, and packet volume over time.

This connected packet-level inspection with basic data analysis techniques.

## Data Ethics and Privacy

Because packet captures can contain sensitive information, I avoided publishing raw packet captures. I used only controlled traffic from my own machine, dummy credentials for the HTTP demo, and redacted or replaced sensitive values such as IP addresses, MAC addresses, DNS details, and visible form data.

The analysis focused on metadata such as protocols, packet lengths, timing, and high-level traffic patterns rather than private payload contents.

## Summary

This lab helped me understand how normal network activity appears in packet captures, including DNS resolution, encrypted web traffic, local discovery protocols, IPv6 neighbor discovery, and insecure HTTP form submissions.

The main takeaway was learning to start with a specific question, apply a focused Wireshark filter, and document observations while handling network data responsibly.
