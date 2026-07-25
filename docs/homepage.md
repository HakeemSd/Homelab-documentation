# Homepage

## Purpose

Homepage is a self-hosted dashboard that provides a central location to access all services running in my homelab. It allows me to quickly launch applications, monitor system resources, and organize links to my self-hosted services.

---

## Prerequisites

- Ubuntu Desktop 24.04 LTS
- Docker Engine
- Docker Compose
- Running Docker services (Portainer, Jellyfin, etc.)

---

## Installation

### Create the Homepage directory

```bash
mkdir -p ~/docker/homepage
cd ~/docker/homepage
```

### Create the Docker Compose file

Create:

```text
docker-compose.yml
```

Paste the Homepage Docker Compose configuration into the file.

### Start Homepage

```bash
docker compose up -d
```

### Verify the container

```bash
docker compose ps
```

or

```bash
docker ps
```

---

## Access Homepage

Open a web browser and navigate to:

```text
http://<SERVER-IP>:3000
```

Example:

```text
http://10.0.0.xxx:3000
```

The exact server IP is intentionally omitted from this public repository.

---

## Configuration

Homepage configuration files are stored in:

```text
~/docker/homepage/config/
```

Key configuration files include:

- services.yaml
- bookmarks.yaml
- widgets.yaml
- settings.yaml

These files allow customization of services, bookmarks, widgets, themes, and dashboard settings.

---

## Current Status

- [x] Homepage installed
- [x] Running in Docker
- [x] Dashboard accessible
- [x] Portainer added
- [x] Jellyfin added
- [x] Resource widgets configured
- [ ] Additional services added
- [ ] Custom icons configured

---

## What I Learned

- How to deploy another Docker application using Docker Compose
- How Homepage stores configuration using YAML files
- How to organize homelab services into groups
- How Docker bind mounts preserve application configuration
- How a centralized dashboard simplifies management of multiple self-hosted services

---

## Screenshot

![Homepage Dashboard](../screenshots/homepage-dashboard.png)

---

## Future Improvements

- Add Sonarr
- Add Radarr
- Add Prowlarr
- Add qBittorrent
- Add Bazarr
- Configure custom icons
- Add weather and calendar widgets
- Monitor Docker containers directly from Homepage