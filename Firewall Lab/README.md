# pfSense Firewall Configuration Lab – Summer 2025

##  Overview
This lab focused on deploying and configuring a **pfSense firewall** within a virtualized environment using VirtualBox. The objective was to understand how perimeter security can be enforced using firewall rules, NAT, and network segmentation. We tested pfSense functionality by isolating network traffic and analyzing how rules impact communication between virtual machines.

---

##  Lab Objectives
- Set up pfSense in VirtualBox with two network interfaces (WAN and LAN).
- Configure firewall rules to restrict and allow traffic between a Kali Linux attacker machine and an Ubuntu server.
- Simulate real-world traffic to verify rule effectiveness.
- Learn to navigate the pfSense web GUI and apply secure firewall policies.

---

##  Lab Setup
| Component          | Configuration Details                            |
|-------------------|---------------------------------------------------|
| **Hypervisor**     | VirtualBox                                       |
| **Firewall**       | pfSense ISO                                       |
| **WAN Interface**  | NAT (connected to internet for updates)          |
| **LAN Interface**  | Internal Network (e.g., `intnet`)                |
| **Client Machine** | Ubuntu Server (Internal Network)                 |
| **Attacker**       | Kali Linux (Internal Network)                    |

---

##  Key Steps Performed
1. Installed pfSense on a VM with two adapters (NAT + Internal).
2. Configured the LAN interface via pfSense console menu.
3. Logged into pfSense web GUI via LAN IP on browser.
4. Set LAN to allow only SSH traffic to Ubuntu server.
5. Denied all other incoming connections to simulate a hardened perimeter.
6. Verified rule effectiveness using Kali machine attempts to connect to blocked services (e.g., HTTP).

---

##  Test Results
-  SSH from Kali to Ubuntu was **allowed**.
-  HTTP and FTP attempts from Kali to Ubuntu were **blocked**.
-  pfSense logs showed clear logs for dropped packets.
-  Internet access from pfSense WAN interface verified.

---

##  Challenges Encountered
- Misconfigured interface assignments during install (resolved by rechecking adapter order).
- Initially locked out from web GUI due to overrestrictive rules.
- Needed to set static IPs correctly in LAN environment for proper routing.

---

##  Key Takeaways
- Learned how pfSense acts as a robust and flexible open-source firewall.
- Practiced creating and ordering rules using the pfSense rule evaluation model (top-down).
- Gained experience in network segmentation and secure perimeter design using virtualization tools.

---

##  Files Included
- `firewall_lab_pfsense_summary.docx` – Full lab report  
  

---

##  Suggestions for Deeper Exploration
- Implement VLANs in pfSense to create segmented subnets.
- Enable pfSense logging and analyze network events.
- Set up Intrusion Detection/Prevention System (IDS/IPS) with Snort or Suricata.
- Configure port forwarding to simulate external access attempts.

---

## Completion Status: Completed 
