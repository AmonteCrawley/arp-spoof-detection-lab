# arp-spoof-detection-lab

**Overview**

This lab demonstrates how ARP works on a local network, how ARP traffic appears in Wireshark, and what ARP spoofing looks like when using Kali Linux tools such as arpspoof

**Tools Used**

- Kali Linux
- Windows 11
- Wireshark
- arpspoof / dsniff
- VMware

**Steps Performed**
**1. Capture ARP Traffic in Wireshark (Windows)**

Wireshark filter used: arp

<img width="2350" height="1279" alt="Screenshot 2025-11-20 155134" src="https://github.com/user-attachments/assets/9737c97e-f436-4b77-9ccc-54143363d08f" />

**2. Run ARP Spoofing Tool on Kali**

Kali using arpspoof to send repeated fake ARP replies.

Command example: sudo arpspoof -i eth1 -t <victim> <gateway>

<img width="2353" height="1315" alt="Screenshot 2025-11-20 160640" src="https://github.com/user-attachments/assets/c30bbfc1-9346-4af0-99cb-4fb962c636e2" />

**Findings**
- Wireshark shows ARP requests and replies clearly.
- ARP spoofing generates repeated unsolicited ARP replies.
- This behavior is typical of MITM attacks.

**MITRE ATT&CK Mapping**
- T1557 – Adversary-in-the-Middle
- T1040 – Network Sniffing

**Summary**
This lab shows how ARP works at a packet level and how ARP spoofing appears during an attack—useful for SOC analysts investigating suspicious network activity.
