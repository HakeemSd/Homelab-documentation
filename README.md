# Homelab
Self-hosted Ubuntu homelab, that includes Docker, Jellyfin , and system administration projects, networking, and automation.


# About

The purpose of this homelab is to gain practical experience with:

- Linux Administration
- Docker & Docker Compose
- Networking 
- Self-Hosting Applications
- Bash Scripting
- System Automation
- Remote Server Management
- Monitoring & Logging
- Media Streaming

  # Hardware

| Component | Details |
|-----------|---------|
| Mini PC | Qotom Fanless Mini PC |
| CPU | Intel Celeron J1900 (Quad-Core, 2.0 GHz, up to 2.42 GHz) |
| RAM | 8 GB DDR3L |
| Storage | 128 GB SSD |
| Network | 4× Gigabit Ethernet |
| Cooling | Fanless Aluminum Chassis |
| Operating System | Ubuntu Desktop 24.04 LTS |


# Services

## Installed

- Ubuntu Desktop 24.04 LTS
- OpenSSH Server
- NoMachine
- Cockpit
- Docker
- Docker Compose
- Portainer
- Jellyfin
- Tailscale
- Homepage Dashboard
- Sonarr
- Radarr
- Prowlarr

## Planned

- qBittorrent
- Grafana
- Prometheus
- Watchtower
- Nginx Proxy Manager

# Repository Structure

homelab/
│
├── docs/
│   ├── ubuntu-install.md
│   ├── ssh-setup.md
│   ├── docker.md
│   ├── jellyfin.md
│   ├── networking.md
│   ├── cockpit.md
│   └── troubleshooting.md
│
├── docker/
│   ├── jellyfin/
│   ├── portainer/
│   ├── homepage/
│   └── docker-compose.yml
│
├── scripts/
│   ├── backup.sh
│   ├── update.sh
│   ├── cleanup.sh
│   └── health-check.sh
│
├── diagrams/
│
├── screenshots/
│
└── README.md


# Goals

- Build a complete self-hosted media server
- Learn Linux system administration
- Gain hands-on Docker experience
- Improve networking knowledge 
- Learn automation with Bash
- Monitor server performance
- Build a professional GitHub portfolio
- Document every step for future reference

# Current Progress

- [x] Installed Ubuntu Desktop 24.04 LTS
- [x] Configured SSH for remote administration
- [x] Installed and configured NoMachine
- [x] Configured headless remote desktop access
- [x] Installed Cockpit for web-based server management
- [x] Install Docker
- [x] Install Docker Compose
- [x] Deploy Jellyfin Media Server
- [x] Configure Portainer
- [x] Configure Tailscale for secure remote access
- [ ] Set up automated backups


# Project Milestones

### Phase 1: Server Setup 
- [x] Install Ubuntu Desktop 24.04 LTS
- [x] Configure SSH
- [x] Configure headless remote access
- [x] Install Cockpit

### Phase 2: Containerization 
- [x] Install Docker
- [x] Install Docker Compose
- [x] Install Portainer

### Phase 3: Media Server 
- [x] Install Jellyfin
- [x] Configure media libraries
- [x] Enable hardware acceleration 

### Phase 4: Media Automation 
- [x] Install Sonarr
- [x] Install Radarr
- [x] Install Prowlarr
- [ ] Configure qBittorrent

### Phase 5: Remote Access 
- [x] Configure Tailscale
- [x] Enable secure remote streaming
- [ ] Configure reverse proxy 

### Phase 6: Monitoring 
- [ ] Install Grafana
- [ ] Install Prometheus
- [ ] Configure automated backups



# Future Projects

- Docker Compose Lab
- Jellyfin Media Server
- Automated Backups
- Reverse Proxy
- Monitoring Dashboard
- Home Network Documentation
- Bash Automation Scripts
- Infrastructure as Code
- Docker Container Management
- Secure Remote Access

 # Screenshots

Screenshots of the homelab setup, dashboards, services, and network diagrams will be added as the project grows.


# Author

**Abdalhakeem Saeed**
