# Metropolitan Area Network (MAN) Simulation

## Project Overview
[cite_start]This project details the topological design, architecture, and traffic characterization of a Metropolitan Area Network (MAN) using Cisco Packet Tracer[cite: 253]. [cite_start]The primary objective is to build a robust and scalable network connecting two distinct branch offices in a city via an Internet Service Provider (ISP) infrastructure[cite: 254]. 

[cite_start]The design accommodates diverse facility requirements, integrating end-devices, wireless networks, VoIP capabilities, and a dedicated server farm to ensure maximum availability and minimum delay[cite: 255].

## Network Architecture
[cite_start]The network is structured hierarchically, with the backbone consisting of an ISP connecting the edge routers of the two branches[cite: 298]. [cite_start]The architecture spans six separate facilities across the two branches[cite: 275].

### Branch 1
* [cite_start]**Facility 1:** Contains PCs, laptops, and smartphones utilizing Web, Email, and FTP services[cite: 304].
* [cite_start]**Facility 2:** Features dedicated infrastructure for Web, FTP, and a VoIP Conference setup[cite: 304].
* [cite_start]**Facility 3 (Server Farm):** The core service hub containing 10 Web servers, 4 FTP servers, and dedicated DHCP, Mail, and DNS Servers[cite: 304].

### Branch 2
* [cite_start]**Facility 1:** A wireless-heavy environment with laptops, tablets, and PCs for Web and Email access[cite: 306].
* [cite_start]**Facility 2:** Workstations dedicated to Web, App Editing, and FTP file transfers[cite: 306].
* [cite_start]**Facility 3:** Contains PCs and mobile devices configured for remote management and daily Web/Email tasks[cite: 306].

## Key Technologies & Hardware
* [cite_start]**Routing & Switching:** Cisco 2911 Series Routers and 2960 Series Switches[cite: 296].
* [cite_start]**Addressing:** IPv4 scheme with `192.168.X.0/24` for local subnets and `10.0.0.X/30` for WAN links[cite: 316, 317].
* [cite_start]**Application Services:** HTTP, FTP, DNS, DHCP, Mail (SMTP/POP3), and SSH[cite: 256].
* [cite_start]**Real-Time Traffic:** VoIP integration using RTP/SIP and Cisco Call Manager Express (CME)[cite: 308, 512].

## Simulated Traffic Scenarios
[cite_start]Through discrete-event simulation, nine distinct network traffic scenarios were validated[cite: 256]:
1. [cite_start]Wireless Web & Email Access via DHCP and DNS resolution[cite: 326, 329].
2. [cite_start]Cross-branch FTP File Transfers using TCP port 21[cite: 471, 473].
3. [cite_start]VoIP Conference Calls establishing RTP audio streams between IP endpoints[cite: 510, 512].
4. [cite_start]Inter-Branch Email communication using centralized SMTP and POP3 retrieval[cite: 521, 524].
5. [cite_start]ICMP Ping validating end-to-end MAN reachability across the ISP[cite: 637, 640].
6. [cite_start]Wireless Laptop Email transmission using 802.11 Association[cite: 668, 694].
7. [cite_start]SSH Remote Management securely accessing the Web Server gateway on port 22[cite: 697, 700].
8. [cite_start]DNS Domain Resolution & Web Service Access[cite: 725].
9. [cite_start]**Round-Robin DNS Load Balancing:** Distributing traffic seamlessly across 4 redundant FTP servers[cite: 819, 821].

## Team Members
* [cite_start]**Olcay Karahasan** - 2023510056 [cite: 248]
* [cite_start]**Alp Kaya** - 2022510068 [cite: 248]

## How to Run
1. Clone this repository.
2. [cite_start]Ensure you have **Cisco Packet Tracer (ver. 8.2 or compatible)** installed[cite: 892].
3. Open the `.pkt` simulation file included in the repository.
4. Switch to **Simulation Mode** to observe the PDU flow for the 9 defined scenarios.
