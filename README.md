# Real-Network-Traffic-Analysis-using-Wireshark
## Protocol Distribution, Packet Size, and Retransmissions

### Course

Data Communication and Networks

### Assignment Type

Research-Based Assignment

### Tool Used

Wireshark 4.6.4

### Protocols Observed

* ICMP
* ARP
* TCP
* ICMPv6
* MDNS

### Authors

* Aarzoo Gupta
* Aegle

---

# Project Overview

This project presents a detailed packet-level analysis of real network traffic captured using Wireshark within a controlled VirtualBox host-only environment.

The report focuses on:

* Protocol distribution
* Packet-size analysis
* Round-trip time (RTT)
* TCP SYN retransmissions
* Throughput and jitter analysis
* Background protocol behavior

The experiment contains a total of **280 captured packets** observed over approximately **637 seconds**.

---

# Objectives

* Identify and quantify protocol distribution.
* Analyze ICMP latency and RTT.
* Study TCP SYN retransmission behavior.
* Examine ARP cache refresh operations.
* Evaluate throughput, jitter, and packet loss.
* Understand background traffic such as ICMPv6 and MDNS.

---

# Network Topology

The experiment was performed inside a VirtualBox host-only network.

| Device       | IP Address    | Role              |
| ------------ | ------------- | ----------------- |
| Guest VM     | 192.168.198.3 | Traffic Initiator |
| Host Gateway | 192.168.198.1 | Traffic Target    |

---

# Key Findings

## Protocol Distribution

| Protocol | Percentage |
| -------- | ---------- |
| ICMP     | 90.7%      |
| ARP      | 4.3%       |
| TCP      | 3.9%       |
| ICMPv6   | 0.4%       |
| MDNS     | 0.7%       |

---

## ICMP Analysis

* Average RTT remained below 1 ms.
* Zero packet loss observed.
* Stable and low-jitter virtual network communication.

---

## TCP SYN Retransmissions

* SSH connection attempt to port 22 failed.
* Multiple TCP SYN retransmissions observed.
* No SYN-ACK or RST packets received.
* Demonstrates TCP exponential back-off mechanism.

---

## ARP Behavior

* ARP requests and replies indicate healthy address resolution.
* Cache refresh operations observed during communication.

---

## Background Traffic

Additional protocols observed:

* ICMPv6 Router Solicitation
* MDNS printer discovery queries

These packets demonstrate normal operating-system background behavior.

---

# Performance Metrics

| Metric              | Value      |
| ------------------- | ---------- |
| Throughput          | ~3.28 kbps |
| ICMP RTT Session 1  | ~0.28 ms   |
| ICMP RTT Session 2  | ~0.24 ms   |
| Packet Loss         | 0%         |
| TCP Connection Loss | 100% (SSH) |
| Jitter              | < 0.1 ms   |

---

# Technologies Used

* Wireshark 4.6.4
* VirtualBox
* ICMP
* TCP/IP
* ARP
* IPv6
* MDNS

---

# Learning Outcomes

Through this project, we learned:

* Real-time packet capture and analysis
* Protocol filtering using Wireshark
* RTT and latency interpretation
* TCP retransmission analysis
* Network troubleshooting techniques
* Practical understanding of layered network communication

---

# Conclusion

The experiment demonstrates how Wireshark can be used not only for packet observation but also for detailed performance analysis, troubleshooting, and protocol interpretation.

The captured traffic clearly illustrates:

* Efficient ICMP communication
* Reliable local virtual networking
* TCP retransmission behavior
* Background service discovery traffic

This project provides a strong practical understanding of packet-level network analysis.

---

# References

1. Practical Packet Analysis – Chris Sanders
2. TCP Congestion Control (RFC 2581)
3. Wireshark Official Documentation
4. Research papers related to network traffic analysis and intrusion detection

---
