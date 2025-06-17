# DNS Server Lab – Cybersecurity Home Lab Project

## Overview

This lab focused on configuring a **DNS server** using `BIND9` on a dedicated Ubuntu Server VM in a VirtualBox environment. The project simulated internal name resolution services in an enterprise network, and it was integrated with a previously configured DHCP server.

## Objectives

- Install and configure a DNS server using BIND9.
- Create a forward lookup zone to resolve hostnames to IP addresses.
- Configure internal clients to use the DNS server.
- Verify DNS resolution and troubleshooting techniques.

## Lab Setup

### Environment

- **Host Machine**: VirtualBox
- **DNS Server OS**: Ubuntu Server 22.04.5
- **Client OS**: Kali Linux
- **Network Setup**:
  - Adapter 1: NAT (for updates and internet access)
  - Adapter 2: Internal Network (`intnet`) for DNS testing

### Configuration Steps

1. Installed `bind9` DNS server on Ubuntu.
2. Configured a forward lookup zone file for a local domain (e.g., `cyberlab.local`) in `/etc/bind/named.conf.local`.
3. Created zone file entries in `/var/cache/bind/db.cyberlab.local`:
   - Set up SOA, NS, A records.
4. Updated `/etc/bind/named.conf.options` to allow internal queries.
5. Restarted and verified BIND9 service using:
   ```bash
   sudo systemctl status bind9
Set Kali client’s DNS settings to point to the internal IP of the DNS server.

Verified name resolution using dig and nslookup.

Challenges Faced
Troubleshooting communication errors with port 53.

YAML and interface configuration conflicts from prior DHCP setup.

Needed to adjust /etc/resolv.conf and fix DNS propagation.

Outcome
BIND9 successfully resolved internal hostnames to IP addresses.

DNS requests from the Kali client were handled locally.

Verified full integration with the DHCP server for network service delivery.

Future Enhancements
Add reverse DNS zone (PTR records).

Secure DNS (DNSSEC) implementation.

Internal DNS caching and forwarding to external resolvers.

Explore local domain management for multiple subnets.


Author
Luis C. – Cybersecurity Student | Home Lab Enthusiast
