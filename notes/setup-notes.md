Custom Router & Firewall Setup Notes

**This project documents the setup of a virtualized pfSense firewall with dedicated WAN/LAN interfaces and DNS-layer filtering using AdGuard Home.
The goal was to create a lightweight, secure, and flexible home router setup using virtualization (Proxmox) and open-source tooling.

---

Overview

- pfSense - VM installed on Proxmox
- Dedicated NIC passthrough - to separate WAN and LAN interfaces
- NAT and Port Forwarding - for remote access tools
- OpenVPN - configured for secure remote connectivity
- AdGuard Home - running in a companion VM for DNS filtering

---

Setup Highlights

- WAN NIC passed directly to pfSense using Proxmox PCI passthrough  
- LAN NIC bridged to internal VMs and home network  
- Configured:
  - Static IPs
  - DHCP Server on LAN
  - Firewall rules by VLAN
  - NAT rules and VPN port forwarding
- DNS requests filtered through AdGuard VM  
- DNS-over-HTTPS (DoH) planned but not yet implemented

---

To-Do

- [x] Create NAT rules for VPN + remote SSH
- [x] Add static IP mapping to test VMs
- [ ] Upload screenshots of pfSense and AdGuard dashboards
- [ ] Document firewall rules (allow/block by VLAN)
- [ ] Set up remote logs to Wazuh (SIEM integration)

---

Notes

Full documentation and example configurations will be added as project matures.

