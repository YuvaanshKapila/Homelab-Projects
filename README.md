# Homelab Project

## Overview

This repository documents my personal homelab setup consisting of multiple virtual machines running various services for monitoring, pentesting, malware analysis, and firewall management.

The homelab simulates a realistic small network environment with isolation and observability features.

## Topology
![Screenshot 2025-07-08 043723](https://github.com/user-attachments/assets/0edc0e07-07ac-4822-bf6c-cb9f65509b82)

- **IPFire** acts as the firewall and router controlling traffic between:
  - **WAN**: Connected via VirtualBox NAT
  - **LAN**: Internal Host-Only Network

- **Ubuntu VM**
  - Monitoring tools: Prometheus, Node Exporter, Grafana

- **Kali Linux VM**
  - Pentesting tools: Wireshark, Metasploit, Nmap

- **Windows 10 VM**
  - Malware analysis lab: Process Monitor, Autoruns, Wireshark, EICAR

All VMs communicate securely via the Host-Only Network. Internet access is selectively allowed through IPFire’s NAT interface.

## Virtual Machines

### IPFire

- Role: Firewall and router between WAN and LAN
- Network interfaces:
  - **RED (WAN)**: Connected to NAT
  - **GREEN (LAN)**: Connected to Host-Only Network
- Admin interface: `https://192.168.10.1:444`

### Ubuntu

- Role: Monitoring Server
- Tools:
  - Prometheus → `http://192.168.10.2:9090`
  - Node Exporter → `localhost:9100`
  - Grafana → `http://192.168.10.2:3000`
- Setup:
  - Node Exporter as systemd service
  - Prometheus scraping from Node Exporter

### Kali Linux

- Role: Pentesting and packet analysis
- Tools: Wireshark, Metasploit, Nmap, curl, traceroute
- Network: Host-Only Adapter for internal communication
- Usage: Packet capture, vulnerability scanning

### Windows 10

- Role: Malware analysis environment
- Tools: Process Monitor, Autoruns, Wireshark, Windows Defender, EICAR
- Usage: Controlled malware testing with VM snapshots for rollback

## Documentation Structure

- `ubuntu/`  
  Prometheus config (`prometheus.yml`), Node Exporter service file, setup notes

- `ipfire/`  
  Network setup documentation and screenshots of firewall rules

- `kali/`  
  Installed tools, usage notes, network captures

- `windows/`  
  Malware lab documentation and VM snapshots

## How to Use This Repository

This repository serves as a guide and reference for replicating and learning from a homelab environment. Each subfolder includes config files, screenshots, and setup instructions that can be followed to build your own learning lab.

If you have suggestions or want to collaborate, feel free to reach out.
