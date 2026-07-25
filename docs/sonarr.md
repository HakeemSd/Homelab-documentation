# Sonarr

## Purpose

Sonarr is a self-hosted TV series management application. It is used to monitor, organize, rename, and manage TV show files for my Jellyfin media library.

Sonarr does not provide media by itself. It manages files and services that are configured separately.

---

## Prerequisites

- Ubuntu Desktop 24.04 LTS
- Docker Engine
- Docker Compose
- Jellyfin
- A TV media directory
- Tailscale for secure remote access

---

## Folder Structure

The TV media directory on the Ubuntu server is:

```text
/home/ahmad-saeed/media/tv
```

Inside the Sonarr container, the media directory is available as:

```text
/data/tv
```

---

## Installation

### Create the Sonarr directory

```bash
mkdir -p ~/docker/sonarr
mkdir -p ~/media/tv
cd ~/docker/sonarr
```

### Create the Docker Compose file

Create:

```text
docker-compose.yml
```

The Compose configuration is stored in:

```text
docker/sonarr/docker-compose.yml
```

### Start Sonarr

```bash
docker compose up -d
```

### Verify the container

```bash
docker compose ps
```

or:

```bash
docker ps
```

### View logs

```bash
docker compose logs --tail 50 sonarr
```

---

## Access Sonarr

Open a browser on the local network and navigate to:

```text
http://<SERVER-IP>:8989
```

Sonarr can also be reached remotely through the server's Tailscale address:

```text
http://<TAILSCALE-IP>:8989
```

The exact IP addresses are intentionally omitted from this public repository.

---

## Authentication

Sonarr authentication was configured using:

```text
Forms (Login Page)
```

Authentication is required for both local and remote connections.

Credentials are not stored in this repository.

---

## Media Management

The Sonarr root folder is:

```text
/data/tv
```

The following media-management options were enabled:

- Rename Episodes
- Create Empty Series Folders
- Use Hardlinks Instead of Copy

These settings help keep the TV library organized for Jellyfin.

---

## Current Status

- [x] Sonarr installed
- [x] Running in Docker
- [x] Web dashboard accessible
- [x] Authentication configured
- [x] TV root folder configured
- [x] Added to Homepage
- [ ] Download client configured
- [ ] Indexer manager configured
- [ ] Test series imported
- [ ] Automated backup configured

---

## What I Learned

- How to deploy Sonarr with Docker Compose
- How PUID and PGID help control container file permissions
- How Docker volume mappings connect host folders to container paths
- How Sonarr organizes and renames TV show files
- How to secure a self-hosted application with authentication
- How consistent container paths simplify media-management services

---

## Screenshot

![Sonarr Dashboard](../screenshots/sonarr-dashboard.png)

---

## Future Improvements

- Add Radarr for movie management
- Add Prowlarr for centralized indexer management
- Connect a legal download client
- Test importing and organizing a TV episode
- Add Sonarr container status to Homepage
- Configure automated backups