# IPFire Network Configuration

This VM is acting as the main firewall and router for the homelab network.

## Network Roles
- RED (WAN): Connected to VirtualBox NAT — gets internet via DHCP
- GREEN (LAN): Connected to VirtualBox Host-Only Network — acts as LAN gateway

## Interface Details
- RED Interface: `dhcp` from VirtualBox NAT
- GREEN Interface: Static IP `192.168.10.1`
- DHCP Server: Enabled on GREEN — range `192.168.10.100–192.168.10.200` (optional, I set static IPs instead)

## Web UI Access
- Accessed from other VMs at: `https://192.168.10.1:444`
- Default admin user changed and password secured

## Notes
- Packet filtering and NAT rules configured to allow outbound traffic
- Firewall rules screenshot shows basic configuration to allow all outbound from GREEN

## Screenshot Included
- `firewall-rules.png`
