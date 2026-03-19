Wireshark Traffic Analysis Lab

Author: Mark Gutierrez

--------------------------------------------------

OVERVIEW:

This lab demonstrates the use of Wireshark to capture and analyze network traffic in a controlled lab environment. The focus is on identifying and understanding key network protocols including ICMP, DNS, and TCP/TLS.

The lab simulates real-world troubleshooting scenarios by generating traffic and analyzing packet-level communication.

--------------------------------------------------

OBJECTIVES:

- Capture live network traffic using Wireshark
- Apply display filters to isolate specific protocols
- Analyze ICMP, DNS, and TCP/TLS traffic
- Understand packet flow and communication between hosts

--------------------------------------------------

ENVIRONMENT:

- Windows 10 Client (VirtualBox)
- Windows Server 2022 Domain Environment
- Wireshark (latest version)
- Internal virtual network

--------------------------------------------------

LAB ACTIVITIES:

1. ICMP Traffic Analysis

- Generated traffic using the ping command
- Captured ICMP packets in Wireshark
- Applied filter: icmp

Identified:
- Echo Request
- Echo Reply

Outcome:
Verified network connectivity between client and external host (8.8.8.8).

--------------------------------------------------

2. DNS Traffic Analysis

- Generated traffic by accessing websites
- Captured DNS queries and responses
- Applied filter: dns

Observed:
- Domain name queries (e.g., google.com)
- DNS server responses with IP addresses

Outcome:
Demonstrated domain name resolution process.

--------------------------------------------------

3. TCP/TLS Traffic Analysis

- Generated traffic by browsing web applications
- Captured TCP and TLS packets
- Applied filter: tcp || tls

Observed:
- TCP handshake behavior
- Encrypted TLS communication

Outcome:
Analyzed application-layer traffic and secure communication.

--------------------------------------------------

KEY CONCEPTS DEMONSTRATED:

- Packet capture and analysis
- Protocol filtering (ICMP, DNS, TCP, TLS)
- Network troubleshooting methodology
- Request/response communication flow
- Encrypted vs unencrypted traffic

--------------------------------------------------

TOOLS USED:

- Wireshark
- Command Prompt (ping)
- Web browser (traffic generation)

--------------------------------------------------

FINDINGS:

- ICMP traffic confirmed successful connectivity between hosts
- DNS traffic showed domain resolution to IP addresses
- TCP/TLS traffic demonstrated secure web communication
- Filtering techniques improved visibility into specific network behaviors

--------------------------------------------------

NOTES:

- Internal IP addresses and MAC addresses have been partially masked for privacy
- Traffic was generated in a controlled lab environment

--------------------------------------------------

CONCLUSION:

This lab demonstrates practical, hands-on experience with network traffic analysis using Wireshark. It highlights the ability to capture, filter, and interpret packet data, which is essential for troubleshooting and understanding network communication in real-world IT environments.
