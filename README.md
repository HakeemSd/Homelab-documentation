
# 🏠 Self-Hosted Infrastructure Homelab

![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04-E95420?logo=ubuntu&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker%20Compose-2496ED?logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white)
![YAML](https://img.shields.io/badge/YAML-CB171E?logo=yaml&logoColor=white)
![Tailscale](https://img.shields.io/badge/Tailscale-242424?logo=tailscale&logoColor=white)
![Portainer](https://img.shields.io/badge/Portainer-13BEF9?logo=portainer&logoColor=white)
![Homepage](https://img.shields.io/badge/Homepage-3B82F6)
![Jellyfin](https://img.shields.io/badge/Jellyfin-00A4DC?logo=jellyfin&logoColor=white)
![Sonarr](https://img.shields.io/badge/Sonarr-35C5F0)
![Radarr](https://img.shields.io/badge/Radarr-FFC230)
![Prowlarr](https://img.shields.io/badge/Prowlarr-FF6A00)
![Grafana](https://img.shields.io/badge/Grafana-F46800?logo=grafana&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?logo=prometheus&logoColor=white)
![Node Exporter](https://img.shields.io/badge/Node%20Exporter-000000?logo=prometheus&logoColor=white)
![cAdvisor](https://img.shields.io/badge/cAdvisor-4285F4)
![Uptime Kuma](https://img.shields.io/badge/Uptime%20Kuma-5CDD8B)
![Nginx Proxy Manager](https://img.shields.io/badge/Nginx%20Proxy%20Manager-009639)

A self-hosted homelab built on a **Qotom Mini PC** running **Ubuntu 24.04 LTS**, showcasing practical experience with Linux, Docker, networking, monitoring, and self-hosted infrastructure.

This homelab documents the design, deployment, and maintenance of a self-hosted infrastructure built on Ubuntu 24.04 using Docker and Docker Compose. Throughout this project, I have deployed and managed services including **Portainer, Homepage, Jellyfin, Sonarr, Radarr, Prowlarr, Grafana, Prometheus, Uptime Kuma, Tailscale, Node Exporter, cAdvisor, and Nginx Proxy Manager** while developing hands-on experience with **Linux administration, containerization, Docker networking, reverse proxies, monitoring and observability, VPN configuration, Git, GitHub, YAML, and infrastructure documentation**.

---

##  Project Highlights

- Built a complete self-hosted infrastructure from the ground up on Ubuntu 24.04.
- Deployed and manage 10+ Docker services using Docker Compose.
- Configured Nginx Proxy Manager with clean `.home.arpa` domains.
- Built a monitoring stack with Prometheus, Grafana, Node Exporter, cAdvisor, and Uptime Kuma.
- Configured secure remote administration using Tailscale VPN.
- Maintain documentation, Docker Compose files, and screenshots for every deployed service.

---

##  Hardware

| Component | Specification |
|---|---|
| Mini PC | Qotom Intel Celeron J1900 |
| RAM | 8 GB DDR3 |
| Storage | 128 GB SSD |
| OS | Ubuntu Desktop 24.04 LTS |

##  Technologies Used

Ubuntu • Linux • Docker • Docker Compose • Portainer • Homepage • Jellyfin • Sonarr • Radarr • Prowlarr • Grafana • Prometheus • Node Exporter • cAdvisor • Uptime Kuma • Nginx Proxy Manager • Tailscale • Git • GitHub • YAML

##  Architecture

```text
Internet
   │
Tailscale VPN
   │
Ubuntu 24.04 (Qotom)
   │
Docker Engine
   ├── Nginx Proxy Manager
   ├── Homepage
   ├── Portainer
   ├── Jellyfin
   ├── Sonarr
   ├── Radarr
   ├── Prowlarr
   ├── Prometheus
   ├── Grafana
   ├── Node Exporter
   ├── cAdvisor
   └── Uptime Kuma
```

##  Reverse Proxy

Uses **Nginx Proxy Manager** with local domains:

- homepage.home.arpa
- portainer.home.arpa
- jellyfin.home.arpa
- sonarr.home.arpa
- radarr.home.arpa
- prowlarr.home.arpa
- grafana.home.arpa
- prometheus.home.arpa
- uptime.home.arpa
- npm.home.arpa

##  Monitoring Stack

| Tool | Purpose |
|---|---|
| Prometheus | Collect metrics |
| Grafana | Visualize metrics |
| Node Exporter | Host metrics |
| cAdvisor | Container metrics |
| Uptime Kuma | Availability monitoring |

## ✅ Current Stack

Ubuntu • Docker • Docker Compose • Portainer • Homepage • Jellyfin • Sonarr • Radarr • Prowlarr • Tailscale • Grafana • Prometheus • Node Exporter • cAdvisor • Uptime Kuma • Nginx Proxy Manager

##  Repository Structure

```text
docker/
docs/
screenshots/
README.md
```

##  Skills Demonstrated

- Linux Administration
- Docker & Docker Compose
- Docker Networking
- Reverse Proxy Configuration
- Monitoring & Observability
- VPN Configuration
- Git & GitHub
- YAML
- Self-Hosting
- Infrastructure Documentation

##  Roadmap

✅ Section 1 – Core Infrastructure
 [x] Ubuntu 24.04 LTS
 
 [x] SSH
 
 [x] NoMachine
 
 [x] Docker
 
 [x] Docker Compose
 
 [x] Portainer
 
 [x] Homepage
 
 [x] Jellyfin
 
 [x] Tailscale
 
 [x] Sonarr
 
 [x] Radarr
 
 [x] Prowlarr

 ✅ Section 2 – Infrastructure & Monitoring
 
 [x] Uptime Kuma
 
 [x] Grafana
 
 [x] Prometheus
 
 [x] Node Exporter
 
 [x] cAdvisor
 
 [x] Nginx Proxy Manager
 
 [x] Reverse Proxy Configuration
 
 [ ] Watchtower
 
 [ ] Automatic Backups

 Section 3 – Media Stack
 
 [ ] Bazarr
 
 [ ] Configure Sonarr
 
 [ ] Configure Radarr
 
 [ ] Configure Prowlarr
 
 [ ] Add External Storage
 
 [ ] Hardware Acceleration
 
 [ ] Mobile Streaming

### Next
- Homepage widgets
- Watchtower
- Automated backups
- Authentik
- Immich
- Nextcloud

## 📈 Future Goals

- # 🎯 Future Goals

- Expand the Jellyfin media library
- Complete the Arr stack with Bazarr
- Implement automated Docker backups
- Configure Watchtower for container updates
- Build more advanced Grafana dashboards
- Learn Docker networking in greater depth
- Learn Infrastructure as Code (Terraform & Ansible)
- Learn Kubernetes fundamentals
- Continue improving Linux administration skills
- Continue developing DevOps and Systems Administration knowledge
