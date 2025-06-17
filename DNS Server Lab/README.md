# DNS Server Lab

## Lab Overview
This lab involved setting up and configuring a DNS server using BIND9 on an Ubuntu Server VM. The DNS server was integrated into a virtual lab environment to provide internal hostname resolution for client machines.

## Objectives
- Install and configure BIND9 DNS server
- Create and configure a forward lookup zone
- Configure DNS clients to use the new DNS server
- Verify DNS resolution functionality

## Environment
- Host: VirtualBox
- DNS Server: Ubuntu Server 22.04.5
- Client: Kali Linux
- Network:
  - Adapter 1: NAT (Internet access)
  - Adapter 2: Internal Network (DNS resolution)

## Steps Completed
1. Installed BIND9 on the Ubuntu Server.
2. Configured `/etc/bind/named.conf.local` with a forward lookup zone.
3. Created zone files with necessary DNS records.
4. Configured `/etc/bind/named.conf.options` for query permissions.
5. Restarted BIND9 and checked service status.
6. Set client machine’s DNS to point to the server’s internal IP.
7. Tested DNS resolution using `dig` and `nslookup`.

## Challenges
- Initial communication errors to port 53.
- Network interface configuration adjustments.
- DNS resolution troubleshooting on client machine.

## Results
- Internal hostnames resolved correctly on client machines.
- DNS server integrated successfully with DHCP service.

## Future Work
- Add reverse DNS zones (PTR records).
- Implement DNSSEC for security.
- Set up DNS forwarding and caching.

## Author
Luis C.  
Cybersecurity Student & Home Lab Enthusiast
