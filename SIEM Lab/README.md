# Home Cybersecurity Lab - SIEM with Wazuh

## Overview
This project documents the process of setting up a Security Information and Event Management (SIEM) environment using Wazuh. The goal is to simulate and monitor attack activity within a virtual network lab.

## Lab Topology
- Wazuh Server (SIEM)
- Kali Linux (Attacker with Agent)
- Metasploitable 2 (Victim)
- Ubuntu Server (DNS/DHCP and monitored endpoint)

## Features
- Wazuh all-in-one server deployment
- Agent installation and configuration
- Detection of scanning, brute-force, and exploit activity
- Alerts visible via Wazuh Dashboard

## Requirements
- VirtualBox
- Ubuntu Server ISO
- Kali Linux ISO
- Metasploitable 2 VM
- Wazuh Agent DEB packages

## Key Logs and Screenshots
- `/var/ossec/logs/ossec.log`
- Wazuh Dashboard alert panels

## Next Steps
- Add IDS tools like Suricata or Zeek
- Expand monitored systems (e.g., Windows VM)
- Add custom OSSEC rules
