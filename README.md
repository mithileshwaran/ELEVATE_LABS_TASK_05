# Wireshark Network Traffic Analysis

## Objective
Capture live network packets and identify basic protocols and traffic types.

## Tools Used
- Wireshark (Free, Open Source)

## Steps Performed
1. Installed Wireshark.
2. Started capture on active network interface.
3. Opened websites to generate traffic (GitHub, etc.).
4. Stopped capture after 1 minute.
5. Applied protocol filters (DNS, TCP, TLS).
6. Saved the capture as `.pcapng`.

## Protocols Identified
1. **DNS** – Used to resolve domain names to IP addresses.
2. **TCP** – Reliable transport protocol for data transfer.
3. **TLSv1.3** – Encryption protocol used in HTTPS communication.

## Sample Packet Details

**Protocol:** DNS  
- Source IP: 192.168.173.241  
- Destination IP: 13.215.86.156  
- Info: Standard query (Malformed Packet)

**Protocol:** TCP  
- Source IP: 192.168.173.241  
- Destination IP: 140.82.114.26  
- Info: TCP SYN to port 443

**Protocol:** TLSv1.3  
- Source IP: 192.168.173.241  
- Destination IP: 140.82.114.26 (SNI = alive.github.com)  
- Info: Client Hello, encrypted communication

## Observations
- DNS queries show the domains I accessed.
- TCP connections established to GitHub servers for HTTPS traffic.
- TLS encrypts the actual data sent between my system and the server.

## Outcome
Gained hands-on experience in capturing and analyzing network packets, identifying protocols, and interpreting packet details.
