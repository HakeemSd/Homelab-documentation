# Prowlarr

## Purpose

Prowlarr is a self-hosted indexer manager and proxy. It provides one central location for managing compatible Torrent and Usenet indexers and can synchronize them with applications such as Sonarr and Radarr.

Prowlarr does not provide media or downloads by itself. Indexers, download clients, and media sources must be configured separately and used only for content that I am legally authorized to access.

---

## Prerequisites

- Ubuntu Desktop 24.04 LTS
- Docker Engine
- Docker Compose
- Sonarr
- Radarr
- Homepage
- Tailscale

---

## Installation

### Create the Prowlarr directory

```bash
mkdir -p ~/docker/prowlarr
cd ~/docker/prowlarr
```

### Create the Docker Compose file

Create:

```text
docker-compose.yml
```

The Compose configuration is stored in:

```text
docker/prowlarr/docker-compose.yml
```

### Start Prowlarr

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
docker compose logs --tail 50 prowlarr
```

---

## Access Prowlarr

Open a browser on the local network and navigate to:

```text
http://<SERVER-IP>:9696
```

Prowlarr can also be accessed remotely through Tailscale:

```text
http://<TAILSCALE-IP>:9696
```

The exact IP addresses are intentionally omitted from this public repository.

---

## Authentication

Prowlarr authentication was configured using:

```text
Forms (Login Page)
```

Authentication is required for both local and remote connections.

Credentials, API keys, authentication links, and tokens are not stored in this repository.

---

## What Is an Indexer?

An indexer is a search service that returns available releases to applications such as Sonarr and Radarr.

Prowlarr supports:

- Torrent trackers and indexers
- Usenet indexers

Prowlarr allows compatible indexers to be configured once and synchronized with multiple applications.

Only authorized and legal sources should be configured.

---

## Application Integration

Prowlarr can synchronize indexer settings with Sonarr and Radarr.

Applications are configured through:

```text
Settings → Apps
```

Each application requires:

- Application URL
- API key
- Synchronization level

API keys are intentionally excluded from this public repository.

---

## Current Status

- [x] Prowlarr installed
- [x] Running in Docker
- [x] Web dashboard accessible
- [x] Authentication configured
- [x] Added to Homepage
- [ ] Sonarr application connected
- [ ] Radarr application connected
- [ ] Authorized indexer configured
- [ ] Download client configured
- [ ] Automated backup configured

---

## What I Learned

- How Prowlarr centralizes indexer management
- The difference between an indexer and a download client
- How Prowlarr integrates with Sonarr and Radarr
- How API keys allow self-hosted applications to communicate
- How Docker Compose deploys and preserves Prowlarr configuration
- Why credentials and API keys should not be committed to GitHub

---

## Screenshot

![Prowlarr Dashboard](../screenshots/prowlarr-dashboard.png)

---

## Future Improvements

- Connect Prowlarr to Sonarr
- Connect Prowlarr to Radarr
- Configure an authorized indexer
- Add a legal download client
- Test application synchronization
- Configure automated backups
- Add Prowlarr status information to Homepage