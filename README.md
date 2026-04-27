# Troubleshoot Default Gateway Issues (Cisco Packet Tracer)
<img width="284" height="292" alt="image" src="https://github.com/user-attachments/assets/286a47e0-0066-4db8-a70b-62d8f7b1c440" />

## Project Overview
This project focuses on the methodical troubleshooting of connectivity issues within a multi-subnet network. The primary objective was to verify network documentation, isolate local and remote connectivity problems, and implement IOS configuration solutions to restore end-to-end network integrity.

## Environments and Technologies Used
* Cisco Packet Tracer (Network Simulation) 
* Cisco IOS CLI (Interface Configuration & Verification)
* ICMP Protocol (Connectivity Testing/Troubleshooting) 
* IPv4 Addressing & Subnetting

## Objectives
**1. Verify Network Documentation**: Complete the addressing table and identify discrepancies between documented and actual configurations.

**2. Isolate Problems**: Perform local and remote connectivity tests (ping) to pinpoint failure points. 

**3. Implement Solutions**: Use Cisco IOS commands to correct IP addressing, subnet masks, and default gateways on hosts and switches. 

**4. Verify Connectivity**: Confirm successful end-to-end communication across all network segments. 

## Addressing Table
<img width="611" height="290" alt="image" src="https://github.com/user-attachments/assets/70735ad5-cfcc-49f8-bf24-cd47b598ee0d" />

## Troubleshooting & Verification Documentation
<img width="606" height="390" alt="image" src="https://github.com/user-attachments/assets/576d37f3-8d00-4ac5-833c-2764336018b3" />

## Troubleshooting & Configuration Steps

**Step 1: Resolving Local IP Conflicts**
* **Issue**: PC1 could not ping PC2 because it was misconfigured with IP 192.168.10.11 (a conflict with PC2). 
  * **Action**: Re-configured PC1 with the documented address 192.168.10.10. 
  * **Result**: Restored local connectivity on the 192.168.10.0/24 subnet.
 <img width="417" height="330" alt="image" src="https://github.com/user-attachments/assets/b2ba095c-e49c-4d64-8649-53a020d6d137" />

*PC1 Ping to PC2- Successful*

Step 2: Correcting Host Default Gateways
* Issue: PC4 could not reach remote subnets because its gateway was set to 192.168.1.1 (incorrect subnet). 
* Action: Updated PC4 Default Gateway to 192.168.11.1. 
* Result: Enabled PC4 to route traffic to the R1 G0/1 interface for remote communication.
*  <img width="422" height="330" alt="image" src="https://github.com/user-attachments/assets/541cb1bf-55e7-4989-b403-3605ebd28e91" />: PC4 Ping to PC1- Successful

Step 3: Switch Management & Gateway Configuration
* Issue: S1 and S2 were unreachable from remote subnets, and S2 was missing its management IP. 
* Configuration (S2):
<img width="440" height="124" alt="image" src="https://github.com/user-attachments/assets/dbdb4101-8d55-4cc5-a224-905b1a37c242" />

* Configuration (S1):
<img width="436" height="71" alt="image" src="https://github.com/user-attachments/assets/b7d8bcf8-f843-4cc4-afbe-1bf482711032" />
* Result: Full management reachability and 100% lab completion verified via ICMP.
* <img width="1283" height="131" alt="image" src="https://github.com/user-attachments/assets/9e290713-857d-47dc-8bf3-565d99b696d0" />

