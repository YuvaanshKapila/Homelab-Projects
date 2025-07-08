# Kali Linux Setup (Pentesting + Network Analysis)

This VM is used for ethical hacking, scanning, and packet analysis in the homelab.

## Network
- Static IP: `192.168.10.3`
- Connected to VirtualBox Host-Only Adapter (GREEN)

## Installed Tools
- `wireshark`: For live packet captures
- `nmap`: Network scanning
- `net-tools`: Includes `ifconfig`
- `metasploit-framework`: Penetration testing suite
- `curl`, `traceroute`, `htop`, and other basic networking utilities

## Use Cases
- Capturing traffic between Ubuntu and Windows VMs
- Running `nmap` scans to test open ports and firewall behavior
- Testing detection of attack patterns on the network

## Screenshot Included
- `wireshark-capture.png`: Capture showing broadcast traffic and port scans
