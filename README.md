# Troubleshoot Default Gateway Issues (Cisco Packet Tracer)

## Project Overview
This project focuses on the methodical troubleshooting of connectivity issues within a multi-subnet network. The primary objective was to verify network documentation, isolate local and remote connectivity problems, and implement IOS configuration solutions to restore end-to-end network integrity.

## Environments and Technologies Used
* Cisco Packet Tracer (Network Simulation) 
* Cisco IOS CLI (Interface Configuration & Verification)
* ICMP Protocol (Connectivity Testing/Troubleshooting) 
* IPv4 Addressing & Subnetting

## Objectives
1. Verify Network Documentation: Complete the addressing table and identify discrepancies between documented and actual configurations.
2. Isolate Problems: Perform local and remote connectivity tests (ping) to pinpoint failure points. 
3. Implement Solutions: Use Cisco IOS commands to correct IP addressing, subnet masks, and default gateways on hosts and switches. 
4. Verify Connectivity: Confirm successful end-to-end communication across all network segments. 

## Addressing Table

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
| :--- | :--- | :--- | :--- | :--- |
| **R1** | G0/0 | 192.168.10.1 | 10.1.1.0 | 10.1.1.1 - 10.1.1.62 | 10.1.1.63 |
| **R1** | G0/1 | 192.168.11.1 | 10.1.1.64 | 10.1.1.65 - 10.1.1.94 | 10.1.1.95 |
| **S1** | VLAN 1 | 192.168.10.2 | 10.1.1.96 | 10.1.1.97 - 10.1.1.110 | 10.1.1.111 |
| **S2** | VLAN 1 | 192.168.11.2 | 10.1.1.112 | 10.1.1.113 - 10.1.1.118 | 10.1.1.119 |
| **PC1** | NIC | 192.168.10.10 | 10.1.1.120 | 10.1.1.121 - 10.1.1.122 | 10.1.1.123 |
| **PC4** | NIC | 192.168.11.11 | 10.1.1.120 | 10.1.1.121 - 10.1.1.122 | 10.1.1.123 |
