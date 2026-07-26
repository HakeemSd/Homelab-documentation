# Homelab Documentation

![GitHub last commit](https://img.shields.io/github/last-commit/HakeemSd/Homelab-documentation?style=for-the-badge)
![GitHub repo size](https://img.shields.io/github/repo-size/HakeemSd/Homelab-documentation?style=for-the-badge)
![GitHub stars](https://img.shields.io/github/stars/HakeemSd/Homelab-documentation?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-23+-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Status](https://img.shields.io/badge/Project-Active-success?style=for-the-badge)

---

# Homelab Overview

This project documents the design, deployment, and maintenance of my self-hosted homelab built on an Ubuntu Mini PC.

The goal of this project is to gain hands-on experience with Linux administration, Docker, networking, reverse proxies, monitoring, automation, and self-hosted services while documenting everything as if it were a real production environment.

The homelab has grown from a simple Jellyfin server into a complete self-hosted environment featuring centralized monitoring, secure remote access, automated media management, and service monitoring.

---

# What I Learned

Throughout this project I gained practical experience with:

- Linux server administration
- Docker & Docker Compose
- Reverse proxy configuration using Nginx Proxy Manager
- VPN networking using Tailscale
- Container management with Portainer
- Monitoring using Grafana, Prometheus, cAdvisor, and Node Exporter
- Service monitoring with Uptime Kuma
- Automated media management using Sonarr, Radarr, Prowlarr, and SABnzbd
- Git & GitHub documentation
- Docker networking and persistent volumes
- Troubleshooting containerized applications
- Building and documenting production-style infrastructure

---

# Architecture

```text
                           Internet
                               │
                               ▼
                        Tailscale VPN
                               │
                               ▼
                      Ubuntu Mini PC Server
                               │
        ┌──────────────────────┼──────────────────────┐
        │                      │                      │
        ▼                      ▼                      ▼
   Homepage              Nginx Proxy Manager     Monitoring
                              │
        ┌─────────────────────┴─────────────────────┐
        │                                           │
        ▼                                           ▼
    Jellyfin                                    Portainer

                    Automated Media Stack

               Sonarr          Radarr
                    │             │
                    └──────┬──────┘
                           ▼
                      Prowlarr
                           │
                           ▼
                        SABnzbd
                           │
                           ▼
                         Eweka
                           │
                           ▼
               /media/movies
               /media/tv
                           │
                           ▼
                        Jellyfin
```

---

# Services

## Dashboard

- Homepage

## Infrastructure

- Ubuntu Server
- Docker
- Docker Compose
- Portainer
- Nginx Proxy Manager
- Tailscale

## Monitoring

- Grafana
- Prometheus
- cAdvisor
- Node Exporter
- Uptime Kuma

## Media Stack

- Jellyfin
- Sonarr
- Radarr
- Prowlarr
- SABnzbd
- Eweka

---

# Features

- Docker-based deployment
- Homepage dashboard
- Reverse proxy with Nginx Proxy Manager
- Secure remote access through Tailscale
- Grafana dashboards
- Prometheus metrics
- Container monitoring with cAdvisor
- Ubuntu monitoring with Node Exporter
- Container management using Portainer
- Service monitoring with Uptime Kuma
- Jellyfin media server
- Automated TV management
- Automated movie management
- Automated Usenet downloads
- Automatic media importing into Jellyfin

---

# Automated Media Workflow

The media stack is fully automated.

1. Sonarr monitors TV shows.
2. Radarr monitors movies.
3. Prowlarr searches configured indexers.
4. SABnzbd downloads through Eweka.
5. Downloads are automatically imported.
6. Jellyfin automatically detects new media.

---

# Project Progress

## Core Infrastructure

- [x] Ubuntu Server
- [x] Docker
- [x] Docker Compose
- [x] Homepage
- [x] Portainer
- [x] Nginx Proxy Manager
- [x] Tailscale

---

## Monitoring

- [x] Grafana
- [x] Prometheus
- [x] cAdvisor
- [x] Node Exporter
- [x] Uptime Kuma

---

## Media Stack

- [x] Jellyfin
- [x] Sonarr
- [x] Radarr
- [x] Prowlarr
- [x] SABnzbd
- [x] Eweka
- [x] Automatic Movie Downloads
- [x] Automatic TV Downloads
- [x] Automatic Library Imports

---

## In Progress

- [ ] Homepage API Widgets
- [ ] External SSD
- [ ] Automatic Backups
- [ ] HTTPS for Every Service
- [ ] Custom Homepage Dashboard

---

## Future Goals

- [ ] Authentik (Single Sign-On)
- [ ] CrowdSec
- [ ] Fail2Ban
- [ ] Custom Grafana Dashboards
- [ ] Automatic Docker Updates
- [ ] Off-site Backups
- [ ] Docker Secrets
- [ ] Centralized Logging

---

# Screenshots

## Homepage Dashboard

![Homepage](screenshots/homepage-dashboard.png)

## Grafana

![Grafana](screenshots/grafana.png)

## Portainer

![Portainer](screenshots/portainer.png)

## Jellyfin

![Jellyfin](screenshots/jellyfin.png)

---

# Future Expansion

Planned additions include:

- External SSD storage
- Authentik authentication
- HTTPS certificates for every service
- Docker Secrets
- Automatic backups
- Grafana custom dashboards
- Additional monitoring
- More self-hosted applications

---

# Repository Structure

```
Homelab-documentation/
│
├── README.md
├── screenshots/
│
├── docker/
│   ├── homepage/
│   ├── jellyfin/
│   ├── sonarr/
│   ├── radarr/
│   ├── prowlarr/
│   ├── sabnzbd/
│   ├── grafana/
│   ├── prometheus/
│   ├── portainer/
│   ├── uptime-kuma/
│   └── nginx-proxy-manager/
│
└── docs/
```

---

# License

This repository is intended for educational purposes and documents my personal homelab learning journey.