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
| **R1** | G0/0 | 192.168.10.1 | 255.255.255.0 | N/A | 
| **R1** | G0/1 | 192.168.11.1 | 255.255.255.0 | N/A | 
| **S1** | VLAN 1 | 192.168.10.2 | 255.255.255.0 | 192.168.10.1 | 
| **S2** | VLAN 1 | 192.168.11.2 | 255.255.255.0 | 192.168.11.1 | 
| **PC1** | NIC | 192.168.10.10 | 255.255.255.0 | 192.168.10.1 | 
| **PC4** | NIC | 192.168.11.11 | 255.255.255.0 | 192.168.11.1 |

## Troubleshooting & Configuration Steps

Step 1: Resolving Local IP Conflicts

* ** Issue: PC1 could not ping PC2 because it was misconfigured with IP 192.168.10.11 (a conflict with PC2). 
* ** Action: Re-configured PC1 with the documented address 192.168.10.10. 
* ** Result: Restored local connectivity on the 192.168.10.0/24 subnet.
