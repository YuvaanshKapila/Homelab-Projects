# Ubuntu Monitoring VM Setup

This VM handles system monitoring using Prometheus, Node Exporter, and Grafana.

## Network
- Static IP: `192.168.10.2`
- Connected to VirtualBox Host-Only Adapter (GREEN network via IPFire)

## Installed Tools
- Prometheus (scrapes system metrics)
- Node Exporter (exposes hardware metrics)
- Grafana (dashboarding and visualization)

## Setup Notes
- Node Exporter binary placed in `/usr/local/bin/`
- Custom `node_exporter.service` created in `/etc/systemd/system/`
- Prometheus installed from official binaries
- Configured Prometheus to scrape Node Exporter at `localhost:9100`
- Grafana installed using APT and set up to run on port `3000`

## Web Interfaces
- Prometheus: `http://192.168.10.2:9090`
- Grafana: `http://192.168.10.2:3000`

## Screenshots Taken
- Prometheus target status
- Grafana dashboard showing CPU, RAM, and disk metrics
