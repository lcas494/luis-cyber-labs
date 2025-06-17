# DHCP Server Lab – Cybersecurity Home Lab Project

## Overview

In this lab, I configured and deployed a **dedicated DHCP server** using a virtualized Ubuntu Server on VirtualBox. The goal was to simulate enterprise-level dynamic IP address assignment within a segmented network. This setup mimics how organizations manage host configuration at scale.

## Objectives

- Install and configure a DHCP server on Ubuntu.
- Assign dynamic IP addresses to client machines within an internal VirtualBox network.
- Test IP lease issuance using a Kali Linux client.
- Ensure services persist and function after reboot.

## Lab Setup

### Environment

- **Host Machine**: VirtualBox
- **DHCP Server OS**: Ubuntu Server 22.04.5
- **Client OS**: Kali Linux
- **Network Setup**:
  - Adapter 1: NAT (for updates and internet access)
  - Adapter 2: Internal Network (`intnet`) for isolated DHCP communication

### Configuration Steps

1. Installed Ubuntu Server and verified network adapters.
2. Configured `netplan` to assign a static IP on `enp0s8`.
3. Installed the `isc-dhcp-server` package.
4. Configured the DHCP scope in `/etc/dhcp/dhcpd.conf`:
   - IP range
   - Default gateway
   - DNS server
   - Lease time
5. Set the correct interface in `/etc/default/isc-dhcp-server`.
6. Enabled and started the DHCP service.
7. Verified that the Kali client received an IP address dynamically.

## Challenges Faced

- Netplan YAML indentation errors.
- Connectivity issues due to adapter misconfiguration.
- Package fetch errors caused by DNS misconfiguration.
- Needed to switch NAT/Internal Adapter order for proper communication.

## Outcome

- DHCP server successfully assigned IP addresses to internal clients.
- Kali machine obtained a dynamic IP, verifying functionality.
- Learned how to debug Ubuntu networking and service management.

## Future Enhancements

- Integrate DNS forwarding with DHCP.
- Deploy logging to monitor DHCP requests and leases.
- Explore PXE boot integration for OS deployments.


## Author

Luis C. – Cybersecurity Student | Home Lab Enthusiast
